# Przypadki testowe: Katalog Produktów (Inventory)

| ID | Moduł | Tytuł | Warunki Wstępne | Kroki do wykonania | Oczekiwany Rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-INV-01 | Katalog | Sortowanie po cenie od najniższej (Low to High) | Zalogowany jako `standard_user`, strona główna katalogu. | 1. Kliknij listę rozwijaną sortowania (prawy górny róg).<br>2. Wybierz "Price (low to high)".<br>3. Przejrzyj ceny pierwszego i ostatniego produktu. | Lista przeładowuje się. Pierwszy produkt na liście jest najtańszy (np. $7.99), a ostatni najdroższy (np. $49.99). Produkty wyświetlają się w porządku rosnącym. | ✅ **PASS** |