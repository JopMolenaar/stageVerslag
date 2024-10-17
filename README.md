# Stage verslag Onetribe
## _Jop Molenaar, 500880472, CMD Amsterdam_

    Functie: Front-end developer
    Docentbegeleider: Anne Marleen Olthof
    Bedrijfsbegeleider: Michael Post, full-stack developer
    Datum: <!-- oplevering datum-->

## Inleiding

<!-- geef aan waarom je stage hebt gelopen bij dit bedrijf. Hoe ben je bij dit
bedrijf terecht gekomen? Hoe is de stage je bevallen? De inleiding moet de lezer
prikkelen om verder te lezen -->

## Omschrijving van het stage bedrijf

<!-- Plaatjes enzo -->

Onetribe is een bedrijf in de houthavens (Amsterdam) dat gefocust is op het maken van websites met een extra oog op een goede gebruikerservaring. Ze gebruiken vooral Nuxt.js en Vue.js voor hun projecten maar aangezien ze een tijd geleden zijn gefuseerd met noprotocol hebben ze ook een aantal projecten met twig en php. Aangezien ze Nuxt.js en Vue.js gebruiken  voor hun projecten zijn er weinig backend developers nodig. De organisatiestructuur bestaat uit een aantal afdelingen. Hier werken visual designers, user experience designers, veel front-end developers, een aantal backenders, contentmakers, copywriters en projectmanagers. 
Ik heb dit bedrijf gevonden door te browsen op het internet. Na wat rondgekeken te hebben op de website sprak dit bedrijf mij al erg aan. Dit komt doordat ze extra aandacht geven aan wat een website echt goed en compleet maakt. Hierbij horen bijvoorbeeld responsiveness, toegankelijkheid en performance en zagen de projecten die ze hadden gemaakt er aantrekkelijk uit. Ook is dit een groter bedrijf dan waar ik eerder stage heb gelopen en dit geeft mij de mogelijkheid om te kunnen vergelijken. Onetribe maakt ook gebruik van frameworks en dit is iets waar ik nog geen ervaring mee heb, en weet zeker dat ik daar veel van kan leren.  

## Profielschets bedrijfsbegeleider

Mijn bedrijfsbegeleider is Michael Post en is een full-stack developer bij Onetribe en personal trainer. Hij heeft CMD gestudeerd en daarnaast functies gehad als front-end developer en project manager. Hij kan mij zeker wat leren aangezien hij veel ervaring en kennis heeft in het vak en aan dezelfde (soort) projecten werkt als ik tijdens mijn stage. 

## Jouw functieomschrijving

Mijn functie die ik ga uitvoeren is front-end developer. Hierbij ga ik meewerken aan projecten op basis van Nuxt.je en Vue.js en kan ik worden gevraagd om werk te testen en aan te geven waar er verbeteringen gemaakt moeten worden of zelf te verbeteren. Deze projecten zijn voor bedrijven zoals Peakz padel. De gebruiker moet op deze websites vaak informatie kunnen vinden en bepaalde acties kunnen ondernemen waar de service voor bedoeld is zoals iets kopen of boeken. 
Het team waarin ik kom te werken zijn vooral andere developers, designers, UX’ers, en project managers.

## Werkzaamheden

