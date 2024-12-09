
# Instrukcja obsługi systemu zarządzania użytkownikami

## Wprowadzenie

Ten skrypt umożliwia zarządzanie użytkownikami poprzez dodawanie, edytowanie, usuwanie oraz walidację danych takich jak NIP, PESEL, REGON oraz adres e-mail.

---

## Funkcje

### 1. Dodawanie użytkownika
**Ścieżka:** `add_user()`

Dodaje nowego użytkownika do systemu po zwalidowaniu jego danych.

**Kroki:**
1. Wprowadź dane użytkownika:
   - ID
   - Imię i nazwisko
   - NIP
   - PESEL
   - REGON
   - Email
2. System zweryfikuje poprawność wprowadzonych danych (NIP, PESEL, REGON).
3. W przypadku poprawnych danych użytkownik zostanie zapisany do pliku `data/users.json`.

---

### 2. Edytowanie użytkownika
**Ścieżka:** `edit_user(user_id, updated_data)`

Pozwala na edycję danych istniejącego użytkownika.

**Kroki:**
1. Podaj ID użytkownika, którego dane chcesz edytować.
2. Wprowadź nowe dane do aktualizacji.
3. Zaktualizowane dane zostaną zapisane w pliku `data/users.json`.

---

### 3. Usuwanie użytkownika
**Ścieżka:** `remove_user(user_id)`

Usuwa użytkownika z systemu.

**Kroki:**
1. Podaj ID użytkownika do usunięcia.
2. Użytkownik zostanie usunięty z pliku `data/users.json`.

---

### 4. Walidacja danych
System obsługuje walidację następujących danych:
- **NIP:** Poprawność sprawdzana za pomocą wag kontrolnych.
- **PESEL:** Walidacja daty urodzenia oraz sumy kontrolnej.
- **REGON:** Sprawdzanie długości (9 lub 14 cyfr) i obliczanie sumy kontrolnej.

---

### 5. Generowanie hasła
**Ścieżka:** `generate_password()`

Tworzy silne hasło zawierające:
- Małe i duże litery
- Cyfry
- Znaki specjalne

---

## Struktura plików
- **`data/users.json`:** Plik JSON przechowujący dane użytkowników. Tworzony automatycznie, jeśli nie istnieje.

---

## Przykład uruchomienia
Uruchom skrypt i wybierz jedną z dostępnych opcji:
1. Dodaj użytkownika
2. Edytuj użytkownika
3. Usuń użytkownika

**Przykład:**
```
Wybierz akcję:
1. Dodaj użytkownika
2. Edytuj użytkownika
3. Usuń użytkownika
Wybierz numer akcji: 1
Podaj ID użytkownika: 1
Podaj imię i nazwisko użytkownika: Jan Kowalski
...
```

---

## Uwagi
- Upewnij się, że folder `data` istnieje lub zostanie automatycznie utworzony podczas działania programu.
- Wprowadzone dane muszą spełniać wymagania walidacji.

---

## Autorzy
Maciej Bogusławski
