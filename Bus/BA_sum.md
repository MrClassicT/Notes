# Inhoud
|Hoofdstuk|Samengevat  |Gekend         |
|---|---|---|
|[Eliciteren](#Eliciteren) |📘 [X] |🧠 [ ] |
|[Documenteren](#Documenteren) |📘 [X] |🧠 [ ]|
|- [[#User stories ontdekken\|User story spel]] |📘 [X] |🧠 [ ]|
|[Valideren](#Valideren) |📘 [X] |🧠 [ ]|
|[Managen](#Managen) |📘 [X] |🧠 [ ]|
|[Processen](#Processen) |📘 [X] |🧠 [ ]|
|[BPMN](#BPMN) |📘 [X] |🧠 [ ]|
|- [Theorie slides](#Theorie-slides) |📘 [X] |🧠 [ ]|
|- [Presentaties](#Presentaties) |📘 [🤌] |🧠 [ ]|
|[Workshop: Refleqt](#Workshop-Refleqt) |📘 [X] |🧠 [ ]|

---
# Eliciteren
> "Eliciteren betekent informatie, reacties of emoties doelgericht opwekken of verkrijgen, vaak door gerichte vragen of handelingen."

## Processen ontdekken
- Opzetten project => Samenstellen team
- Informatie verzamelen => Proces goed leren begrijpen. Dit adhv ElicitatieTechnieken.
- Begeleiden modelleertaak => Procesmodel maken adhv modelleermethode
- Kwaliteitsborging => Procesmodellen beantwoorden aan de voorgestelde kwaliteitescriteria. Dit helpt vertrouwen te creëren voor alle stakeholders.

### Uitdagingen
- Gefragmenteerde kennis. Niet iedereen kent alles over het gehele proces.
- Experten denken op "instance"-niveau => Proces-instance = unieke passage doorheen een proces voor 1 bepaalde unit(artikel, reis, ...)
- Kennis over procesmodellering is zeldzaam => Als analyst kun je vaak niet vragen of het diagram correct is gezien ze het meestal niet zullen begrijpen.

## Expertise procesanalysten
- Problemen begrijpen
	- Kennis van probleemdomein.
	- Kennis van de organisatie om probleem te structureren.
- Problemen oplossen
	- Identificatie van de procestriggers.
	- Hypothese-beheer.
	- Top-down strategie.
- Modelleerskills
	- Goed gestructureerd en met duidelijke layout.
	- Systematische labels.
	- Expliciete start- en eindpunten.
	- Gepaste granulariteit en decompositie
		- Granulariteit: Kiezen van het juiste niveau van details.
		- Decompositie: Proces opsplitsen indien nodig naar subtasks.

## Elicitatietechnieken
![[BA_Elicitatietechnieken.png]]
### Creatieve technieken
- **Brainstormen**: 
	- **Nadelen**: Ervaren moderator nodig en sommige deelnemers zullen dominanter zijn dan andere.
	- **Alternatieven**: Brainwriting ([6-3-5 methode](https://www.youtube.com/watch?v=TR1i1PPd8ZU)) en de 
	  [GPS-methode](https://www.youtube.com/watch?v=dfU4mBgUokg) => Vorm van brainstormen waar er geen dominantie zou mogen plaatsvinden.
- **Invalshoek veranderen**: 
	- 6 denkhoeden, elke hoed heeft een bepaalde visie om een probleem op te lossen.
- **Analogie**:
	- Analogie = We gaan zaken gelijkstellen aan elkaar om ze zo beter te kunnen begrijpen.
	- Analogieën stimuleren creativiteit.
	- **bvb**. "Het brein is als een computer, met het geheugen als de harde schijf en gedachten als de software."

### Uitvraagtechnieken
- **Interview**:
	- **Succesvol interview** => Voorbereid en met ervaring, met de juiste persoon, bereidheid interviewee, verstandhouding opbouwen.
	- **Uitdagingen**:
		- Moeilijke vaardigheid om goed te beheersen.
		- Resultaat kan fout geïnterpreteerd worden.
		- Soms is er al dan niet bewuste achterhouding van info.
	- [[BA_Interview-right-person.png|Interview de juiste persoon.]]![[BA_Interview-right-person.png]]
	- Interview **plan**:
		- Datum, plaats, project, interviewee, rol van deze persoon, reden interview, hoofdvragen
			- vragen: 3 tot 5 open hoofdvragen in combinatie met gesloten vragen.
				- Let op voor manipulatieve vragen
			- Open vragen
				- Opletten dat men bij de kern van de vraag blijft.
			- Gesloten vragen
				- Enkel ter verduidelijking.
	- Uitvoering:
		- Ban opbouwen, verwachtingen stellen, juiste vragen stellen op correcte manier, actief luisteren, notuleren en afsluiten interview.
		- Zoek wat nodig is, niet enkel wat er gewenst is.
	- Follow-up:
		- Formele bedanking, nota's review, acties opstellen.
- **Enquête**:
	- Fysiek of digitale vragenlijst.
	- Deelnemers kunnen vragen verkeerd interpreteren en je mist body-language => non verbale communicatie.

### Observatietechnieken
- Veldobservatie:
	- Gebruiker werkt in bijzijn van een analist.
		- Gebruiker legt uit wat hij doet, zonder interactie analyst.
- Werkstage:
	- Analist voert zelf het werk uit.
		- Tijdrovend maar levert diepgaande kennis op.

### Documentatie-georiënteerde technieken
- **Systeemarcheologie**: Studie van bestaande systemen om hun structuur en werking te begrijpen.
- Lezen vanuit specifiek oogpunt
- Hergebruik van requirements: kunnen tijd en kosten voor analyse sterk reduceren. Gebruik voorgaande analyses.

### Ondersteunende technieken
- **Workshop**: samenbrengen van alle key-stakeholders, discussie om een gedeeld begrip te creëren, vaak ondersteund door software en het resulterende model dient als referentie voor verdere discussies.
- **CRC-kaarten**: Class Responsability Collaboration (workshop)
	- Belangrijke business objecten worden op kaarten geschreven
	- Deelnemers voegen eigenschappen hieraan toe.
	- Gebruikt om processen en requirements in kaart te brengen.
- **Video/audio opname**:
	- Evt nadeel: deelnemers kunnen zich anders gaan gedragen.
- **Use cases en user stories**:  
	- 1 persoon, 1 moment, 1 plaats
	- Maken deel uit van een groter geheel
	- helpen elicitatieproces te structureren.

## Techniekkeuze
Elke techniek heeft zijn voor- en nadelen. Combinatie van technieken is nodig. Tijdens maken keuze rekening houden met: Menselijke -, organisatorische - en vakinhoudelijke aspecten.

- Menselijke aspecten:
	- Communicatieve en persoonlijke vaardigheden stakeholders.
	- Ervaring met bepaalde technieken.
	- Mate waarin stakeholders zich bewust zijn van de requirements.

- Organisatorische aspecten: 
	- beschikbaarheid belanghebbenden
		- Weinig tijd?  Veldobservatie > Interviews
		- Beschikbare budget en doorlooptijd.
		- Creatieve technieken minder haalbaar bij fixed-price / fixed date projecten.
		- Bij vervanging bestaand systeem, kies voor documentatiegebaseerde technieken.
		
- Vakinhoudelijke aspecten:
	- vereiste detailniveau beïnvloed keuze
	- ervaring analist met bepaalde technieken

![[BA_vb_keuze-technieken.png]]
- open cultuur waar alle medewerkers aangemoedigd worden om hun ideeën en kritiek te uiten:
	- Workshop gebruiken => Deelnemers zijn gewoon om hun ideeën te delen.
- strikt-hiërarchische organisaties:
	- Elke stakeholder moet in gelijke mate aan bod komen.
	- Zorg ervoor dat kritiek en ideeën niet achtergehouden worden => Anonieme enquêtes. 

## Addendum - interview tips
- LSD : Luisteren, Samenvatten, Doorvragen.
- Analist en stakeholder verstaan elkaars terminologie.

| HOE LUISTEREN? | HOE BRENGT U DIT IN PRAKTIJK? |
|----------------|--------------------------------|
| **EMPATHIE**<br>Luisteren op een ondersteunende en behulpzame manier. | Stel uzelf in de plaats van uw gesprekspartner en probeer u voor te stellen hoe hij denkt. Stel hem op zijn gemak en let goed op wat hij zegt. Spreek zelf weinig, maar moedig uw gesprekspartner aan met hoofdknikjes en korte antwoorden. |
| **ANALYSE**<br>Zoek concrete informatie en probeer feiten en gevoelens uit elkaar te houden. | Stel analytische vragen om uit te vinden wat de spreker exact bedoelt, zeker als u een reeks feiten of een gedachtegang wil begrijpen. Stel uw vragen omzichtig en gebruik elementen uit het antwoord om een volgende vraag voor te bereiden. |
| **SYNTHESE**<br>Stuur het gesprek pro-actief in de richting van een vooraf vastgestelde doelstelling. | Als u een bepaald doel wil bereiken, moet u beginnen met verklaringen waarop anderen met ideeën kunnen antwoorden. Luister aandachtig en laat uit uw antwoord blijken welke ideeën u waardevol vindt. Formuleer eventueel een alternatieve oplossing in uw volgende vraag. |


---
# Documenteren
## Functionele Requirements beschrijven
- Use cases (Functional Analysis)
	- Analyse techniek
	- Specificatie
- User stories
	- Communicatie middel voor requirements
	- Moet aangevuld worden met extra technieken voor specificatie

### User stories
> **INVEST**: Independent, Negotiable, Valuable, Estimatable, Small, Testable

- **Definitie**: Een korte, duidelijke beschrijving van een software feature vanuit het perspectief van de eindgebruiker.
- **Doel**: Uitdrukken van wat de gebruiker nodig heeft en waarom, in dagelijkse taal.
- **Gebruik**: Essentieel in agile softwareontwikkeling voor het definiëren van requirements.
- **Kenmerk**: Moet beknopt genoeg zijn om op een post-it te passen.

#### Voordelen
- Makkelijk te verstaan
- Makkelijk te delen
- Lage inspanning (snel opgesteld)
- Moet niet perfect zijn
- Makkelijk te plannen

### 6 aspecten
- Independent: Onafhankelijk.
- Negotiable: Het is geen contract, ze beschrijven gewoon zonder te specificeren. Ze kunnen wijzigen doorheen de tijd. Details volgen pas zo laat mogelijk.
- Valuable: Moeten business waarde bevatten. Geen voordeel? Waarom moet het dan gebouwd worden? Gesloten, we eindigen altijd met de user's goal (tenzij triviaal(=> af te leiden)). Ook moeten alle lagen van de applicatie voorkomen. (bv. Als een klant wil ik producten kunnen filteren op prijs zodat ik snel de producten kan vinden binnen mijn prijsklasse; hierdoor weten we: db model aanpassen, db query voor filteren, business logica voor filter en UI voor filter.)
- Estimatable: Schatbaar
- Small: Klein
- Testable: Testbaar
#### Voorbeeld
- Als een {wie}, 
	  wil ik {wat},
	  Zodat {waarom}

- "Als bioscoopbezoeker wil ik mijn tickets kunnen ontvangen op mijn gsm om de wachttijd aan de kassa te vermijden."

### Stories, Epics en tasks
Meerdere niveau's van details.
- Epic
     \/\
  Stories
     \/\
  Tasks
#### Epics
Groot stuk functionaliteit die de business wilt hebben en waarde oplevert. Opgeleverd a.d.h.v. kleinere user stories, gespreid over meerdere iteraties.
Format van de user stories moet niet gevolgd worden.

#### Tasks
Story kan onderverdeeld worden in uitvoerbare taken.
Geschreven door Devs en voor Devs, mag dus technisch zijn
Input DevOps is van belang! Nodige hardware/systemen, beperkingen naar security toe.

## User stories ontdekken 
### Customer Journey
- Customer journey visualiseert de ervaring van de klant van begin tot einde aangaande doelen, fases, activiteiten, contactpunten en emoties. (komt ook voor in e-marketing!)
- **Doel**: Inzicht krijgen in het gedrag van de klant. 
	- Toont mogelijke problemen.
	- Identificeert opportuniteiten.
	- aligneert de organisatie.

- **Stappenplan**:
	- Maak persona's
	- Identificeren van verschillende fases, elk met hun doel en beschrijving.
	- Identificeer contactpunten tussen klant en bedrijf.
	- Beschrijf het gevoel van de klant tijdens de actie.
	- Identificeer de belangrijkste acties.
	- Vind ideeën voor verbetering.

### [Story mapping](https://www.jpattonassociates.com/wp-content/uploads/2015/03/story_mapping.pdf)

- **Doel**: Creëert visueel gedeeld begrip (shared understanding) tussen Business en IT.
- **Opbouw**: Vertelt horizontaal een verhaal via activiteiten van een product/site.
- **Detail**: Elke activiteit wordt verticaal uitgediept met details of verschillende taken, vaak in user story formaat.
- **Prioritering**: Na ontdekking van alle activiteiten worden deze geprioriteerd en kunnen MVP's (Minimum Viable Products) worden vastgesteld.
- **Resultaat**: Vormt de start van de Product Backlog. Deze kan uiteraard nog wijzigen doorheen het doorlopen van het proces.

#### 4 stappen
1) **Prepare**: bepaal wat je wilt onderzoeken.
2) **Co-create**: Medewerkers en klanten creëren een story map.
3) **Verify**: Check story map voor volledigheid.
4) **Prioritise**: Identificeer de belangrijkste punten en kijk naar de haalbaarheid.

#### Prioriteiten
Zeer belangrijk om prioriteiten te stellen. Na elke release is user feedback van belang.

- **MoSCoW**: Must have, Should have, Could have, Won't have

---
# Valideren
Bepalen van het succes.
## GWT
> Given, When, Then

Manier om acceptatie criteria op te stellen.
- BDD (Behaviour Driven Development)
- User story als basis, bevatten meer details(kunnen UI elementen en user gedrag bevatten).
- Kan de aanzet geven tot functionele testen.
	- Kan geautomatiseerd worden.

## 3 Amigos
- Business analyst: Welk probleem willen we oplossen?
- Developer: Hoe kunnen we het probleem oplossen?
- Tester: Lost deze oplossing het probleem kwalitatief op?

Refinement sessies worden gebruikt om User Stories te verduidelijken.
- Opgesplitst in kleinere stories
- Acceptatie criteria worden opgesteld
- Stories worden opgesplitst (optioneel)

## Testplan
> Testen, de missing link tussen IT en business.

Testen zijn goed om:
- Beperken risico's.
- Te testen voor fouten.
- Aan te tonen dat requirements voldaan zijn.
- Ook het proces moet getest worden, niet enkel de resultaten.
- Geeft vertrouwen in de kwaliteit van de code.
- Volledigheid en correctheid

Testen doen we best zo vroeg mogelijk. Horen in elke fase van de ontwikkeling toe te komen, verweven in het SW-ontwikkelen. Zo blijven problemen controleerbaar. Hoe vroeger men iets test, hoe vroeger men fouten kan vinden en hoe goedkoper en sneller we het kunnen oplossen.

- Risk based testen
- Mensen, tijd, geld (in staat zijn om in te rekening te houden met hoeveel van elk beschikbaar is voor het project.)
- Verantwoorde wijze tests voorbereiden/uitvoeren
- Voldoende vertrouwen opbouwen om Software te accepteren.


### Tester profiel
- Algemene kennis van IT
- Kennis van infrastructuur, tools en IDE's
- Sociale vaardigheden

- Goed oordeel geven over kwaliteit van Software
- Toegevoegde waarde aantonen in de levenscyclus.
- Toont de knelpunten aan in het project.

### Schade aan klant en gebruiker
1) Bedreigend voor veiligheid van menselijke wezens
2) Aantasting van een essentiële organistatiefunctie
3) Aantasting van een werking van firmware
4) Aantasting essentiële functie maar vervangbaar door alternatief systeem
5) ....

- Financieel verlies
- Niet-kwantitatieve schade
	- Negatieve impact op toekomstige verkoopcijfers
	- Terugval van de huidige verkoopcijfers.


### Verschillende belangen & aandachtspunten binnen een project.
- Projectmanager: haal ik de deadline?
- Programmeur: zijn er nieuwe features?
- Gebruiker: kan ik mijn werk blijven doen?
- Beheerder: wat verandert er allemaal?
- Business manager : behaal ik mijn business-doelen?
- Tester : heb ik alles getest?

### 10 testprincipes
1) Focus op het resultaat
	1) Verificatie: systeem gebouwd volgens systeemontwerp?
	2) Validatie: business doelen gehaald? inzicht geven tot hoever het systeem past binnen bedrijfsprocessen.
2) Bouw aan vertrouwen: verstop geen fouten, maar meld ze optijd.
3) Neem verantwoordelijkheid: Juiste testen voorbereiden, test coverage, rekening houden met risico's, ... 
4) Beheers het testvak
5) Sla bruggen: Veranderende requirements, inleving in de plaats van belanghebbenden.
6) Test gefaseerd: test in een logische volgorde
7) Faciliteer de gehele IT-lifecycle: 
	1) **Ontwerpfase**: producten toetsen op testbaarheid en nagaan hoe het beoogde resultaat behaald gaat worden.
	2) **Ontwikkelfase**: hoe vroeger fouten gevonden worden, hoe beter. Module testen, module integratietesten.
	3) Beheerfase: delen van testware, goede overgang van projectfase naar beheerfase