<!-- wat heb je concreet gedaan. Een uitgebreide beschrijving van de
jouw werkzaamheden en van jouw gemaakte beroepsproducten. Laat afbeeldingen
zien van wat je hebt gemaakt en het proces erachter. TIP: Gebruik hierbij het logboek
dat je tijdens je stage hebt bijgehouden -->

  ### Werkwijzen Onetribe

  Aangezien Onetribe gefuseerd is met noprotocol hebben ze nu nog meerdere werk-omgevingen en manieren voor de versie beheer. Ik dacht eerst dat er meerdere manier waren maar uiteindelijk kwam ik erachter dat ze allemaal de git flow manier willen aanhouden. Hierbij wordt de versie van je applicatie automatisch geupdate aan de hand van wat je in je commit messages zet. Ook worden de branches automatisch in een map geordend aan de hand van wat je voor je branch zet. Naast git flow heb ik ook geleerd dat ze de commit messages in voltooide tijd schrijven, dit is handig want dan leest diegene die het reviewed wat die changes gaan doen en niet wat ze al gedaan hebben, want dat is niet zo. 

  #### Git flow

  Om de versie beheer goed inzichtelijk te houden maken ze gebruik van git flow.
  Je zet `feature/`, `hotfix/` of `release/` voor de titel van je branch als je die cloned en de titel van je commit is eigenlijk vaak ook je issue nummer. Welke het meest wordt gebruikt is `feature/`.
  Voor de semantic release (het versienummer van je project die je automatisch kan updaten aan de hand van hoe je je commits opbouwt) moet je je commits beginnen met chore:, fix:, feature: of perf:. 
  voorbeelden:

  ![Git flow](images/gitflow.png)

  > Bron: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow 

  Ook zei Raoul dat niet iedereen zich aan de standaard van git flow houdt en vind dat je je gewoon aan de standaard moet houden en niet dingen er bij moet verzinnen die je dan eerst weer moet uitleggen. 

  ##### Git flow deployment 

  Nadat ik een feature had gebouwd voor DRN heb ik samen met Raoul DRN kunnen deployen naar productie (de website die live staat). Dit mocht na een GO van de klant. Eerst moesten we een nieuwe versie releasen om de versie tag up te daten. Deze werd v2.1.0 aangezien er een commit met feat: (feature added) begon en moesten we handmatig schrijven aan de hand van de git flow. Dit kan automatisch worden gedaan maar aangezien github soms dingen meeneemt die niet de bedoeling zijn hou je het hier mee in eigen hand. Daarna hebben we een pull request gemaakt van `develop` naar `master`. Hierin stonden stappen die we moesten doorlopen voor deze deploy en dat waren: 

  ```
  - [x] Nieuwe versie tag: vX.Y.Z
  - [x] Backup van productie database downloaden (evt. minus activity logs content)
  - [x] Nieuwe env variabelen? Op productie dyno instellen (check: .env.example)
  - [x] PR aanmaken van [acceptance|develop|release]-branch naar [main|master]
  - [x] Nieuwe Node versie? Set node versie in buddy action “Execute yarn lint. semantic release” (check in .nvmrc & package.json)
  - [x] Productie deployen (via BuddyWorks/Heroku)
  - [x] Na deployment In het CMS de nieuwe velden voorzien van teksten (popup titels, beschrijvingen, etc.)
  - [x] Eventuele Freeform formulieren aanvullen met nieuwe velden
  - [x] PR mergen
  - [] Branches Cleanup (alleen master, develop en feature-branches over?)
  - [x] Backmerge Master
  ```

  De eerste stap was dus het aanmaken van een nieuwe versie tag doormiddel van semantic release, alleen dan handmatig. Daarna maakte Raoul een backup van de database, dit is belangrijk voorals de deployment fout gaat, dan kan je het namelijk altijd terug zetten. Nieuwe env's hadden we niet. PR hadden we ook gemaakt. We hadden geen nieuwe Node versie dus die konden we ook overslaan. Daarna heeft Raoul de `develop` branch gedeployed in BuddyWorks. 
  Terwijl het aan het deployen was liet Raoul mij Cypress zien waarmee je met bepaalde scripts heel snel websites (vooral de basis functionaliteiten zoals of zoeken werkt en of je geen lege lijst krijgt bij een bepaalde pagina) kan testen. Hij raadde mij dit wel aan om in te duiken. 
  Daarna was het geployed en konden wij `develop` naar `master` mergen. Daarna moesten we nog een backmerge doen van `master` naar `develop` om 100% zeker te zijn dat alles changes die in master zitten ook in develop zitten (denk aan hotfixes of iets dat nog niet is gemerged naar develop). 

  Na de deploy even gekeken of het allemaal goed werkte op productie daarna weer doorgegeven aan Lars. 

  Content kon ik al toevoegen maar aangezien de klant juist de optie wilde om daar een video te plaatsen heb ik dat niet gedaan, Lars uiteindelijk wel. 

  Ook had ik een GO gekregen om oba-congres op productie te zetten. Hier heb ik een pr voor aangemaakt van `develop` naar `master`, en nadat Colin de pr goed heeft gekeurd, op buddy de deploy heeft gedraait (Hier hoefde geen backups of iets voor gedraait te worden aangezien het een singlepage website is zonder database of iets) kon ik een release aanmaken `v1.2.2`. Colin vroeg zich nog af of het niet `v1.3.0` moest zijn maar ik zei dat het inprincipe alleen maar content changes zijn voor de gebruiker en dit voegt verder geen extra features toe en daar was hij het mee eens. 
  <!-- [screen shots] -->

   ##### Merge regel

   Bij Onetribe is er een regel dat je je eigen branch merged. Dit is een regel die bij mijn minor bij de HBO ICT het tegenovergestelde was. Daar gelde je merged meteen de branche die je hebt geapproved, als er iets fout is aan de changes, dan zijn jullie allebei verantwoordelijk. Aangezien degene die het approved en mergen goed had moeten testen en reviewen. 

   Bij Onetribe geld dat niet. Hier maak je een pr, deze wordt gereviewed, feedback gegeven of approved en dan mag je hem daarna zelf mergen. Dit geeft als gevolg dat de reviews niet uitermate wordt getest en vooral wordt gekeken naar de kwaliteit van de code. Wel is dit sneller qua reviewen, is alleen degene die het heeft geschreven verantwoordelijk maar geeft mogelijk wel meer kleine (over het hoofd geziende) issues later omdat 1 persoon mogelijk meer fouten maakt dan 2 mensen bij elkaar. 

   Wel is dit natuurlijk een professionele omgeving waar iedereen op een redelijk niveau codeerd en niet zoals op school waar een deel er niks van begrijpt en je juist van elkaars code ook wil leren.

  #### Code enviroments & andere tools

  Bij Onetribe gebruiken ze Bitbucket en Github om hun code op te slaan. Dit verschilt per project door de fusering met noProtocol. 

  - Jira -> Issue boards
  - Sentry -> Website monitoring (debug, errors)
  - Algolia -> Search
  - Dato of Craft cms -> content management system
  - Heroku -> Hosting
  - Akamai -> Cache
  - Screamingfrog -> SEO test
  - Extra widgets zoals FOYS of localfocus -> hiermee komt vaak de klant mee aanzetten. Hier kiest Onetribe dus niet perse voor, en hebben dus ook vaak problemen door bugs bij de andere partij.
  - Buddy.works tussen iets om websites te deployen/hosten

  #### Vue.js/Nuxt.js Onetribe

  Veel projecten maken gebruik van het Vue.js/Nuxt.js framework. Dit was helemaal nieuw voor mij dus dit was erg interessant. 
  Wat ik meteen al zag is dat dit erg component based wordt geschreven. Je hebt pages, en die bestaan uit components, en sommige components bestaan weer uit andere components. Door data door te geven en te kijken of bepaalde dingen moeten worden ingeladen als het nodig is, kun je dus met dezelfde componenten verschillende pagina's maken, zonder veel code duplication. Ook hebben deze componenten hun eigen component based styling en scripts. 
  <!-- meer voorbeelden en code hieronder -->

