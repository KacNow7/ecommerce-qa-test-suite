# Sesja Testów Eksploracyjnych (Exploratory Testing Charter)

**Data sesji:** 9 lipca 2026
**Cel misji:** Próba ominięcia walidacji w formularzu Checkout poprzez wstrzykiwanie znaków specjalnych i kodu (XSS) oraz sprawdzanie limitów znaków.
**Czas trwania sesji:** 45 minut
**Tester:** QA Junior

## Notatki z testów:
1. **Pola tekstowe (First Name, Last Name):** Przetestowano wpisywanie cyfr i znaków specjalnych (np. `@!#`). System akceptuje dowolne znaki. Brakuje walidacji dla imion (Defekt UX).
2. **Próba XSS (Cross-Site Scripting):** Wpisałem prosty skrypt `<script>alert('Test')</script>` w pole "Zip/Postal Code".
   * *Wynik:* Skrypt nie został wywołany na stronie podsumowania. System prawidłowo formatuje znaki jako zwykły tekst. Brak podatności.
3. **Limity znaków:** Wklejono ciąg 500 znaków w pole "First Name".
   * *Wynik:* Formularz to przyjmuje, a strona podsumowania "rozjeżdża się" wizualnie na mniejszych ekranach.

## Konkluzja:
Moduł Checkout jest odporny na podstawowe ataki XSS, ale brakuje mu jakiejkolwiek walidacji wejściowej. Użytkownik może zamówić towar na nazwisko "123" z kodem pocztowym "!@#". Powinno to zostać poprawione w przyszłych sprintach.