8) Geef overzicht en inzicht: Systeem heeft veel functies. Afdekken van risico's, aandachtspunten, kwaliteitsaspecten
9) Zorg voor herbruikbaarheid: testen herbruikbaar maken. Herbruikbaarheid = kosten besparen.
10) Bedenk: testen is leuk! : Flexibel en creatief zijn, toegevoegde waarde en verantwoordelijkheid. Specialisatie is mogelijk.

### Soorten testen
- Moduletesten (MT) en module integratietesten (MIT)
	- Geautomatiseerd
	- Whitebox-testen
	- Unit testen, component testen, programma testen
- Systeemtest (ST)
	- Heel systeem testen
	- Blackbox testen
	- Werkt het systeem conform met functionele ontwerp?
- Functionele acceptatietest (FAT)
	- Heel systeem testen
	- Opdrachtgever
	- verificatie a.d.h.v. systeemeisen en functionele ontwerp

- Gebruikersacceptatietesten (GAT)
	- Validerende test
	- Representatieve scenario's uit het dagelijkse werk van de gebruikers
	- Gebruiksvriendelijkheid, bruikbaaheid, ...
- Productieacceptatietesten (PAT)
- Ketentesten
	- Samenwerken met de aanliggende systemen.
- Pilot
	- Parallel testen met bestaande systemen.