## Leerdoelen

  ### Samen ontwerpen

  ### Prototypen en uitwerken

  ### Evalueren

  ### Oriënteren en begrijpen

  ### Verbeelden en conceptualiseren

## Observatieopdrachten

Voor de drie observatieopdrachten wilde ik onder andere stand-ups bijwonen, een livegang bijwonen en een kick-off/ start development proces van een project bijwonen. Dit is allemaal gelukt. 

Ik heb veel **standups** bijgewoond waar verschillende functies bij aanwezig waren. Daarbij heb ik goed opgelet, geluisterd en input gegeven. Daarnaast vinden er ook veel gesprekken op de wwerkvloer plaats waar dingen worden besproken over projecten, volgende moves en statussen. Deze heb ik ook gezien, bijgewoond, en zelf gestart. Hierdoor heb ik een goed beeld gekregen over de samenwerking en communicatie op de werkvloer binnen het team en hieraan zelf ook meegedaan en zelf geoefent. Communicatie is key, je kan beter iets te veel zeggen dan te weinig. Wat ze met die informatie doen is niet jou probleem. Wel is het handig om de tijd van een ander te respecteren en bijvoorbeeld meerdere vragen tegelijkertijd stellen in person of in de mail. Hierdoor wordt de persoon niet onnodig meerdere keren uit zijn flow gehaald. 
Wat er besproken wordt in de standups is vaak of er nog meer informatie is van de klant, statussen van tickets van de developers naar de pm'ers.

