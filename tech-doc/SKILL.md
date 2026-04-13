---
name: tech-doc
description: |
  Skill pro psaní kvalitní technické dokumentace k softwarovým projektům (uživatelské příručky, administrátorské příručky, vývojářské příručky, popisy datových formátů). Použij tento skill kdykoli uživatel chce psát dokumentaci, vytvořit manuál, napsat návod, popsat API, vytvořit příručku, napsat nápovědu, nebo strukturovat technický text. Použij ho i když uživatel jen zmiňuje „docs", „dokumentace", „readme s návodem", „help text", „how-to", „guide" nebo „příručka". Skill pokrývá kompletní proces: strukturu dokumentu, styl psaní, formulaci nadpisů, psaní postupů, varování, terminologii i typografii pro elektronické dokumenty.
---

# Technická dokumentace k softwarovým projektům

Tento skill tě provede tvorbou kvalitní technické dokumentace. Všechny principy vycházejí z osvědčených postupů profesionální technické komunikace a jsou zaměřené na elektronickou dokumentaci (web, nápověda, wiki, Markdown, HTML).

## Základní principy psaní

### KISS — Keep It Short and Simple

Piš krátce a jednoduše. Čtenář dokumentace nehledá literární zážitek — chce rychle najít odpověď a vrátit se k práci. Každé slovo musí nést informaci. Pokud ho můžeš odstranit bez ztráty významu, odstraň ho.

### Piš pro čtenáře, ne pro sebe

Nepiš, abys ukázal, co všechno víš. Piš to, co čtenář potřebuje vědět. Představ si konkrétního uživatele — jakou má roli, co chce udělat, co už ví a co ne.

### Začni tím nejdůležitějším

Nejdůležitější informaci dej na začátek — sekce, odstavce i věty. Čtenáři skenují text a často čtou jen první větu. Pokud je klíčová informace schovaná uprostřed odstavce, nenajdou ji.

### Buď konkrétní

Vyhni se vágním formulacím. Místo „systém může zpracovat velké množství dat" napiš „systém zpracuje až 10 000 záznamů za sekundu". Konkrétní čísla, názvy a příklady budují důvěru a jsou užitečnější.

### Buď stručný — odstraň prázdné kalorie

Každé slovo, které nepřidává informaci, je prázdná kalorie. Odstraň výplňová slova, redundantní přívlastky a zbytečné věty. Porovnej:
- Špatně: „V podstatě je důležité zmínit, že uživatel by měl vzít v úvahu možnost restartování služby."
- Dobře: „Restartujte službu."

### Buď konzistentní

Konzistence se týká tří věcí:
1. **Terminologie** — jeden pojem = jedno slovo. Nepoužívej střídavě „uživatel", „operátor" a „administrátor" pro tutéž osobu.
2. **Formátování** — stejné typy informací formátuj stejně v celém dokumentu.
3. **Struktura** — stejné typy sekcí mají stejnou vnitřní strukturu (např. každý popis funkce: úvod → postup → příklad).

---

## Styl psaní

### Slovesný čas a způsob

- Používej **přítomný čas**: „Aplikace zobrazí dialog" (ne „zobrazila" nebo „zobrazí se").
- Používej **rozkazovací způsob** v postupech: „Klikněte na Uložit" (ne „Uživatel klikne").
- Používej **činný rod**: „Systém uloží soubor" (ne „Soubor je uložen systémem").

### Oslovení čtenáře

Mluv přímo ke čtenáři — používej „vy" (vykání). Netvoř vzdálenost obraty jako „uživatel provede" — místo toho napiš „proveďte". Čtenář je ten, kdo text čte, a text je pro něj.

### Neříkej „prosím"

V technické dokumentaci nepoužívej „prosím". Dokumentace je instrukce, ne žádost. „Klikněte na Uložit" je správně, „Prosím klikněte na Uložit" je špatně — působí to neprofesionálně a prodlužuje text.

### Neříkej „nyní"

Slovo „nyní" je v postupech zbytečné. Kroky následují přirozeně za sebou, takže „nyní klikněte" je redundantní — stačí „klikněte".

### Slova, kterým se vyhni