![[BA_Testen_Schema.png]]

### Methodologieën
Verschillende methodologieën
- Agile testing
- Scripted testing
- Exploratory testing
- Rapid software testing

Afhankelijk van:
- Project organisatie
- "Application criticality"
- De testers

## Testplan
- Opgesteld aan het begin van een testtraject.
- Doel: aanpak beschrijven binnen het programma, project, release of change
- Opgesteld door de verantwoordelijke van het testtraject. (testmanager, testcoördinator, functioneel beheerder of eender wie de opdracht accepteert)

![[BA_Testplan_tekening.png]]

- Waarom: Wat is de aanleiding?
- Hoe: Wat is de aanpak?
- Wat (en wie): 
	- Wat zijn de benodigde mensen en middelen?
	- Benodigde tijd?
	- Wat is het op te leveren product?

Vaak gebruikt men een template testplan.

![[BA_TestplanInUitvoering.png]]
Er is een planning die voorafgaat, eens de plan fase voorbij is komen we in de beheerfase. Dit is de opvolging om te zien of alles loopt zoals gepland.
Eerst is er de voorbereiding, gevolgd door de specificatie en uitvoering. Tot slot is er de afronden. Al deze stappen worden opgevolgd. Dit geheel aan stappen behoort ook tot de inrichting en het beheer van de infrastructuur.


