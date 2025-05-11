
---

## Opis Poszczególnych Elementów

- **data/**  
  Folder posiadający pliki Excel (w formacie CSV), które zawierają dane z tabel wygenerowanych przez phpMyAdmin (XAMPP) na potrzeby analizy. Dane te pochodzą z bazy MySQL i dotyczą informacji związanych z "droptime.mysql".

- **Part_1/**  
  Folder zawierający rozwiązanie części zadania oznaczonej jako **Part_1** pliku `Data Analyst Intern recruitment task.docx`. Znajdziesz tu odpowiedź odnoszącą się do pierwszej części zadania.
  - **Daniel_Szarek.csv**  
    Plik Excel (w formacie CSV) zawierający rezultat z query utworzonego w pliku `Part_1_query.sql`
  - **droptime.sql**  
    Plik SQL zawierający dane, które zostały wgrane do bazy danych MySQL. Ten plik stanowi źródło danych używanych podczas analizy.
  - **Part_1_query.sql**  
    Plik SQL zawierający query do zadania z Part_1

- **raports/**  
  Folder zawierający raporty przygotowane jako odpowiedzi na pozostałe części zadania:
  - **results/**  
    Folder, w którym zapisane są wykresy wygenerowane przez plik `Analiza_zadania.ipynb`. Znajdziesz tu m.in. histogram rzeczywistego czasu dostawy, histogram błędu predykcji, wykres średnich czasów dostawy wg sektorów, wykres planowanego czasu vs. błędu predykcji oraz inne wizualizacje pomocnicze.
  - **Daniel_Szarek_analysis.pdf**  
    Raport odpowiadający na **Part_2** pliku `Data Analyst Intern recruitment task.docx`. Plik ten to szczegółowa analiza danych, generacja wykresów oraz wnioski uzyskane na podstawie analizy przeprowadzonej w pliku `Analiza_zadania.ipynb`.
  - **Daniel_Szarek_research.pdf**  
    Raport odpowiadający na **Part_3** pliku `Data Analyst Intern recruitment task.docx`. Plik ten to dokumentacja procesu tworzenia i weryfikacji hipotez, proponowanych metod predykcyjnych oraz omówienie dodatkowych czynników wpływających na czas dostawy.

- **Analiza_zadania.ipynb**  
  Główny plik zadania (notebook Jupyter), w którym przetwarzane są dane z pliku `droptime.sql` oraz `data.csv`. W tym pliku wykonano całość analiz: od wstępnego czyszczenia danych, przez generowanie wykresów (które trafiają do katalogu `results`), po analizy korelacji i grupowania.

- **Data Analyst Intern recruitment task.docx**  
  Plik Word (w formacie docx) zawierający opis problemu i wytyczonych zadań, których rozwiązania znajdują się dalej w tym katalogu z rozwiązaniem zadania.

- **README.md**  
  Ten plik z dokumentacją realizacji zadania, opisu procesu analizy oraz z instrukcjami uruchomienia programów.

---

## Podsumowanie Rozwiązania

W ramach zadania przeprowadzono następujące kroki:

1. **Wczytanie i czyszczenie danych:**  
   Dane z różnych źródeł (CSV) zostały wczytane, a następnie oczyszczone z brakujących lub nieprawidłowych rekordów.

2. **Analiza i wizualizacja:**  
   Na podstawie przygotowanych danych wykonano szczegółową analizę, w tym wygenerowano wykresy przedstawiające rzeczywisty czas dostawy z dokładnością do jednej minuty, histogramy błędu predykcji oraz wizualizacje średnich czasów dostawy w zależności od sektora. Wyniki te wskazują na ogromną rozbieżność między planowanym a rzeczywistym czasem dostawy.

3. **Budowanie i weryfikacja hipotez:**  
   W raportach (**Daniel_Szarek_analysis.pdf, Daniel_Szarek_research.pdf**) opisano nasze założenia, metodologię oraz hipotezy dotyczące zmiany sposobu prognozowania czasu dostawy. Zaproponowano m.in. segmentację zamówień według sektora oraz zastosowanie bardziej zaawansowanych modeli predykcyjnych.

4. **Propozycje ulepszeń:**  
   Na podstawie analizy zaproponowano nowe podejścia do predykcji, uwzględniające dodatkowe zmienne (np. liczba produktów, waga zamówienia, godzina/dzień dostawy) oraz potencjalne proxy dotyczące typu budynku (którego bezpośrednich danych nie posiadamy).

---

## Instrukcje Uruchomienia

1. **Uruchomienie Analizy:**  
   Otwórz plik `Analiza_zadania.ipynb` w środowisku Jupyter Notebook lub Jupyter Lab. W notebooku znajdują się komórki kodu, które kolejno wczytują dane z plików z rozszerzeniem .csv, wykonują czyszczenie danych oraz generują wykresy.
   
2. **Przegląd Raportów:**  
   Raporty znajdują się w folderze `raports`:
   - **Daniel_Szarek_analysis.pdf** dla szczegółowej analizy danych (Part_2).
   - **Daniel_Szarek_research.pdf** dla dokumentacji hipotez oraz propozycji nowego podejścia (Part_3).

3. **Wyniki Wizualne:**  
   Wszystkie wykresy i wizualizacje są zapisywane w katalogu `results`. Możesz przejrzeć obrazy, aby zobaczyć graficzną reprezentację wyników analizy.

---