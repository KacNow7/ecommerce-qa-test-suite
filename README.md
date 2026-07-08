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

### 1. Planowanie i Strategia
* [Plan Testów (Test Plan)](./test-plan/test-plan.md) - Zakres, środowisko i kryteria akceptacji.

### 2. Przypadki Testowe UI (Test Cases)
* [Moduł Logowania](./test-cases/login-tests.md)
* [Katalog Produktów i Sortowanie](./test-cases/inventory-tests.md)
* [Zarządzanie Koszykiem](./test-cases/cart-tests.md)
* [Proces Zakupowy (Checkout)](./test-cases/checkout-tests.md) *(Zawiera przypadek negatywny z krytycznym błędem)*
* [Bezpieczeństwo i Sesja](./test-cases/security-tests.md)

### 3. Raportowanie Błędów (Bug Tracking)
Wykryte błędy są na bieżąco raportowane w systemie śledzenia.
* [Zobacz zgłoszone błędy (GitHub Issues)](../../issues)

### 4. Testy API (Postman)
* [Dokumentacja Scenariuszy API](./api-tests/api-scenarios.md)
* [Kolekcja Postman do pobrania (.json)](./api-tests/Ecommerce_API_Tests.json)

### 5. Podsumowanie
* [Raport z Wykonania Testów (Test Execution Summary)](./test-execution-summary.md) - Wyniki kampanii testowej i ostateczna rekomendacja wdrożeniowa (Go/No-Go).
