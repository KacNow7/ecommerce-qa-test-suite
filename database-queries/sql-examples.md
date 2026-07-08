# Weryfikacja Bazy danych (SQL)

W profesjonalnym środowisku QA, błędy UI należy weryfikować na poziomie bazy danych. W nawiązaniu do zgłoszonego błędu krytycznego z pustym koszykiem (Issue #1), poniżej znajdują się przykładowe zapytania SQL, których użyłbym do zweryfikowania, czy i jak system zapisał to błędne zamówienie.

### 1. Sprawdzenie, czy system wygenerował zamówienie z kwotą 0.00
```sql
SELECT order_id, user_id, total_amount, order_date
FROM orders
WHERE total_amount = 0.00 
ORDER BY order_date DESC;
```

---

### 2. Sprawdzenie przypisanych produktów do pustego zamówienia (JOIN)
Oczekujemy, że zamówienie nie będzie miało powiązanych rekordów w tabeli szczegółów.

```sql
SELECT o.order_id, u.username, o.total_amount, od.product_id
FROM orders o
JOIN users u ON o.user_id = u.user_id
LEFT JOIN order_details od ON o.order_id = od.order_id
WHERE o.order_id = 12345;
```

---

# Przypadki testowe: Urządzenia Mobilne (RWD)

Testy przeprowadzone w przeglądarce Safari przy użyciu wbudowanego trybu responsywnego (Responsive Design Mode), symulującego urządzenie iPhone 15 Pro.

| ID | Moduł | Tytuł | Warunki wstępne | Kroki do wykonania | Oczekiwany rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-MOB-01 | UI/UX | Rozwijanie menu bocznego na urządzeniu mobilnym | Zalogowany jako `standard_user`, symulacja iPhone 15 Pro (szerokość ekranu 393px) | 1. Sprawdź widoczność lewego menu (powinno być ukryte pod ikoną "hamburgera").<br>2. Kliknij ikonę trzech poziomych kresek.<br>3. Zweryfikuj, czy animacja jest płynna i czy opcje są klikalne palcem. | Menu płynnie wyjeżdża z lewej strony, przesłaniając produkty. Przyciski są odpowiednio duże dla interfejsu dotykowego (zgodnie z dobrymi praktykami mobile-first). | **PASS** |