<!-- - Ook wil ik graag een sprint voor de livegang en de livegang zelf bijwonen. Zo kan ik antwoord krijgen op hoe gaat dit in zijn werk, hoe werkt iedereen voor een bepaalde deadline, hoe gaat de communicatie tussen de klant, externe stakeholders, project managers en developers. Komen er nog veel dingen bij als je eenmaal live bent gegaan, dingen waar klanten nog op komen of niet chill vinden nadat ze live zijn gegaan.  -->

**Livegang** van bepaalde websites heb ik ook zeker gezien, en zelfs zelf gedaan. De grootste livegang was die van peakz padel. Deze website zat in totaal al een jaar in het development traject en aan het einde is er steeds meer focus op gekomen. Dit kwams onder andere doordat er een definitieve datum was wanneer er banen kwamen in duitsland en voor die tijd moest de webiste af. Uiteindelijk is die in de 5de week van mijn stage live gegaan. Eerst Nederland (deze was het spannendst) en daarna Duitsland (dezelfde source code, alleen andere content). Dit ging allemaal makkelijker dan verwacht. Voor de livegang was er nog een spoed overleg omdat er peformance issues waren (onnodig data verkeer). Dit zou ervoor zorgen dat de site er snel uit zou liggen als er veel bezoekers op zouden komen. Uiteindelijk is ervoor gekozen om de livegang alsnog door te laten gaan en in Heroku (waar de website wordt gehost) een quick fix te doen waardoor de server scaleable is en deze hoeveelheid dataverkeer dus aan kan. Dit kwam wel met een kosten plaatje van 3500 euro per maand dus dit moest snel gefixed worden. 
Colin en Wiebe hadden de laatste dingen naar master gemerged. En Tim en Stef gingen het stappenplan van Job doorlopen om de website op productie te krijgen en te koppelen aan de DNS records. Na de livegang zaten de pm'ers op te letten of de website het goed deed en hielden contact met de klant. Ondertussen waren Colin en Wiebe de website aan het optimaliseren en ik was andere bugs aan het oplossen. Een aantal dagen later was dit allemaal opgelost en kon Duitsland live. 

<!-- - En het liefst zou ik een kick off van een project bijwonen, een beginnend project in kijken of de start van het development traject willen bijwonen of aan mee werken. Zo krijg ik meer inzicht over hoe het vanaf het begin in zijn werk gaat, door welke handen zulke projecten gaan voordat het live gaat.  -->

Ik heb ook een **kickoff** van een nieuw project bij kunnen wonen. Dit project begint aan zijn development traject nadat het door de discovery, concept en bijna de design fase is gelopen. Deze kickoff begon met een meeting onder de developers zelf samen met een pm'er om deze dingen te bespreken:

- Het concept te bespreken
- Wat het is **=>** (15 websites naar 1 webiste, veel content, geen lastige styling, blokken bouwen, wel veel clickouts)
- Welke tech stack **=>** Craft blokken bouwen, twig templating language, styling tailgrid, (1 tool waar vue voor wordt gebruikt (alleen ingelanden op die pagina))
- Wat belangrijk is **=>** pagespeed, accessability en de grootste uitdaging is het goed opzetten van de craft structuur zodat het voor de klant en content beheerders het makkelijk is om overizichtelijk content te beheren. 
- Taak verdeling
- Planning
- Deadline
- Eerste taken
- Doelen 

Verder werd er besproken hoe ze het willen bouwen, nieuwe dingen zoals (craft 5, tailgrids, algolia ook relatief nieuw voor veel developers)

<!-- ##### kickoff Patienten federatie -->
<!-- Verder werd er besproken:
 Wat is het (15 websites naar 1 webiste, veel content, geen lastige styling, blokken bouwen, wel veel clickouts)
 Tech stack waarvoor is gekozen: craft blokken bouwen, twig templating language, styling tailgrid, (1 tool waar vue voor wordt gebruikt (alleen ingelanden op die pagina))
