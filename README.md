# 🕹️ Levels — Zaawansowana Gra Platformowa (Godot 4 / C#)

![C#](https://img.shields.io/badge/C%23-.NET-purple?style=for-the-badge&logo=c-sharp&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)

**Levels** to wymagająca, precyzyjna gra platformowa 2D stworzona w środowisku **Godot Engine 4** przy użyciu języka **C#**. Głównym założeniem projektu było całkowite odejście od gotowych, silnikowych automatów ruchu na rzecz napisania własnej, deterministycznej logiki poruszania się postaci (Physics Engine Bypass), pełnego zrozumienia architektury stanów gry oraz wdrożenia czystych wzorców projektowych w środowisku obiektowym.

---

## 🚀 Kluczowe Rozwiązania Techniczne i Architektura

Projekt służy jako poligon doświadczalny dla zaawansowanych mechanik gamedevu i inżynierii oprogramowania w C#. Skupiłem się w nim na następujących problemach:

1. **Autorski Kontroler Fizyki Postaci (Advanced Kinematic Controller):**
   * **Custom Movement Curve:** Napisanie od zera logiki grawitacji, twardego tarcia kinetycznego, bezwładności oraz asymetrycznej krzywej skoku (szybsze opadanie, zmienna wysokość skoku zależna od czasu wciśnięcia klawisza).
   * **Gładka Interpolacja:** Wykorzystanie metod matematycznych (np. `MoveToward` / `Lerp`) do operacji na wektorach prędkości (`Vector2`), co eliminuje efekt "pływania" i zapewnia idealną responsywność.
   * **Detekcja Środowiskowa:** Zaawansowana weryfikacja stanów `OnFloor` / `InAir` oparta o precyzyjną analizę kolizji, eliminująca błędy utykania postaci w geometriach pionowych.
   * **Gamefeel Tweaks:** Implementacja niewidocznych buforów wejściowych (np. *Coyote Time* oraz *Jump Buffering*), drastycznie podnoszących komfort sterowania.

2. **Zarządzanie Stanem i Cyklem Życia Gry (Game Architecture & Core Loop):**
   * Zastosowanie wzorca **Singleton** do implementacji globalnego menedżera gry (`GameManager`), który kontroluje cykl życia scen, asynchroniczny restart poziomów po kolizji oraz izolację danych sesji.
   * Wykorzystanie architektury sterowanej zdarzeniami (**C# Events & Delegates**) do komunikacji między logiką gry a interfejsem użytkownika, realizując zasadę *Separation of Concerns*.

3. **Modularny System System Triggers & Hazards:**
   * Oprogramowanie generycznego systemu wykrywania kolizji ze strefami śmierci, punktami kontrolnymi (*Checkpoints*) oraz obiektami interaktywnymi z użyciem masek kolizji (*Collision Layers / Masks*).

4. **Odizolowany Interfejs Użytkownika (UI State Management):**
   * System UI monitorujący i renderujący w czasie rzeczywistym parametry rozgrywki (licznik śmierci, milisekundowy stoper czasu rzeczywistego) bez obciążania głównego wątku pętli fizycznej.

---

## 🛠️ Technologie i Narzędzia

* **Silnik gry:** Godot Engine 4.x (wersja .NET Mono)
* **Język programowania:** C# / .NET 6.0+
* **Zarządzanie kodem:** Git / GitHub
* **Paradygmat:** Programowanie Obiektowe (OOP), pełna enkapsulacja logiki, kompozycja ponad dziedziczeniem.

---

## 🎮 Sterowanie

Rozgrywka wymaga chirurgicznej precyzji, do której wykorzystywane są następujące mapowania:
* `Ruch w lewo / prawo` — Klawisze <kbd>A</kbd> / <kbd>D</kbd> lub <kbd>Strzałka w lewo</kbd> / <kbd>w prawo</kbd>
* `Skok` — Klawisz <kbd>Spacja</kbd> / <kbd>W</kbd>
* `Szybki restart` — Automatyczny po śmierci lub wywoływany natychmiastowo z poziomu kodu gry.

---

## 📦 Pobieranie i Uruchomienie (Dla Rekruterów)

Projekt posiada skompilowaną wersję wykonywalną przygotowaną bezpośrednio pod system Windows:

1. Przejdź do zakładki **Releases** w tym repozytorium.
2. Pobierz najnowszą paczkę produkcyjną (np. `Levels-v0.5.3-Alpha-Windows.zip`).
3. Rozpakuj archiwum ZIP w dowolnym katalogu i uruchom plik główny `Levels.exe`.

*Alternatywnie można sklonować repozytorium lokalnie i otworzyć plik `project.godot` bezpośrednio w edytorze Godot Engine (wymagane zainstalowane SDK .NET).*

---

## 🗺️ Roadmap (Najbliższe Kamienie Milowe)

- [ ] **Dynamiczny Level Design:** Implementacja ruchomych platform obliczających i przekazujących swój wektor prędkości na postać gracza (dziedziczenie pędu).
- [ ] **Asynchroniczne ładowanie:** Przebudowa menedżera scen na wielowątkowe ładowanie poziomów w tle przy użyciu mechanizmów `Async/Await` w C#.
- [ ] **Audio System:** Dedykowany mikser audio obsługujący dynamiczne zmiany ścieżki dźwiękowej w zależności od stanu gracza.

---

## 👨‍💻 Autor

**Michał Wojewnik**
* **Portfolio:** [lontem2.github.io](https://lontem2.github.io/)
* **LinkedIn:** [Michał Wojewnik](https://www.linkedin.com/in/micha%C5%82-wojewnik-759baa35b/)
* **E-mail:** [wojewnikmichal@gmail.com](mailto:wojewnikmichal@gmail.com)

---
*Projekt rozwijany jako niezależne portfolio inżynieryjne i pokaz twardych umiejętności programistycznych w technologii .NET.*
