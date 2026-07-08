# Przypadki testowe: Kasa (Checkout)

| ID | Moduł | Tytuł | Warunki wstępne | Kroki do wykonania | Oczekiwany rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-CHK-01 | Checkout | Finalizacja zamówienia przy pustym koszyku | Pusty koszyk, zalogowany jako `standard_user` | 1. Kliknij ikonę koszyka.<br>2. Kliknij "Checkout".<br>3. Wypełnij dane dostawy.<br>4. Kliknij "Continue". | System powinien zablokować przejście do kasy i wyświetlić komunikat o pustym koszyku. | ❌ **FAIL** (Zgłoszono Issue #1) |