Tato slova signalizují vágnost, nerozhodnost nebo lenost. Nahraď je konkrétním vyjádřením nebo je odstraň:

| Slovo | Problém | Řešení |
|-------|---------|--------|
| a tak dále, atd., apod. | Čtenář neví, co ještě patří do výčtu | Vypiš vše, nebo napiš „například X, Y a Z" |
| a/nebo | Nejednoznačné — je to „a", nebo „nebo"? | Rozhodni se: buď „a", nebo „nebo", případně formuluj jinak |
| může, mohlo by | Nejasné — je to schopnost, nebo možnost? | Nahraď: „umožňuje", „dokáže", nebo podmínkou „pokud…, pak…" |
| mělo by | Tak má, nebo nemá? | Napiš jednoznačně: „musí" nebo přeformuluj |
| odpovídající | Vágní — odpovídající čemu? | Napiš konkrétně, čemu to odpovídá |
| objekt | Příliš obecné | Pojmenuj konkrétně: „soubor", „záznam", „prvek" |
| některý, nějaký | Neurčité | Buď konkretizuj, nebo odstraň |
| docela, poměrně, raději | Subjektivní výplň | Odstraň nebo nahraď měřitelným údajem |

---

## Nadpisy

Nadpisy jsou nejdůležitější navigační prvek dokumentace. Čtenář podle nich skenuje obsah a rozhoduje se, co bude číst. Špatný nadpis = čtenář informaci nenajde, i když v dokumentu je.

### Pravidla pro nadpisy

1. **Nadpis musí přesně vystihovat obsah sekce.** Pokud sekce popisuje konfiguraci databáze, nadpis je „Konfigurace databáze", ne „Nastavení" nebo „Databáze".

2. **Nadpis musí dávat smysl i sám o sobě.** Čtenář často vidí nadpis v obsahu nebo ve výsledcích hledání bez okolního kontextu. Pokud nadpis sám o sobě nic neříká, je špatný.

3. **Formuluj nadpisy z pohledu uživatele.** Uživatel přemýšlí v úkolech a cílech, ne ve vlastnostech systému. Nadpis by měl „lovit pozornost" — ukazovat přínos, ne jen popisovat funkci.
   - Špatně: „Funkce exportu"
   - Dobře: „Export dat do CSV"
   - Benefit: „Úspora času díky dávkovému exportu"

4. **Snaž se dostat do nadpisu sloveso nebo název činnosti.** Nadpisy se slovesem lépe komunikují, co čtenář v sekci najde.
   - Špatně: „Databáze - Nastavení"
   - Dobře: „Nastavení databáze"

5. **Vyhni se začátkům jako „Používání…", „Práce s…", „Informace o…"** Tyto začátky nenesou informaci a odsouvají skutečný obsah nadpisu dozadu. Porovnej:
   - Špatně: „Používání kontroly pravopisu"
   - Dobře (koncept): „Jak funguje kontrola pravopisu"
   - Dobře (úkol): „Kontrola pravopisu v rozepsaném dokumentu"

6. **Odstraň víceznačnost.** Nadpis „Tisk" může znamenat „Jak tisknout", „Nastavení tiskárny" nebo „Řešení problémů s tiskem". Buď konkrétní.

7. **Používej jednotné číslo.** Uživatel pracuje na jednom úkolu v jednu chvíli. Jednotné číslo je konkrétnější a bližší jeho situaci.
   - Špatně: „Vytváření nových dokumentů"
   - Dobře: „Vytvoření nového dokumentu"

8. **Nadpisy na vyšších úrovních by měly být krátké.** Dlouhé nadpisy ztěžují skenování obsahu. Na nižších úrovních hierarchie mohou být nadpisy delší, protože jsou specializovanější.

9. **Nadpisy na stejné úrovni musí mít paralelní strukturu.** Pokud jeden nadpis začíná podstatným jménem, všechny na téže úrovni by měly začínat podstatným jménem. Pokud jeden začíná slovesem, všechny by měly začínat slovesem.
   - Špatně: „Instalace" / „Jak konfigurovat systém" / „Údržba"
   - Dobře: „Instalace" / „Konfigurace" / „Údržba"
   - Nebo: „Instalace systému" / „Konfigurace systému" / „Údržba systému"

