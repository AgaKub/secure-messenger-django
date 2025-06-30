# Projekt: Secure Messenger (wersja Django)

## 1. Opis projektu

Django'owa wersja bezpiecznego komunikatora, bazująca na logice i strukturze projektu konsolowego. Aplikacja umożliwia:

* Rejestrację użytkowników
* Przechowywanie danych użytkowników w bazie danych
* Możliwość rozbudowy o szyfrowanie, logowanie, wysyłkę wiadomości itd.

---

## 2. Struktura katalogów

```
secure-messenger-django/
├── messenger/               # Nasza główna aplikacja Django
│   ├── __init__.py
│   ├── admin.py             # Rejestracja modeli w panelu admina
│   ├── apps.py              # Konfiguracja aplikacji
│   ├── migrations/          # Pliki migracji bazy danych
│   ├── models.py            # Modele danych (np. UserProfile)
│   ├── tests.py
│   └── views.py             # Widoki aplikacji (na razie puste)
├── secure_messenger/        # Ustawienia całego projektu
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py                # Plik startowy Django
└── README.md                # Ten plik
```

---

## 3. Instalacja i uruchomienie

> 💬 *Poniższe kroki są przeznaczone dla nowych użytkowników projektu lub do ponownego uruchomienia projektu na innym komputerze.*
> *Jeśli masz już Django zainstalowane i środowisko gotowe — możesz pominąć część związaną z instalacją.*

### Krok 1. Stwórz środowisko wirtualne (opcjonalnie, ale zalecane)

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

### Krok 2. Zainstaluj Django

```bash
pip install django
```

### Krok 3. Wykonaj migracje bazy danych

```bash
python manage.py makemigrations
python manage.py migrate
```

### Krok 4. Uruchom lokalny serwer developerski

```bash
python manage.py runserver
```

Aplikacja powinna działać pod adresem: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 4. Co dalej?

W kolejnym etapie planujemy:

* Zbudować system rejestracji i logowania
* Dodać funkcję tworzenia i szyfrowania wiadomości
* Zintegrować klucze RSA i AES podobnie jak w wersji konsolowej

---

## 5. Autorzy

* Aga: migracja projektu do Django, struktura bazy danych, README
* Grzesiek: wersja konsolowa i pełna dokumentacja bezpieczeństwa

---

## 6. Jak uruchomić projekt lokalnie (dla Grześka)

1. Sklonuj repozytorium:

```bash
git clone [TUTAJ LINK DO REPO]
```

2. Przejdź do katalogu projektu:

```bash
cd secure-messenger-django
```

3. Aktywuj środowisko wirtualne i zainstaluj wymagane biblioteki (jeśli potrzebne):

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
pip install django
```

4. Wykonaj migracje:

```bash
python manage.py makemigrations
python manage.py migrate
```

5. Uruchom serwer lokalny:

```bash
python manage.py runserver
```

**Do uruchomienia wymagany jest Python 3.10+ i Django 5+**