Wat belangrijk is: pagespeed, accessability en de grootste uitdaging is het goed opzetten van de craft structuur. 
Alles van scratch
Verder is er dus een tool uit een website die opnieuw moet worden gebouwd. 
Gesprekken over hoe ze het willen bouwen, nieuwe dingen zoals (craft 5, tailgrids, algolia ook relatief nieuw voor veel developers)
Taak verdeling
Prioriteit/focus: snel, leesbaar voor content beheerders in craft, toegankelijk
Planning, deadline, eerste taken en doelen, tickets -->

Uiteindelijk moest ik even onderzoek doen naar Tailgrid. Hoe werkt het en wat heeft het.
Het bestaat eigenlijk uit templates en components die gemaakt zijn met tailwind. De installatie is makkelijk. Tailgrid heeft ingebouwde functies om bijvoorbeeld classes te togglen en `:class=""` toe te voegen aan de hand van een boolean etc. Dit scheelt javascript schrijven. Qua menging met twig is het makkelijk want alle data gaat zo: `{{{ data.iets }}}` en twig heeft ook loop functies, verder is het allemaal html waar je de tailwind classes op kan zetten. Design gebruikt ook tailgrids dus dat is ook makkelijk want dan kan je de gekozen tailgrid components opzoeken, kopieeren en customizen. 

<!-- Tailwind en tailgrids installeren

De tailwind.config.js updaten met tailgrids als plugin: plugins: [require("tailgrids/plugin")]

input.css opzetten en tailwind includen

Build command toevoegen en de output.css toevoegen aan het twig component

Tailgrids gebruikt alpine.js voor interactieve componenten. Dit komt niet gelijk mee met tailgrids dus dat moet apart geïnstalleerd worden. 

Verder kunnen we html templates en/of componenten kopiëren uit tailgrids aan de hand van het design dat ook gebruik maakt van tailgrids en omschrijven naar een mooie twig componenten. -->

Daarna heb ik nog vragen gesteld over algolia en craft aan Colin. => Beter beeld over wat er gedaan moet worden voor hun. 
In craft staat alle content, dat wordt gelinked met algolia, dat wordt ingeladen op de website en kan makkelijk en snel zoeken in wat in algolia staat. Verder gevraagd over wat ze denken te doen in craft. Sections in sections kunnen niet. Entries (soort pagina's) en reusable entries (herbruikbaare pagina's) bestaan ook. Verder vindt Tim het niet echt een goed idee om een tag op pagina's te zetten onder welke omgeving die moet komen, er zijn namelijk drie omgevingen met secties die pagina's bevatten. En in die omgevingen zijn een aantal secties hetzelfde, en je wilt geen dubbele pagina's maken. Ik zei dus tegen Colin of hij die niet als reusable pagina kon maken en die dan op meerdere pagina's kunnen gebruiken. Hij zei dat dat kon maar dat het niet echt zo werkt. 

Verder hadden we de volgende dag nog twee andere meetings waar ik bij kon zitten. Deze meetings waren met design en UX en daar werd vooral de focus besproken voor nu. Ook werden de wireframes en informatie structuur doorlopen en werden er punten opgesteld terug naar de klant waar op sommige punten stevig druk op moest worden gevoerd. Dit komt omdat de klant vaak laat is met dingen aanleveren of feedback geven. 

Ook werd er gegeken of ze dingen aan het concept konder tweaken waardoor het werk scheelt, en het beter is voor de gebruiker. 

<!-- Als die feedback steeds in fases laat komt dan is daar vaak geen tijd meer voor en dat is zonde. Ook verspilt dit uren aangezien het voorkomen had kunnen worden en soms changes terug moeten worden gedraaid aan de hand van feedback die er al had kunnen zijn.  -->

Ook werd er discussie gevoerd over bepaalde beslissingen met betreft opzet CMS omdat dit veel gevolgen gaat hebben op uren en hoe de klant straks content beheert. 

> Week 1 PFED = Job (backend developer) heeft craft, sentry, heroku (productie, staging) en AWS opgezet. Colin heeft de structuur van craft uitgedacht in excel en gespard met Raoul hiervoor. 

> Week 2 PFED = 










## Analyse feedbackformulieren 

## Reflectie

## Bijlagen