## Wie voert de testen uit?
### Dedicated testing professionals
Testing is een erkend beroep. Zo zijn er diverse certificaten voor te behalen om dit aan te tonen. (vb. Scrum master, certified test manager, ...)
- Opgeleid
- Ervaren
- "Carrière"
- Mogelijkheid tot specialisatie:
	- Security testers
	- Performance testers
	- Test automaters
	- Embedded software testers
	- ...


### Agile testing quadrants
![[BA_AgileTestingQuadrants.png]]


## Kwaliteitsborging

- Controle a.d.h.v opgeleverde tussenproducten om te zien of deze voldoen aan de vooropgestelde kwaliteit eisen.
	- Hoe vroeger je een fout opmerkt, hoe goedkoper en makkelijker het is om deze te corrigeren.
- Hoe?
	- Collegiale reviews
	- Expert reviews
	- Inspecties
	- Walk-throughs
	- Monitoring (opdrachtgever) = audit

### 6 beoordelingsgrondslagen
![[BA_Beoordelingsgrondslagen.png]]

### Collegiale review
- Collega's die hetzelfde werk doen, beoordelen medecollega's.
- Collega's leren van elkaar.
- Deze personen zijn goed op de hoogte van de omgeving, problematiek en hebben een technische achtergrond.
- Minder vertrouwen in "vreemden" (audit, inspecteur)

**Positief**: collega's leren van elkaar.

**Risico's:**
- Te informeel
- Geen eenduidige beoordelingsgrondslag
	- Vooraf bepalen welke aspecten in de review moeten belicht worden.
		- Enkel inhoud? Zijn de standaarden gehanteerd? Taalfouten? Vertaalslag correct gebeurd? 
		- Voorgeschreven standaarden gehanteerd?
		- Taalfouten corrigeren
		- Controle of vertaalslag correct gebeurd is?
		- Checklist?
- Opsteller van het product en de reviewer dienen over voldoende communicatievaardigheden te beschikken.
	- Afkraken van het product wordt beschouwd als oncollegiaal gedrag
	- Maker van product mag collegiale review niet zien als aanval op zijn werk. Het product is ook niet alleen van de maker maar eerder een projectaangelegenheid.
	- Doel van de review: Het product verbeteren.
- Te vergevingsgezind
	- Wanneer er sommige afwijkingen toch niet vermeld worden.

> Aandacht voor algemene communicatievaardigheid.

### Expert review
- Expert die geen deel uitmaakt van het team.
- Resultaten blijven intern
- Iets formeler van aard.
- Gebruik van checklists en een lijst van bevindingen.
- Minpunt:
	- Expert kent de specifieke aspecten van de omgeving niet.
- Pluspunt:
	- De expert werkt onbevooroordeeld.


> Duurder maar vaak beter.


### Structured walkthrough
- Auteur leidt de groep door een document/product en licht achterliggende gedachte en keuzes toe.
- Doel: Consensus (=overeenkomst) bereiken over de inhoud.
- Auteur: Actieve rol.


### Inspectie
- 6 fasen:
	1) Planning
	   - Toetsen van de eisen waaraan het product dient te voldoen om geïnspecteerd te kunnen worden. Behulp van een checklist is handig hier. 
	   - Strategiebepaling.
	   - Verzamelen documenten
	   - Benaderen inspecteurs.
	   - Doel: Voorkomen dat kostbare tijd verloren gaat.
	2) Kick-off
	   - Kick-off meeting
		   - Maker
		   - Inspecteurs
		   - Aspecten
		   - Belang
	3) Voorbereiding
	   - Alle betrokkenen zoeken naar fouten (= belangrijke fouten die schadelijk kunnen zijn voor het proces.)
	4) groepsmeetings
	   - Kwaliteitsmanager leidt de vergadering, korte toelichting, geen discussie. Zorg voor een aangename sfeer. Goede voorbereiding is key!
	   - 3 groepsmeetings:
		   - Bevindingen-registratiemeeting
		   - Discussiemeeting
		   - Oorzaakanalyse
	5) Aanpassing product
	   - Op basis van bevindingen gebeuren er aanpassingen.
	   - Onafhankelijke functionaris (kwaliteitsmanager) checkt of alle bevindingen goed verwerkt zijn.
	   - Maker blijft eindverantwoordelijke; sommige aanbevelingen kunnen bewust aan de kant plaatsen.
	6) Afsluiting
	   * Korte rapportage
		   * Auteur
		   * Inspecteurs
		   * Management

