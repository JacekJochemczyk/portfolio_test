# Portfolio - Jacek Jochemczyk

Nowoczesne portfolio techniczne stworzone w Astro jako zamiennik wcześniejszej strony opartej na WordPressie.

Celem projektu było przygotowanie lekkiej, szybkiej i łatwej w utrzymaniu strony prezentującej moje doświadczenie, projekty, certyfikaty i zainteresowania związane z IT, monitoringiem, cyberbezpieczeństwem i programowaniem.

## Technologie

- Astro
- TypeScript
- HTML / CSS / JavaScript
- Docker
- Docker Compose
- Nginx
- Git / GitHub
- Oracle Linux

## Główne funkcje

- responsywny interfejs na komputer i telefon
- menu hamburgerowe na urządzeniach mobilnych
- sekcja "O mnie"
- panel statusu aplikacji
- nieskończona karuzela projektów
- obracane karty projektów z listą technologii
- sekcja certyfikatów w formie akordeonu
- pełnoekranowy podgląd certyfikatów
- linki do GitHub i LinkedIn
- możliwość pobrania CV
- responsywna stopka z danymi kontaktowymi

## Struktura danych

Dane projektów i certyfikatów zostały oddzielone od komponentów:

src/data/projects.ts
src/data/certificates.ts

Dzięki temu dodanie kolejnego projektu lub certyfikatu nie wymaga przebudowy całej sekcji.

## Docker

Projekt jest uruchamiany w kontenerze Docker.

Budowa odbywa się w dwóch etapach:
1. Node.js buduje statyczną wersję Astro.
2. Gotowe pliki trafiają do lekkiego kontenera Nginx.

Uruchomienie:

docker compose up -d

Przebudowanie po zmianach:

docker compose up -d --build

## Tryb developerski

Do pracy nad stroną lokalnie:

npm run dev -- --host 0.0.0.0

Domyślny port: 4321

## Dlaczego taki stack?

Astro zostało wybrane, ponieważ portfolio nie potrzebuje rozbudowanego backendu ani bazy danych.

Docker i Docker Compose pozwalają uruchamiać projekt w powtarzalnym środowisku i przygotowują go pod późniejsze wdrożenie na serwerze.

Nginx służy do serwowania gotowej statycznej strony.

## Plan wdrożenia

Docelowo portfolio będzie działać pod:

https://jacekjochemczyk.pl

Planowane środowisko:
- Oracle Cloud
- Oracle Linux
- Docker
- Nginx
- Astro

W przyszłości planowane jest również:
- wdrożenie na ARM64
- GitHub Actions
- GitHub Container Registry
- automatyczne budowanie obrazów
- dynamiczne sprawdzanie statusu aplikacji
- dodatkowe zabezpieczenia i nagłówki bezpieczeństwa

## Autor

Jacek Jochemczyk

GitHub:
https://github.com/JacekJochemczyk

LinkedIn:
https://www.linkedin.com/in/jacek-jochemczyk-266a2b340/
