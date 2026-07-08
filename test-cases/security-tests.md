# Przypadki testowe: Bezpieczeństwo i Sesja (Security)

| ID | Moduł | Tytuł | Warunki Wstępne | Kroki do wykonania | Oczekiwany Rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-SEC-01 | Sesja | Próba powrotu do sklepu po wylogowaniu za pomocą przycisku przeglądarki "Wstecz" | Zalogowany jako `standard_user`, przebywa na stronie katalogu. | 1. Kliknij menu (trzy poziome kreski) w lewym górnym rogu.<br>2. Kliknij "Logout". (System przenosi na stronę logowania).<br>3. W przeglądarce Safari kliknij przycisk "Wstecz" (strzałka w lewo). | Użytkownik nie zostaje wpuszczony z powrotem do zasobów sklepu. System powinien wymusić ponowne logowanie i ewentualnie wyświetlić komunikat błędu o braku autoryzacji. | ✅ **PASS** |