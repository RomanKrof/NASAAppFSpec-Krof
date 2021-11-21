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
  * Pro koho je dokument určený
    * Pro širokou veřejnost např. pro lidi, které zajímá vesmír
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
    * Vybere si jednu ze záložek, které reprezentují typy schůzek - pracovní nebo soukromá
    * Uživatel přidá do vybraného seznamu schůzku
    * Uživatel přepne seznam a upraví dříve přidanou položku
    * Uživatel uloží změny a program vypne
  * Všechny detaily: obrazovky, okna, tisky, chybové zprávy, logování
    * Hlavní okno, které v levé části obrazovky bude zobrazovat list schůzek s vybranou záložkou (2 - pracovní a soukromé schůzky), ve spodní části bude tlačitko k přidání, v pravé části budou vypsány všechny podrobnosti dané schůzky, v pravém spodním rohu části s podrobnostmi bude tlačítko, které uloží všechny úpravy, v levém spodním rohu části s podrobnostmi bude tlačítko na úpravu vybrané schůzky
    ![obrázek 1](https://github.com/RomanKrof/UzitecnySoftwareNavrh/blob/main/N%C3%A1vrh%20hlavn%C3%ADho%20okna.png "Obrázek 1")
    * Při kliknutí na tlačítko úpravy se vyvolá menší podokno, ve kterém budou vypsány podrobnosti, které se budou moci přepsat, ve spodní části tohoto podokna bude tlačítko pro uložení změn schůzky, při chybném zadání informací se u dané informace objeví červeně zbarvený text s chybovou hláškou
    
    ![obrázek 2](https://github.com/RomanKrof/UzitecnySoftwareNavrh/blob/main/N%C3%A1vrh%20upravovac%C3%ADho%20a%20p%C5%99id%C3%A1vac%C3%ADho%20okna.png "Obrázek 2")
  * Dohodnuté principy
    * Data se budou vyposovat pomocí API od NASA