![[BA_Toetstechnieken_Inspectie.png]]

---

---
# Managen

## [Product Owner](https://www.youtube.com/watch?v=502ILHjX9EE)
- **Cruciaal** voor het slagen van een project. 
	- Heeft een **visie** voor het project
	- **Aanspreekpunt** voor de stakeholders en dev team.
	- **Beheert** de <u>Product Backlog</u>
		- Product backlog:
			- Resultaat van een [[#Story mapping|story mapping]].
			- Kan wijzigen doorheen het project.
				- Stakeholders hebben veranderende eisen.
				- Communication is key!
			- Bepalen of iets al dan niet gedaan moet worden. [[#Schatten|Value VS Effort]].![[BA_Value_Effort.png]]

### Schatten
- **Value**:
	- **MoSCoW**: "Must have", "Should have", "Could have" en "Won't have"
	- Bepaald door de stakeholders.
- **Effort**:
	- Man-uren
	- T-shirt sizing
	- Story points

#### T-shirt sizing
Relatieve manier om werk in te schatten.
- Zeer ruw
- Bepaal eerst baseline!

| Size | Tijd |
| ---- | ---- |
| S | 0-2 Weken |
| M | 2-4 weken |
| L | 4-8 weken |
| XL | 8-16 weken |

#### Story points
Deze moeten rekening houden met:
- De hoeveelheid werk
- Complexiteit
- Risico
- Afhankelijkheid

Vaak worden hiervoor de getallen van Fibonacci (of iets gelijkaardigs dat hierop gebaseerd is => Story points) gebruikt.
	=> Hoe groter het getal in de reeks van Fibonacci, hoe minder men vertrouwd is ermee. Als PO (Product Owner) is het belangrijk om hier dan rekening mee te houden. Er moet dan gewerkt worden aan het verduidelijken van de probleemstelling. Een mogelijke andere optie is om een complex (taak met groot Fibonacci getal) op te splitsen in meerdere kleinere, simpelere en dus duidelijkere taken.
	 ![[BA_StoryPoints_Fibonacci.png]]
		- vb. Voor een bouwfirma, kan een huis bouwen gelijk gesteld worden aan 1, iets heel simpel waar men direct weet wat er van hun verwacht wordt en hoe ze het moeten aanpakken. Het heeft relatief weinig risico en werk nodig. In vergelijking met "the shard" met waarde 40, weet het team voor dit niet waar het zal moeten beginnen, hoeveel risico het effectief in zal houden en hoeveel werktijd ervoor nodig is omdat dit iets uniek is dat ze nog niet gemaakt hebben en dus geen kennis over hebben.

#### Refinement sessie
Sessies die op regelmatige basis gehouden worden om:
- Stories in te schatten, PO met Dev team.
- Prioriteiten stellen in Backlog
- Zoveel mogelijk JIT (Just In Time) werken
- Leren uit feedback loop geeft betere inschattingen.

Dev Team kan effort inschatten aan de hand van Story Points (Planning Poker)
- PO legt story uit
- Team geeft individuele schatting
- Team overlegt en bespreekt schattingen
- Team komt tot een consensus (overeenkomst) over het aantal story points van de story.


### Sprint planning
Wanneer de backlog in een goede staat is.
	d.w.z.:
		- Prioriteiten in orde
		- Top stories zijn duidelijk en hebben een schatting.

Bepalen wat er in de volgende sprint komt?
	- Velocity
	- Yesterday's weather

#### Velocity
- Snelheid van het team
	- Hoeveel werk kan er gerealiseerd worden binnen een tijdslimiet? (bv. Aantal story points binnen een sprint)
- Tijdens de sprint review sessie kan de velocity berekend worden.
	- Hoeveel story points zijn er opgeleverd tijdens de vorige sprint?
	- Wat verstaan we onder opgeleverd?
		- **Definition of done** ^61e9d9
			- Belangrijk voor een goed werkend agile team.
			- Door en voor het Dev team.
		- Development klaar? Getest? Deployed? User Accepted?
- Dit zal voor een beginnend team, beginnend project vaak fluctueren.
	- Over meerdere sprints zal dit stabieler worden.

#### Yesterday's weather
Kijken naar het verleden om een voorspelling te doen.
	- Hoeveel story points zijn er vorige sprint opgeleverd?
	- Geeft een indicatie van hoeveel werk er in de volgende sprint kan opgenomen worden.

Vaak wordt er een gemiddelde genomen van de X aantal laatste sprints.
	  - Dit voorkomt uitschieters.

### Forecasting
Door de velocity bij te houden, kunnen we aan een forecasting doet met een 'Burn up chart'.

![[BA_BurnUp_chart.png]]

### Perfecte oplossing
#### Build the right thing
Focus op de juiste oplossing. <= Rol van de PO

#### Build the thing right
Door samenwerking met het dev team

![[BA_BuildTheRightThing_BuildTheThingRight_BuildItFast.png]]

## Scrum master
- Essentiële rol in elk Agile team
- Kan [[#^61e9d9|Definition of Done]] opleggen.
- Gaat vaak op zoek binnen andere agile methodologieën naar manieren om het team te verbeteren.
	- Vaak uit eXtreme Programming (XP) volgende principes:
		- **(Automated) testing**
			- Programma zonder automated testing bestaat niet => Het is onmogelijk om zelf alles manueel op voorhand te schrijven.
		- **Refactoring**
			- Permanent ontwerp en code die wijzigt, refactoring is dus een must.
		- **Pair programming**
			- Junior met Senior, met 2 weet je meer dan alleen.
		- **Permanente integratie** 
			- Code wordt geïntegreerd en getest na enkele uren.
			- Bv. Jenkins 
				- Extra info: Open source automation server. Helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration, and continuous delivery.
	- => Geeft vertrouwen aan de klant en een goed gevoel bij de gebruiker

## Agile Tester
Iemand die verandering omarmt en goed samenwerkt met zowel technische als business mensen, het concept begrijpt van testen te gebruiken om requirements te documenteren en development te stimuleren.

---
# Processen
## Wat is een proces?
Een proces neemt input (wat vaak de output van een ander proces kan zijn) en transformeert het naar een output. Het doel van een proces is om waarde te creëren voor de belanghebbenden om zo een doel te realiseren.

Een proces kan zowel complex als iets eenvoudig zijn.

![[BA_ProcesActiviteit_termen.png]]

---

**Business case**: Vooraf eisen helder en eenduidig formuleren.

---
## BPM vs Business Analyse
Business Process Management:
	- Gericht op bedrijfsorganisatie.

Business Analyse: 
	- Gericht op IT-project.

![[BA_Proces.png]]
IT is geen directe business waarde. De veranderingen en het meer efficiënt maken van andere processen is echter wel een grote business waarde voor bedrijven.

---
### Toepassen
– **Continuous Process Improvement** (CPI)
	• Stelt de huidige processtructuur niet in vraag
	• Identificeert problemen en lost ze één voor één op. Stap voor stap. 

– **Business Process Re-Engineering** (BPR)
	• Stelt de fundamentele veronderstellingen en principes van de huidige processtructuur in vraag.
	• Gericht op het realiseren van een doorbraak, bv. door dure taken zonder directe toegevoegde waarde te elimineren.


## End-to-end
Wanneer een proces start en eindigt bij dezelfde klant.

## Proces vs. Functie
**Proces**: Verzameling activiteiten, gericht op het bereiken van één of meerdere outputs.

**Functie**: Verzameling van activiteiten, gegroepeerd volgens competentie.

### Belang van processen
- Processen zijn het hart van een organisatie.
- Lopen vaak fout bij transfers.
- 2 belangrijke dimensies in een organisatie:
	1) Strategische dimensie (doe het juiste) - Effectiviteit.
	2) Operationele dimensie (doe het goed) - Efficiëntie.

#### **Strategische dimensie**
- Gericht op verbeteren van vermogen om waarde te creëren.
- Kosten en baten afwegen met elkaar.
- ==1e stap (in BPM): Identificeren van waarde creërende stromen.==
	- Meestal primaire/kritische processen, gelinkt aan kerncompetenties van de organisatie.


## Procesmodel
- Ordenen van sleutelprocessen
- Visuele voorstelling => Op het meest globale niveau.
- 3 clusters

![[BA_Procesmodel_visueel.png]]

### 3 clusters
- **Primaire processen (=core business processen).**
	- Processen die nodig zijn om de behoeften te vervullen.
		- bv. order-intake => facturatie, product-idee tot lancering, ...
- **Ondersteunende processen (=support business processen) .**
	- Ondersteunen de primaire processen.
		- bv. aanwerving nieuw personeel, goedkeuring binnenkomende facturen, ...
- **Sturende processen (=management processen).**
	- Nodig om een organisatie(-eenheid) te sturen. 
		- bv. project management proces
	- Om te voldoen aan wet- en regelgeving.

#### Oefening
- Opgave: 
![[BA_clusters_oef_opgave.png]]
- [[BA_clusters_oef_oplossing.png|Oplossing]] (extra uitleg als sub list)
	- Een ondersteunend proces kan primair zijn, inschrijving aan hogeschool. Omdat zonder dit, er geen primaire activiteit kan plaatsvinden.


## Problemen bij processen

- **Functioneel georganiseerde organisaties**
	- Functie/afdeling = verticaal
	- Proces = horizontaal
- **Dalende doeltreffendheid door groei**
	- groei leidt tot specialisatie. Hierdoor kan men  het einddoel, de klant, uit het oog verliezen.
- **Gewoontevorming**
	- Men stelt niet meer in vraag wat men doet en hoe men het doet.


## Processen in verschillende organisatietypes
### Verticale functionele "kachelpijpen"
- Hiërarchisch
- Specifieke functie of dienst
	- IT, marketing, financiën, HR, R&D, ...
- Expertise over heel het bedrijf
- Duidelijke carrière-paden en opleidingsprogramma's.
- Backups voor elke functie
- Manager is vertrouwd met werk van ondergeschikten
- Standaarden zijn makkelijk te hanteren.
#### Nadelen
- Het geheel is een eenheid op zich. (bureaucratie; dat men hun eigen regeltjes en dergelijke begint te maken.)
- Focus op individuele dienstverlening, i.p.v. op de dienstverlening aan de klant.
- Processen zijn gericht op efficiëntie (de dingen juist doen) en niet op effectiviteit (de juiste dingen doen).
- Communicatieproblemen (eigen jargon)
- Bus. prioriteiten kunnen afwijken van functionele prioriteiten.
- Projecten voldoen niet aan de noden van de business units.

>Projecten van administratieve vereenvoudiging hebben vaak het wegnemen van verticale barrières als doel. 
>
>Vb: Ondernemingsloketten.

### Horizontale process-tunnels
- Decentralized organisations
- Focus op individuele dienstverlening
- Processen gericht op efficiëntie, niet op effectiviteit.
- Communicatieproblemen
- Bus. prioriteiten kunnen afwijken van functionele prioriteiten.
- Projecten voldoen niet aan de noden van bus. units.

#### Nadelen
- Perceptie: beperkte opwaartse carrièrepaden.
- Jobevaluaties gebeuren vaak door leidinggevenden die de job zelf niet kennen.
- Weinig back-up personeel
- Weinig synergie in het bedrag.
	- Iedere bus. unit werkt op zijn eigen manier, wat tot redundantie en inefficiëntie kan leiden.


### Spotify as a framework
Het is ontworpen om flexibiliteit, snelheid en samenwerking te bevorderen in softwareontwikkelings- en productteams. 

#### Kenmerken
1. **Tribes en Squads:** Organisaties worden opgesplitst in Tribes (stammen), die bestaan uit meerdere Squads (squadrons). Elke Squad is een klein, autonoom team met verschillende vaardigheden.

2. **Chapters en Guilds:** Binnen Squads zijn er Chapters, groepen van mensen met vergelijkbare vaardigheden. Guilds zijn informele groepen die kennisdeling en samenwerking over Squads heen bevorderen.

3. **Product Owners en Product Backlogs:** Elk Squad heeft een Product Owner die verantwoordelijk is voor de prioritering van taken op basis van de Product Backlog, een lijst met functies en taken.

4. **Spotify Tribe:** Een overkoepelende Tribe bestaat uit meerdere Squads die samenwerken aan gerelateerde delen van het product. Tribes hebben vaak een duidelijk gedefinieerde missie of doel.

5. **Spotify Coach:** Er zijn vaak coaches aanwezig om teams te begeleiden bij het begrijpen en implementeren van het Spotify Framework.

6. **Spotify Ceremonies:** Het framework omvat ceremonies zoals "Squad Kick-off" en "Tribe Kick-off" om samenwerking en communicatie te bevorderen.

Het moedigt autonomie aan en probeert silo's tussen teams te verminderen, waardoor een meer collaboratieve en wendbare werkomgeving ontstaat. 


## Procesverbetering (start)
- Kritische/sleutel processen
	- In functie van de **strategie** van een organisatie
	- Dragen bij tot het voldoen aan de **behoeften** van de **belanghebbenden**
	- zijn de sleutel tot het **succes of continuïteit** van de organisatie
	- worden bepaald op basis van **kritische succesfactoren**.
- Mogelijk vertrekpunt: **SWOT analyse**

### SWOT-analyse

![[BA_SWOT_analyse.png]]

#### Oefening
- Opgave:
  ![[BA_swot_oef_opgave.png]]
- [[BA_swot_oef_oplossing.png|Oplossing]]

---
# BPMN
## Theorie-slides
### Modelleren
Doel: Reduceren van complexiteit
 - Moet 1 boodschap bevatten, duidelijk < 10 mins.
 - Communicatiemiddel.
 - Geeft antwoord op concrete vragen
 - Meer dan tekenen van diagram.
	 - Bevat: gegevenstypes, voorwaarden, gegevens-mappings, foutafhandeling, ...
 - Alle modellen zijn onvolledig, sommige nuttig.
 - Meerdere modellen van 1 proces.

Communicatie, simulatie, kostprijsberekening.
![[BA_DoelVanModelleren.png]]

#### Partijen:
	 - Strategische consultants
	 - Business analisten
	 - Process designers
	 - Systeem architecten
	 - Software engineer

#### BPMN (Business Process Modelling notation) VS BPEL (Business Process Execution Language)
BPMN: Bedrijfsomgeving | doel: modelleren
BPEL: Technologische implementatie | doel: Uitvoeren

BPMN 1.0/1.1 naar 2.0 heeft significant veel meer events. 63 events in BPMN2.
	- Tools: 
		- Visual Paradigm
		- Draw.io
		- ARIS (express)
		- ....
	- Bestaat uit:
		- (Intermediate( vinden plaats tussen het begin en einde van een proces)) Events, Tasks, Flows en gateways, gerichte en ongerichte associaties, annotations (voor extra info te geven), data objects, data stores (containers van data objecten die moeten gepersisteerd worden na de levensduur van het proces).
		- Resource: Menselijke actor of toestel die nodig is om activiteit uit te voeren.
		- Resource klasse: Verzameling resources met gemeenschappelijke karakteristieken.
			- Voorgesteld als zwembaden of zwembanen.
				- Zwembad: Onafhankelijke organisatorische eenheid. (vb. klant, leverancier, ...)
				- Zwembaan: Resource klasse binnen dezelfde organisatie, die gebruik maken van dezelfde systemen. (vb. Verkoop, marketing, productie, HR, ...)

Er zijn verschillende gezichtspunten (perspectieven) op een proces.
	- Organisatorisch niveau <-> Functie Niveau <-> Niveau van een bepaalde Dienst/ Gegevens/Product ![[BA_GezichtspuntenOpProcessen.png]]

#### Voorwaarden:
- Een goed model bevat alleen die aspecten waar je grip op probeert te krijgen.
- Modelleren is kiezen tussen twee uitersten.![[BA_Modelleren_uitersten.png]]
- Goed model bevat een boodschap => Communicatiemodel.

| Beperkingen | Voordelen |
| ---- | ---- |
| Vele poorten verminderen leesbaarheid | Rollen zijn duidelijk weergegeven |
| Beperkt aantal objecten:<br>geen andere objecten dan rollen, activiteiten en outputs zijn weergegeven. (dus geen plaats of tijd) | Activiteiten en hun volgorde zijn duidelijk weergegeven. |
| Slechts 1 voorstellingswijze | Inputs en outputs (of interacties) tussen rollen zijn zichtbaar. |
| Geen datamodellen mogelijk | Internationale standaard |
| Geen materiaalstromen | Link met BPEL |
|  | Toegankelijk voor business |

#### BPMN poorten
![[BA_BPMN_Poorten.png]]
-> Belangrijk om ervoor te zorgen dat er default flow is. Deze vermijden deadlocks.
#### Activiteiten
Kenmerken:
	- Duurtijd (tijd >0)
	- Middelen verbruik
	- Uitgevoerd door een rol
	- Altijd een trigger
	- Minstens 1 (intermediaire) output.
	- Leidt tot een status
	- Uitgevoerd op 1 of meerdere plaatsen.
- Benaming: "Verzenden van vergunning" (<u>ww</u> VAN iets).
	- <u>ww</u> moet specifiek genoeg zijn. Vb: Beheer is te vaag. | Actieve werkwoorden gebruiken.

#### Verbindingselementen
- **Sequentiële stroom**: binnen eenzelfde zwembad over 1 of meerdere zwembanen.
- **Boodschappenstroom**: enkel tussen verschillende zwembaden.

##### Associatie
Verbindt info en artefacten met stroomelementen.

#### Vaak voorkomende fouten
![[BA_VeelVoorkomendeFoutenBPMN.png]]

#### Stappenplan
1) Bepalen doel van het BPMN diagram
2) Context van het proces
3) Zwembaden en zwembanen bepalen
4) Begin en einde van elk zwembad bepalen
5) Bepalen verschillende activiteiten, poorten en tussentijdse evenementen en de sequentiële stromen binnen elk zwembad.
6) Vervolledigen diagram met artefacten waar nodig.