---

## Postupy (instrukce krok za krokem)

Postupy jsou jádrem uživatelské dokumentace. Čtenář je následuje, aby splnil konkrétní úkol.

### Struktura postupu

```
[Úvodní věta vysvětlující účel postupu:]

Předpoklady (pokud existují):
- Předpoklad 1
- Předpoklad 2

1. První krok.
2. Druhý krok.
   Systém zobrazí potvrzovací dialog.
3. Třetí krok.

Výsledek: [Co se stane po dokončení postupu.]
```

### Pravidla pro postupy

1. **Začni úvodní větou s dvojtečkou.** Úvodní věta říká, k čemu postup slouží, a končí dvojtečkou, která uvozuje seznam kroků: „Vytvoření nového uživatelského účtu:"

2. **Maximálně 10 kroků.** Pokud postup přesáhne 10 kroků, rozděl ho na dílčí postupy. Dlouhé postupy odrazují čtenáře a zvyšují riziko chyby.

3. **Jeden krok = jedna akce.** Neslučuj více akcí do jednoho kroku. „Klikněte na Soubor a vyberte Uložit jako" jsou dva kroky, ne jeden (výjimka: triviální navigační sekvence jako „Soubor → Uložit").

4. **Používej rozkazovací způsob.** „Klikněte", „Zadejte", „Vyberte" — ne „Uživatel klikne" nebo „Je třeba kliknout".

5. **Předpoklady patří před krok 1.** Vše, co musí být splněno před zahájením postupu (přihlášení, nainstalovaný software, oprávnění), uveď před prvním krokem, ne uprostřed postupu.

6. **Zachovej chronologický pořád.** Kroky musí jít v přesném pořadí, v jakém je uživatel provádí.

7. **Vysvětli proč** (pokud to není zřejmé). Pokud krok vyžaduje neobvyklou akci, krátce vysvětli důvod: „Restartujte službu, aby se změny konfigurace projevily."

8. **Popiš, co uživatel uvidí.** Po klíčových krocích popiš očekávaný výsledek: „Systém zobrazí potvrzení o úspěšném uložení." Čtenář tak ví, že je na správné cestě.

9. **Větvení řeš odrážkovým podseznamem.** Pokud se postup liší podle situace:
   ```
   3. Vyberte typ exportu:
      - **CSV** — pro tabulková data
      - **JSON** — pro strojové zpracování
      - **PDF** — pro tiskové výstupy
   ```

10. **Podmínku dej na začátek věty.** „Pokud používáte Linux, spusťte příkaz…" — ne „Spusťte příkaz…, pokud používáte Linux." Čtenář na Windows musí vědět hned, že ho krok netýká, aby ho neprováděl zbytečně.

11. **Vynechej odkazy mezi kroky.** Slova jako „potom", „příští", „dále", „následně" jsou zbytečná — kroky jsou číslované, pořadí je zřejmé. Tyto spojky jen prodlužují text.

