# GPW Scraper – Archiwum notowań z GPW zautomatyzowane

Scraper w Pythonie oparty na Selenium, który automatyzuje pobieranie archiwalnych danych giełdowych z portalu GPW: https://www.gpw.pl/archiwum-notowan

# Problem

GPW umożliwia pobranie całej historii notowań tylko dla jednego konkretnego instrumentu (np. WIG20).  
Natomiast dla kategorii takich jak "Akcje" lub "Obligacje skarbowe" nie da się pobrać danych zbiorczych i trzeba klikać osobno każdy dzień.  

Dla badaczy, analityków i studentów to oznacza:
- godziny ręcznego pobierania plików,
- ryzyko pomyłek,
- brak automatyzacji.

# Rozwiązanie

Ten skrypt:
- automatycznie przegląda wskazany zakres dat (np. 2005–2025),
- pobiera pliki `.xls` z notowaniami dla wybranych kategorii (np. Akcje, Indeksy, Obligacje),
- zapisuje każdy dzień jako osobny plik `.xls` (tak jak robi GPW),
- rozwiązuje problem braku masowego eksportu.

Dzięki temu możesz zautomatyzować pozyskiwanie danych do:
- analiz inwestycyjnych,
- backtestów,
- pracy magisterskiej,
- i wszelkich projektów opartych o dane historyczne GPW.

# Pliki wyjściowe

Dane zapisywane są jako osobne pliki `.xls` w folderze `Downloads`.

# Technologie

- Python
- Selenium + Edge WebDriver
- Pandas

# Przykładowe pliki danych

W repozytorium znajdują się przykładowe pliki `.xls` wygenerowane przez scraper dla dnia **2022-01-31**:

- `_2022-01-31_akcje.xls` – notowania akcji,
- `_2022-01-31_indeksy.xls` – notowania indeksów,
- `_2022-01-31_obligacje.xls` – notowania obligacji skarbowych.

Każdy z tych plików został pobrany automatycznie z archiwum GPW i pokazuje strukturę danych, jaką generuje skrypt.
Można je otworzyć bez potrzeby uruchamiania kodu, aby szybko zapoznać się z efektem działania scrapera.
---

Autorka: Arina Reutskaya  
Repozytorium stworzone na potrzeby pracy magisterskiej dot. strategii FIRE w warunkach GPW.