## Presentaties
Termen die bij de opdracht aan bod kwamen:
### Agile Manifesto
Het Agile Manifesto is een leidende set principes voor softwareontwikkeling, waarbij de nadruk ligt op individuen en interacties, werkende software, samenwerking met klanten en het vermogen om te reageren op veranderingen boven vasthouden aan strikte plannen en processen. Het richt zich op flexibiliteit, klanttevredenheid en continue verbetering.

### ERP
> Enterprise Resource Planning

Softwaretoepassingen die bedrijfsprocessen automatiseren en informatie stroomlijnen binnen een organisatie, waaronder financiën, voorraadbeheer, human resources en andere kernactiviteiten.

#### PRINCE2 (PRojects IN Controlled Environments) 
PRINCE2 is een gestructureerde projectmanagementmethode die uitgebreide richtlijnen en best practices biedt voor het beheer van projecten. Het verdeelt projecten in beheersbare fasen, met duidelijke rollen, processen en documentatie om de efficiëntie en effectiviteit van projecten te verbeteren. PRINCE2 is flexibel en kan worden aangepast aan verschillende projectomgevingen.

#### PMBOK (Project Management Body of Knowledge)
PMBOK is een referentiehandleiding die is ontwikkeld door het Project Management Institute (PMI). Het biedt een uitgebreid raamwerk van processen, kennisgebieden en best practices die nodig zijn voor effectief projectmanagement. PMBOK benadrukt vijf procesgroepen (initiëren, plannen, uitvoeren, monitoren en controleren, en sluiten) en tien kennisgebieden, waaronder scope, tijd, kosten, risico en communicatie. Het is meer een overkoepelende gids die kan worden toegepast op verschillende projectmanagement methoden.

