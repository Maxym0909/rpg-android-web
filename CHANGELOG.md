# Gra RPG Dungeon - Historia Aktualizacji i Opis Projektu

## O Grze (Opis Projektu)
**RPG Dungeon** to wciągająca, przeglądarkowa gra typu RPG (Role-Playing Game) z elementami strategii i dungeon-crawlera, zbudowana całkowicie w oparciu o technologie webowe (HTML/JS/CSS). Projekt został stworzony w architekturze "Single-File", co sprawia, że jest niezwykle lekki i doskonale nadaje się do wstrzyknięcia w aplikację na systemy Android (jako WebView).

Gracz wciela się w jedną z trzech klas postaci (Ciężko uzbrojony Wojownik, Zwinny Łucznik lub Posługujący się magią Mag) i wyrusza do proceduralnie generowanych, mrocznych podziemi.

**Najważniejsze elementy rozgrywki:**
1. **Eksploracja Lochów:** Gracz porusza się po siatce za pomocą wirtualnego D-Pada. Na mapie działa "Mgła Wojny" (Fog of War) – nieodkryte terytoria są czarne, a każdy krok odsłania nieznane niebezpieczeństwa, skrzynie pełne skarbów, wędrownych kupców lub schody na jeszcze trudniejsze poziomy.
2. **Turowa Walka Taktyczna:** Kiedy gracz wejdzie na pole z potworem, przenosi się na ekran bitwy. Walki są turowe i opierają się na zarządzaniu Zdrowiem (HP) i Maną (MP). Gracz może używać ataków fizycznych, postawy obronnej, czy specjalnych umiejętności obszarowych (AoE) dopasowanych do swojej klasy. Całość wieńczą animacje lecących pocisków i obrażeń.
3. **Progresja Postaci:** Za walkę zdobywa się punkty EXP. Po osiągnięciu odpowiedniego progu, postać awansuje na nowy level, jej statystyki wzrastają, a gracz otrzymuje Punkty Umiejętności (SP) do wydania w Księdze Umiejętności. Można również podnosić zdobyty sprzęt i wymieniać go w ekwipunku, by zwiększać bazowy Atak i Obronę.
4. **Rozbudowa Wioski (Baza Wypadowa):** Po przegranej bitwie lub udanym rajdzie wraca się do wioski. Za zarobione złoto gracz może stawiać i ulepszać budynki (Tartak, Kopalnia, Koszary), które generują pasywny przychód surowców, a także kupować cenne mikstury i odblokowywać nowe czary.
5. **Retro Audio System:** Gra nie korzysta z ciężkich plików MP3. Wszystkie utwory muzyczne (jak klimatyczny motyw przewodni) oraz dźwięki uderzeń miecza czy leczenia są matematycznie generowane w locie przy użyciu oscylatorów z Web Audio API.

---

## Najnowsze Poprawki: Wizualizacje Pocisków i Zmysł Słuchu
- **Wizualne Pociski w Walce:** Wprowadzono dynamiczne animacje rzucania czarów i ataków. Od teraz po kliknięciu "Atak" z gracza w stronę wroga wylatuje miecz, strzała lub kula ognia (w zależności od klasy). W przypadku rzucania czarów AoE, pociski lecą we wszystkich wrogów naraz!
- **Dedykowane Dźwięki Zdolności:** Zastąpiono domyślny odgłos magii unikalnymi tonami dla każdej postaci. Ataki fizyczne brzmią teraz ostrzej, a picie potki brzmi jak charakterystyczne bulgotanie fiolki.

## Dzisiejsze Zmiany (Poprzednia Sesja)
- **Ekran Zwycięstwa:** Naprawiono błąd z brakiem opcji kontynuowania gry po wyczyszczeniu lochów ze wszystkich wrogów. Wyświetlają się poprawne przyciski powrotu do wioski z łupami lub zejścia na niższy poziom lochu.
- **Zbalansowanie Many (MP):** Dodano zapasy many startowej dla każdej klasy (Mag - 120, Łucznik - 70, Wojownik - 50). Umiejętności poprawnie zabierają MP, blokując spamowanie superatakami bez odnawiania many.
- **Nerf Szamana:** Zmniejszono szansę na leczenie rannych sojuszników przez wrogiego Orka Szamana z każdorazowych 100% do zbalansowanych 40%.
- **Ulepszenia Audiowizualne (Tło):**
  - Odtwarzanie proceduralnej 8-bitowej muzyki w tle po wejściu do gry.
  - Odgłosy powolnych kroków przy chodzeniu postaci po kratkach.
  - Dźwięk alarmujący przed ekranem przejścia do bezpośredniego starcia.
  - Płynny, przyciemniony ekran podczas "powrotu do Wioski".

## Kamienie Milowe Projektu
- **Mgła Wojny (Fog of War) i Skalowanie:** Mapa reaguje na pozycję gracza zasłaniając odległe kafelki. Wraz ze schodzeniem w dół podziemi, wymiary z generowanych pokoi powiększają się z 7x7 aż do epickich 15x15 pól.
- **System Umiejętności (SP):** System poziomów napędzający fioletowy, interaktywny pasek EXP. Każdy awans pozwala na modyfikowanie swojego zestawu ruchów w "Księdze Zdolności".
- **Ataki Obszarowe (AoE):** Przebudowana logika walki potrafiąca na ułamek sekundy zamrozić planszę i w tym samym momencie obrać za cel wszystkich potworów stojących do walki (wraz ze zliczaniem sumy zadanych uderzeń).
- **Całkowita Fuzja (Single-File):** Kod gry został ostatecznie scentralizowany i napisany tak, aby bez problemu funkcjonował offline i skalował się responsywnie pod mobilne dotykowe panele użytkowników.
