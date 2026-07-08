# E-commerce QA Testing Portfolio

Ten projekt to kompleksowa dokumentacja procesu testowania (STLC) dla platformy e-commerce (Swag Labs / SauceDemo) oraz testów API (RESTful Booker). 

Projekt ma na celu zaprezentowanie mojego warsztatu jako Młodszego Testera Manualnego (Junior QA) z uwzględnieniem analizy wymagań, projektowania przypadków testowych, raportowania błędów oraz testów API.

## Wykorzystane Narzędzia i Środowisko
* **Środowisko testowe:** macOS (Apple Silicon M2), Safari 18.5
* **Zarządzanie testami:** Markdown, GitHub Codespaces
* **Bug Tracking:** GitHub Issues (z użyciem niestandardowych szablonów)
* **Testy API:** Postman
* **Narzędzia analityczne:** Safari Web Inspector (DevTools)

## Struktura Projektu

Poniżej znajdziesz bezpośrednie linki do najważniejszych elementów mojego procesu testowego:

### 1. Dokumentacja Testów UI
* [Plan Testów (Test Plan)](./test-plan/test-plan.md)
* [Moduł Logowania](./test-cases/login-tests.md)
* [Katalog Produktów i Sortowanie](./test-cases/inventory-tests.md)
* [Zarządzanie Koszykiem](./test-cases/cart-tests.md)
* [Proces Zakupowy (Checkout)](./test-cases/checkout-tests.md) *(Błąd Krytyczny!)*
* [Bezpieczeństwo i Sesja](./test-cases/security-tests.md)
* [Testy Responsywności (iPhone / Mobile)](./test-cases/mobile-tests.md)

### 2. Poza Utartym Szlakiem (Bazy danych i Exploratory)
* [Karta Testów Eksploracyjnych (Exploratory Session)](./exploratory-testing/session-01.md)
* [Weryfikacja defektów w bazie (SQL)](./database-queries/sql-examples.md)

### 3. Zgłaszanie Błędów
* [Zobacz profesjonalnie zgłoszony Bug (GitHub Issues)](../../issues)

### 4. Testy API (RESTful Booker)
* [Dokumentacja Scenariuszy API](./api-tests/api-scenarios.md)

### 5. Podsumowanie
* [Raport z Wykonania Testów i Rekomendacja (Test Execution Summary)](./test-execution-summary.md)