#### ALM
> Application Lifecycle Management

Het is een geïntegreerde set van processen, tools en best practices die de levenscyclus van een softwaretoepassing beheren, vanaf de initiële conceptie en planning tot aan de ontwikkeling, testen, implementatie, en uiteindelijk het beheer en onderhoud. ALM streeft naar een gestroomlijnde en gecontroleerde aanpak om de ontwikkeling en levering van hoogwaardige softwareproducten te optimaliseren. Het omvat aspecten zoals requirements management, versiebeheer, testen, release management en rapportage.


---
# Workshop-Refleqt
**SDLC**: Software Development LifeCycle

Waterval => Alles of niets, testen vormen een bottleneck omdat ze pas op het einde staan.

## Shifting to the left:
De testen als een **vroegere** fase in het ontwikkelen beschouwen.

Vroeg testen, geautomatiseerde tests tijdens de ontwikkelingsfase, integratie van beveiligingscontroles in de ontwerpfase.

![[BA_Refleqt_ShiftLeft.png]]


Kwaliteit start bij de "check". Het is dus belangrijk dat dit niet alleen op het einde gebeurt, maar ook doorheen sprints.

### Tri amigo systeem
Mensen met verschillende achtergronden die rond eenzelfde topic gaan brainstormen.

- Functioneel Analist
- Software Developer
- QA (Quality Assurance) Engineer

