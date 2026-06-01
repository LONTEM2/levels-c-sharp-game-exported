# 🕹️ Levels — Trudna Gra Platformowa (Godot / C#)

![C#](https://img.shields.io/badge/C%23-.NET-purple?style=for-the-badge&logo=c-sharp&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)

**Levels** to wymagająca dwuwymiarowa gra platformowa rozwijana w środowisku **Godot** przy użyciu języka **C#**. Głównym celem tego projektu było odejście od gotowych komponentów na rzecz napisania własnej, zaawansowanej logiki ruchu postaci (Physics Engine Bypass), zrozumienie architektury stanu gry (Game State) oraz optymalizacja struktury kodu pod kątem rozbudowy w architekturze obiektowej.

---

## 🚀 Główne Wyzwania Techniczne i Funkcjonalności

Projekt nie jest jedynie prostą grą – to pokaz moich umiejętności programistycznych w C# i gamedevie. Skupiłem się w nim na następujących aspektach:

1. **Autorski Kontroler Postaci (Advanced Character Controller):**
   * Precyzyjne programowanie fizyki skoku, grawitacji, bezwładności oraz tarcia.
   * Zaawansowana detekcja podłoża (Ground Detection) oparta na rzucaniu promieni (*Raycasting* / *BoxCast*), co zapobiega powszechnym błędom utykania w ścianach.

2. **Architektura Stanu Gry (Game Architecture & Core Loop):**
   * Wdrożenie czystego cyklu życia rozgrywki (ładowanie poziomu, resetowanie stanu po śmierci, płynne przejścia).
   * Zastosowanie wzorców projektowych ułatwiających zarządzanie menedżerami gry (*GameManager*, *UIManager*).

3. **System Przeszkód i Interakcji:**
   * Modularny system kolizji i triggerów obsługujący natychmiastową śmierć gracza, punkty kontrolne (*Checkpoints*) oraz warunki zwycięstwa.

4. **Dynamiczne UI (UI State Management):**
   * Architektura interfejsu na bieżąco zliczająca czas rozgrywki, liczbę prób (licznik śmierci) oraz postęp w czasie rzeczywistym.

---

## 🛠️ Technologie i Narzędzia

* **Silnik gry:** Godot (wersja wspierająca LTS)
* **Język programowania:** C# / .NET
* **Zarządzanie kodem:** Git / GitHub
* **Podejście do kodu:** OOP (Programowanie Obiektowe), enkapsulacja logiki, separacja komponentów (Separation of Concerns).

---

## 🎮 Sterowanie

Rozgrywka opiera się na precyzji, do której wykorzystywane są klasyczne klawisze:
* `Poruszanie się` — Klawisze <kbd>A</kbd> / <kbd>D</kbd> lub <kbd>Strzałki lewo</kbd> / <kbd>prawo</kbd>
* `Skok` — Klawisz <kbd>Spacja</kbd> / <kbd>W</kbd>
* `Restart poziomu` — Automatyczny po skuszeniu lub dedykowany klawisz szybkiego restartu.

---

## 📦 Pobieranie i Uruchomienie (Dla Rekruterów)

Gra jest skompilowana i gotowa do przetestowania na systemie Windows. 

2. Pobierz najnowszą paczkę `.zip` (np. `Levels-v1.0.0-Windows.zip`).
3. Rozpakuj archiwum i uruchom plik `Levels.exe`.

*Alternatywnie możesz sklonować to repozytorium i otworzyć projekt bezpośrednio w Godot Editor.*

---

## 🗺️ Roadmap (Plany na Przyszłość)

Projekt jest stale rozwijany. W najbliższych wersjach planuję dodać:
- [ ] **Zaawansowany Level Design:** Dodanie ruchomych platform, stref ze zmienioną grawitacją oraz portali.
- [ ] **Audio System:** Implementacja dynamicznej ścieżki dźwiękowej reagującej na tempo gry.

---

## 👨‍💻 Autor

**Michał Wojewnik**
* Portfolio: [https://lontem2.github.io/index.html#]
* LinkedIn: [https://www.linkedin.com/in/michał-wojewnik-759baa35b/]
* E-mail: [wojewnikmichal@gmail.com]

---
*Projekt stworzony w celach naukowych i portfolio inżynieryjnego.*
