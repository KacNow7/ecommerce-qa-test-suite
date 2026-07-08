# Przypadki testowe: Logowanie (Login)

| ID | Moduł | Tytuł | Warunki wstępne | Kroki do wykonania | Oczekiwany rezultat | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TC-LOG-01 | Logowanie | Poprawne logowanie | Użytkownik jest na stronie głównej | 1. Wpisz login: `standard_user`<br>2. Wpisz hasło: `secret_sauce`<br>3. Kliknij "Login" | Przekierowanie do katalogu produktów (/inventory.html). Wyświetla się lista produktów. | ✅ **PASS** |
| TC-LOG-02 | Logowanie | Logowanie zablokowanego użytkownika | Użytkownik jest na stronie głównej | 1. Wpisz login: `locked_out_user`<br>2. Wpisz hasło: `secret_sauce`<br>3. Kliknij "Login" | System wyświetla czerwony komunikat błędu: "Epic sadface: Sorry, this user has been locked out." Użytkownik nie zostaje zalogowany. | ✅ **PASS** |