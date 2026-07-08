# Przypadki testowe: Koszyk (Cart)

| ID | Moduł | Tytuł | Warunki Wstępne | Kroki do wykonania | Oczekiwany Rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-CRT-02 | Koszyk | Usuwanie produktów z poziomu koszyka | Zalogowany jako `standard_user`, koszyk jest pusty. | 1. Dodaj 3 różne produkty do koszyka klikając "Add to cart".<br>2. Zauważ wskaźnik na ikonie koszyka (powinien wynosić '3').<br>3. Kliknij ikonę koszyka, aby przejść do widoku podsumowania.<br>4. Kliknij "Remove" przy jednym z produktów. | Kliknięty produkt znika z listy. Licznik na ikonie koszyka w prawym górnym rogu automatycznie aktualizuje się z '3' na '2' bez konieczności odświeżania strony. | ✅ **PASS** |