12. **Nekombinuj alternativní metody do kroků.** Pokud existuje klávesová zkratka nebo alternativní cesta, neuváděj ji v kroku. Přidej samostatnou sekci (např. „Klávesové zkratky"). Stručnost v postupu je vždy výhoda.

13. **Popisuj věci v pořadí, jak nastanou.** Vyhni se větám typu „Udělejte X, potom co jste udělali Y." Čtenář musí vědět, co má udělat, *předtím* než to udělá.
    - Špatně: „Stiskněte Uložit v okně Možnosti."
    - Dobře: „V okně Možnosti stiskněte Uložit."

### Scénáře

Pro popis interakcí více rolí nebo systémů použij tabulkový scénář. Definuj role jako sloupce a činnosti jako řádky v chronologickém pořadí — podobně jako technický scénář filmu.

### Seznamy

- Položky seznamu musí být **stručné a vyvážené** (přibližně stejně dlouhé).
- Dodržuj paralelní strukturu — všechny položky začínají stejným slovním druhem.
- Pokud je seznam součástí věty (úvodní fráze + dvojtečka + položky), dodržuj interpunkci: položky odděluj čárkami a poslední ukonči tečkou. Pokud jsou položky celými větami, každá začíná velkým písmenem a končí tečkou.

---

## Struktura dokumentu

### Typy softwarové dokumentace

Rozhodni, jaký typ dokumentu píšeš, protože každý má jinou strukturu a cílovou skupinu:

- **Uživatelská příručka** — pro koncové uživatele. Struktura podle úkolů a cílů uživatele.
- **Administrátorská příručka** — pro správce systému. Instalace, konfigurace, údržba, řešení problémů.
- **Vývojářská příručka / dokumentace API** — pro vývojáře. Architektura, API reference, příklady integrace.
- **Popis datových formátů** — pro vývojáře a integrátory. Struktura dat, validace, příklady.

### Typy struktur

Zvol typ struktury podle povahy dokumentu:

- **Uživatelsky řízená struktura** (preferovaná) — organizuj podle uživatelských skupin, úrovně zkušeností, scénářů použití, cílů a potřeb uživatele. Reaguj na to, co uživatel chce dosáhnout, ne na to, jak je produkt vnitřně uspořádaný.
- **Časově řízená struktura** — chronologické pořadí procesů nebo kroků, které uživatel musí vykonat. Vhodná pro tutoriály a průvodce prvním použitím.
- **Tématicky řízená struktura** — téma má vlastní přirozenou hierarchii (např. síťová architektura → podsítě → uzly). Vhodná pro referenční dokumentaci.
- **Produktem řízená struktura** — popis vlastností podle struktury produktu (menu, dialogy). Téměř vždy nejméně vhodná, protože neodpovídá tomu, jak uživatel přemýšlí.
- **Abecední/číselné řazení** — pouze pro rejstříky, glosáře a referenční tabulky.

### Principy strukturování

1. **Strukturuj podle uživatele, ne podle produktu.** Neopisuj menu položku po položce. Místo toho organizuj obsah podle toho, co uživatel chce dosáhnout.
   - Špatně: „Menu Soubor" → „Menu Úpravy" → „Menu Nástroje"
   - Dobře: „Vytvoření projektu" → „Import dat" → „Export a sdílení"

2. **Od jednoduchého ke složitému.** Začni nejdůležitějším. Nejprve to, co je důležité pro všechny. Snadné před obtížným. Časté problémy dříve než náhodné.

3. **Koncepty → Postupy → Reference.** V rámci každého tématu nejdřív vysvětli pojmy (co to je a proč), pak dej návod (jak to udělat), a nakonec referenční informace (kompletní výčet parametrů, tabulky hodnot).

4. **Segmentuj podle cílové skupiny.** Pokud dokument slouží více skupinám (uživatel, admin, vývojář), jasně odděluj sekce určené různým skupinám. V elektronické dokumentaci používej oddělené stránky nebo sekce. Uživatelsky řízená struktura odráží: uživatelské skupiny, zkušenosti uživatelů, scénáře případů užití, fáze užití, uživatelské cíle a potřeby.

5. **Používej vrstvení (progressive disclosure).** V elektronické dokumentaci skrývej pokročilé detaily do rozbalovacích sekcí, tabů nebo odkazů. Základní informace je vidět hned, detaily si čtenář rozbalí, když je potřebuje. Kritéria pro vrstvení:
   - **Důležitost** — nutné vs. doplňující informace
   - **Typ informace** — koncept, postup, reference
   - **Cílová skupina** — začátečník, středně pokročilý, pokročilý

6. **Rozděluj příliš dlouhý obsah.** Dlouhý manuál rozděl na kratší manuály. Dlouhou sekci na kratší sekce. Dlouhé téma na kratší témata. Dlouhý odstavec na kratší odstavce. Dlouhou větu na kratší věty. Na nejnižší úrovni platí pravidlo „jedna obrazovka" — čtenář by neměl muset příliš scrollovat v rámci jednoho tématu.

7. **Křížové odkazy používej střídmě.** Odkaz na jinou sekci je užitečný, ale příliš mnoho odkazů rozbíjí čtení. Odkazuj jen na skutečně související obsah, ne na vše, co by mohlo být relevantní. Odkazy by měly být stabilní — použij trvalé identifikátory, ne pozice v dokumentu.

---

## Varování a upozornění

V softwarové dokumentaci se varování používají při riziku ztráty dat, bezpečnostních problémech nebo nevratných operacích.

### Úrovně

| Úroveň | Kdy použít | Příklad |
|---------|-----------|---------|
| **Upozornění** (Note/Caution) | Riziko ztráty dat, chybné konfigurace, nežádoucího chování | „Změna tohoto nastavení vymaže všechna lokální data." |
| **Varování** (Warning) | Bezpečnostní riziko, nevratná operace s vážnými důsledky | „Smazání databáze je nevratné. Před smazáním vytvořte zálohu." |
| **Nebezpečí** (Danger) | Kritické bezpečnostní riziko, potenciální únik dat, zničení systému | „Nikdy neukládejte API klíče do veřejného repozitáře." |

### Pravidla pro varování

1. **Varování patří PŘED akci, ne za ni.** Čtenář musí varování vidět dříve, než provede krok, který může způsobit problém.

2. **Buď stručný.** Varování musí být krátké a jasné. Dlouhé varování nikdo nečte.

3. **Nejdřív popiš nebezpečí, pak instrukci.**
   - Špatně: „Klikněte na Smazat. Pozor, tato akce je nevratná."
   - Dobře: „**Varování:** Smazání je nevratné. Před kliknutím na Smazat vytvořte zálohu."

4. **Používej činný rod.** „Tato akce smaže všechna data" (ne „Všechna data budou smazána").

