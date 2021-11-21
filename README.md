# NASA App - Funkční specifikace
## Verze 1

Roman Krof <br/>
krof.roman.2018@skola.ssps.cz <br/>
21. 11. 2021

* Úvod
  * Účel dokumentu
    * Dokument slouží k rychlému představení programu
  * Konvence dokumentu
    * Všechny kritické požadavky budou tučně
  * Ostatní dokumenty
    * https://api.nasa.gov/
* Scénáře
  * Všechny reálné způsoby použití
    * Uživatel se může kouknout na tělesa, která v minulosti prolétla okolo Země
    * Uživatel se můžou podívat na podrobnější detaily těchto těles
  * Typy uživatelských rolí, „personas“
    * Kdokoli, nikdo se nikam nepřihlašuje, všichni mají stejné možnosti využití
  * Vymezení rozsahu – co v programu **NEbude**
    * Program bude dostupný pouze v českém jazyce
  * Na co se **NEbude** klást důraz
    * Nebude se klást takový důraz na rychlost aktualizace informací
* Celková hrubá architektura
  * Pracovní tok
    * Uživatel zapne program
    * Pokud má k dispozici internetové připojení, aktualizuje seznam
    * Následně se zobrazí výpis asteroidů, které se přiblížily k Zemi
  * Všechny detaily: obrazovky, okna, tisky, chybové zprávy, logování
    * Program bude obsahovat hlavní okno, na kterém budou okna s lehce odlišnou barvou, ve kterých bude vepsán asteroid a jeho základní informace (datum přiblížení, průměr)
    * V horní části obrazovky bude vypsán čas poslední aktualizace a tlačítko "aktualizace", které seznam aktualizuje
    
    ![obrázek 1](https://github.com/RomanKrof/NASAAppFunspecs-Krof/blob/main/N%C3%A1vrh%20aplikace%20-%20hlavn%C3%AD%20strana.png)
    * Ve spodní části tohoto okénka bude tlačítko "podrobnosti" - po kliknutí se zobrazí podokno, které bude obsahovat podrobnější údaje asteroidu (datum přiblížení, rychlost, průměr, vzdálenost od Země)
    ![obrázek 2](https://github.com/RomanKrof/NASAAppFunspecs-Krof/blob/main/N%C3%A1vrh%20aplikace%20-%20podrobnosti.png)       
  * Dohodnuté principy
    * Data se budou vyposovat pomocí API od NASA
