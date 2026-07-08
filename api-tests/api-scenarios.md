# Testy API (RESTful Booker)

W ramach weryfikacji warstwy backendowej, przygotowałem kolekcję zapytań w narzędziu **Postman**. Testy opierają się na publicznym API RESTful Booker.

Plik z pełną kolekcją (`.json`) gotową do zaimportowania w Postmanie znajduje się w tym folderze.

## Scenariusze Testowe

### 1. Pobranie listy rezerwacji (Happy Path)
* **Metoda:** `GET`
* **Endpoint:** `https://restful-booker.herokuapp.com/booking`
* **Cel testu:** Weryfikacja, czy serwer poprawnie zwraca listę aktualnych rezerwacji.
* **Zastosowane asercje w Postmanie:**
  * Sprawdzenie, czy kod odpowiedzi (Status Code) to `200 OK`.
  * Sprawdzenie, czy czas odpowiedzi jest krótszy niż 1000ms.

### 2. Autoryzacja i generowanie tokenu (Happy Path)
* **Metoda:** `POST`
* **Endpoint:** `https://restful-booker.herokuapp.com/auth`
* **Cel testu:** Logowanie do API w celu uzyskania tokenu zabezpieczającego niezbędnego do operacji PUT/DELETE.
* **Wysłany Body (JSON):**
  ```json
  {
      "username" : "admin",
      "password" : "password123"
  }
  ```
* **Zastosowane asercje w Postmanie:**
  * Sprawdzenie, czy kod odpowiedzi (Status Code) to `200 OK`.
  * Weryfikacja, czy odpowiedź zawiera wygenerowany ciąg znaków (token).

### 3. Błędna autoryzacja (Ścieżka negatywna)
* **Metoda:** `POST`
* **Endpoint:** `https://restful-booker.herokuapp.com/auth`
* **Cel testu:** Sprawdzenie zabezpieczeń API poprzez wysłanie niepoprawnego hasła.
* **Wysłany Body (JSON):**
  ```json
  {
      "username" : "admin",
      "password" : "wrong_password"
  }
  ```
  * **Zastosowane asercje w Postmanie:**
  * Sprawdzenie, czy odpowiedź serwera zawiera komunikat błędu (np. Bad credentials).