5. **Nenadužívej varování.** Pokud je všechno varování, nic není varování. Používej je jen tam, kde je reálné riziko.

### Formátování v Markdownu

```markdown
> **Upozornění:** Změna portu vyžaduje restart služby.

> **Varování:** Smazání uživatele odstraní všechna jeho data. Tuto akci nelze vrátit.

> **Nebezpečí:** Nikdy nespouštějte tento příkaz v produkčním prostředí bez předchozí zálohy databáze.
```

---

## Terminologie

### Správa terminologie

Pro každý projekt udržuj seznam termínů. Tabulka terminologie obsahuje:

| Správný termín | Nepoužívat | Poznámka |
|----------------|-----------|----------|
| uživatel | user, klient, zákazník | V kontextu dokumentace pro koncové uživatele |
| repozitář | repo, repository | „Repozitář" v prvním výskytu, dále lze zkrátit |
| nasadit (deploy) | deployovat, nahrát | Sloveso „nasadit" nebo „nasazení" jako podst. jm. |

### Pravidla

1. **Jeden pojem = jedno slovo.** Jakmile zvolíš termín, používej ho konzistentně v celém dokumentu.
2. **Definuj termín při prvním výskytu.** Pokud používáš odborný pojem, vysvětli ho při prvním použití nebo v glosáři.
3. **České vs. anglické termíny.** Preferuj zavedené české termíny. Pokud český ekvivalent neexistuje nebo je nezvyklý, použij anglický termín a při prvním výskytu vysvětli.
4. **Zkratky rozepíš při prvním použití.** „CI/CD (Continuous Integration / Continuous Deployment)" — pak už jen „CI/CD".

---

## Psaní sekcí a odstavců

1. **Každá sekce má jeden hlavní téma.** Nemíchej nesouvisející témata do jedné sekce.
2. **Každý odstavec rozvíjí jednu myšlenku.** Nová myšlenka = nový odstavec.
3. **Odstavec má 2–5 řádků.** Příliš dlouhé odstavce jsou nepřehledné a odrazují od čtení.
4. **První věta odstavce shrnuje jeho obsah.** Čtenář skenující text přečte jen první věty — musí z nich pochopit hlavní sdělení.
5. **Každá sekce má popisný nadpis.** Sekce bez nadpisu je jako kniha bez obálky — čtenář neví, co v ní najde.

---

## Paralelismus

Paralelismus znamená, že stejné typy prvků mají stejnou gramatickou strukturu. Zlepšuje čitelnost a profesionalitu textu.

