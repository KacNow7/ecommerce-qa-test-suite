# Raport z Wykonania Testów (Test Execution Summary)

**Data wykonania testów:** 8 lipca 2026
**Środowisko testowe:** macOS (Apple Silicon M2), przeglądarka Safari 18.5
**Testowana platforma:** Swag Labs (saucedemo.com)

## 1. Podsumowanie Metryk (Metrics Summary)
* **Zaplanowane przypadki testowe:** 4
* **Wykonane przypadki testowe:** 4
* **Zaliczone (PASS):** 3
* **Oblane (FAIL):** 1

## 2. Szczegóły Egzekucji (Execution Details)

| ID Testu | Moduł | Status | Uwagi / Zgłoszone Błędy |
| :--- | :--- | :--- | :--- |
| TC-CHK-01 | Checkout | ❌ **FAIL** | Krytyczny błąd biznesowy: system pozwala na Checkout z pustym koszykiem. Zgłoszono w [Issue #1] *(tutaj później wkleisz link do swojego zgłoszenia z GitHuba)* |
| TC-INV-01 | Katalog | ✅ **PASS** | Filtrowanie działa zgodnie z oczekiwaniami. |
| TC-CRT-02 | Koszyk | ✅ **PASS** | Wskaźnik koszyka odświeża się asynchronicznie, bez przeładowania strony. |
| TC-SEC-01 | Sesja | ✅ **PASS** | Mimo wczytania widoku z pamięci cache (Safari), backend prawidłowo blokuje nieautoryzowane zapytania po wylogowaniu. |

## 3. Rekomendacja (QA Sign-off / Go-No-Go Decision)
**Decyzja: NO-GO (Wdrożenie wstrzymane)**
Mimo poprawnego działania modułów asortymentu i koszyka, aplikacja posiada błąd o priorytecie High/Critical w module płatności (TC-CHK-01). Dopóki błąd z możliwością składania "pustych" zamówień nie zostanie naprawiony przez zespół deweloperski, aplikacja nie powinna trafić na środowisko produkcyjne.