Deze 3 werken samen met de Product Owner.

#### BDD - Behaviour Driven Development
![[BA_Refleqt_BDD.png]]

## Shifting right
De testen als een **latere** fase in het ontwikkelen beschouwen.

Nadruk op monitoring, feedback van gebruikers en continue verbetering na implementatie in de productieomgeving.

Technieken:
- Synthetic user monitoring
- Canary releases
- A/B testing
- Chaos engineering
- ...

### Canary release
De update enkel uitvoeren naar een beperkt aantal users en slecht met een beperkt aantal veranderingen per keer, zij dienen als proefpersonen. Zo kunnen er fouten gerapporteerd worden en kan de versie verbeterd worden alvorens andere mensen de update krijgen. 

Beta/alpha/pre build participants. Deze krijgen pre releases om te testen of zaken al dan niet goed werken. Hierop kan gemonitord worden.

### A/B Testing
2 versies gebruiken. Een subset van users krijgt versie A en het andere deel versie B. We kijken welke versie het "beste" werkt, als in: welke versie behaalt onze doelstellingen het meeste?

### Chaos engineering
Proactief identificeren van zwakke punten en potentiële storingen in het systeem. In plaats van te wachten tot problemen zich voordoen in een productieomgeving, simuleert chaos engineering opzettelijk onverwachte gebeurtenissen of storingen om te zien hoe goed een systeem presteert onder stressvolle omstandigheden.

Het doel is om de veerkracht en betrouwbaarheid van een systeem te verbeteren, zodat het beter bestand is tegen echte operationele uitdagingen. Door gecontroleerde chaos te introduceren, kunnen ontwikkelaars en operators inzicht krijgen in de zwakke punten van een systeem en proactief maatregelen nemen om de algehele stabiliteit te verbeteren.

Vb. bij Netflix. Enige wat telt is views per second. Per cluster kijken naar hoe succesvol die is. Indien een cluster al dan niet succesvol is, kan hierop ingegrepen worden.

---
Alles testen is niet mogelijk, het beste is dus om een selectie.

![[BA_Refleqt_Piramide.png]]

### Icecone strategy
Exploratory testing
**E2E testing**: Hele ketting testen, bv. bij bank, geld is verzonden oké, maar is het ook aangekomen? Dit gaan we testen en is dan E2E.
Integration test: meerdere zaken te samen testen om tot 1 geheel te komen.
**Unit test**: Individuele testen voor de kleine zaken in de applicatie.

Hoe hoger we gaan in de cone, hoe duurder de kost is. Hoe lager in de cone, hoe lager de precisie, betrouwbaarheid en snelheid.

## Sanity VS Regression

| Sanity | Regression |
| ---- | ---- |
| 20% of the functionality & 80% of the actual usage | 100% of the features covered |
| Executes after each commit | Executes time based, at least once a day. |
| Focus on happy cases | Focus on both happy and error cases. |
| E2E flow of the applications | All functionalities covered by individual test cases |
| Focus on one browser <> Platform | More relevant combinations |

---

## Spring
### What is spring
- Programmeren in Java, maar sneller, makkelijker en veiliger.
- Legt focus op: Snelheid, simpliciteit, productiviteit, flexibiliteit, ...

## Cucumber
### What is cucumber
![[BA_Refleqt_Cucumber_Syntax.png]]

![[BA_Refleqt_Cucumber_InAction.png]]

## Appium
### What is Appium
- Open source automation tool: Server en client.
- Om mobiele applicaties te testen: Android, IOS & Hybrid.