### Kde uplatňovat paralelismus

- **Nadpisy na stejné úrovni:** Všechny začínají stejným slovním druhem.
  - Dobře: „Instalace systému" / „Konfigurace systému" / „Aktualizace systému"
  - Špatně: „Instalace" / „Jak konfigurovat" / „Aktualizujte systém"

- **Položky seznamu:** Všechny mají stejnou strukturu.
  - Dobře: „Otevřete soubor" / „Upravte hodnotu" / „Uložte změny"
  - Špatně: „Otevřete soubor" / „Hodnota se upraví" / „Uložení změn"

- **Kroky postupu:** Všechny začínají slovesem v rozkazovacím způsobu.

- **Věty ve výčtu:** Pokud jedna položka začíná slovesem, všechny začínají slovesem. Pokud jedna je větou, všechny jsou větami.

---

## Typografie pro elektronické dokumenty

- **Tučné písmo** — pro zvýraznění důležitých pojmů, prvků UI (názvy tlačítek, položky menu), klíčových slov. Používej střídmě — pokud je tučné všechno, nic nevyniká.
- **Kurzíva** — pro názvy, nové termíny při prvním výskytu, tituly. Používej ještě střídměji než tučné.
- **Podtržení** — POUZE pro odkazy (linky). V elektronickém textu podtržení = odkaz, jiné použití mate čtenáře.
- **Kódové formátování** (`monospace`) — pro příkazy, názvy souborů, proměnné, výstupy konzole, fragmenty kódu.
- **Nekombinuj efekty.** Nepoužívej tučnou kurzívu ani tučné podtržení. Jeden efekt na jednom místě stačí.

---

## Struktura typického softwarového dokumentu

Při vytváření kompletní dokumentace k softwaru použij tuto orientační strukturu a přizpůsob ji konkrétnímu projektu:

```
1. Úvod
   - Co software dělá (stručně, 2-3 věty)
   - Pro koho je určen
   - Požadavky (systémové, softwarové)

2. Začínáme (Getting Started)
   - Instalace / nastavení
   - První spuštění
   - Základní pracovní postup (quick start)

3. Hlavní funkce (organizované podle uživatelských úkolů)
   - Úkol/cíl A
     - Koncept (co a proč)
     - Postup (jak)
     - Příklady
   - Úkol/cíl B
     - ...

4. Pokročilé použití
   - Konfigurace
   - Automatizace
   - Integrace s dalšími nástroji

5. Řešení problémů (Troubleshooting)
   - Časté chyby a jejich řešení
   - FAQ

6. Reference
   - Kompletní přehled příkazů / API
   - Konfigurační parametry
   - Glosář
```

---

## Kontrolní seznam před odevzdáním

Než považuješ dokumentaci za hotovou, zkontroluj:

- [ ] Nadpisy přesně popisují obsah svých sekcí a dávají smysl i bez kontextu
- [ ] Nadpisy na stejné úrovni mají paralelní strukturu
- [ ] Nadpisy jsou v jednotném čísle
- [ ] Nadpisy na vyšších úrovních jsou krátké
- [ ] Postupy mají max. 10 kroků, každý krok = jedna akce
- [ ] Předpoklady jsou uvedeny před prvním krokem
- [ ] Kroky neobsahují odkazy mezi sebou (potom, dále, následně)
- [ ] Alternativní metody jsou v samostatných sekcích, ne v krocích
- [ ] Varování jsou umístěna PŘED krokem, kterého se týkají
- [ ] Terminologie je konzistentní v celém dokumentu
- [ ] Neobsahuje zakázaná slova (atd., a/nebo, může, mělo by…)
- [ ] Text je v činném rodě a přítomném čase
- [ ] Oslovuje čtenáře přímo (vykání, rozkazovací způsob)
- [ ] Neobsahuje „prosím" ani „nyní"
- [ ] Odstavce mají 2–5 řádků
- [ ] Formátování je konzistentní (tučné, kurzíva, kód)
- [ ] Struktura je orientovaná na uživatele, ne na produkt
- [ ] Dlouhé sekce jsou rozděleny na kratší
