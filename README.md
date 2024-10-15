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

  Ook had ik een GO gekregen om oba-congres op productie te zetten. Hier heb ik een pr voor aangemaakt van `develop` naar `master`, en nadat Colin de pr goed heeft gekeurd, op buddy de deploy heeft gedraait (Hier hoefde geen backups of iets voor gedraait te worden aangezien het een singlepage website is zonder database of iets) kon ik een release aanmaken `v1.2.2`. Colin vroeg zich nog af of het niet `v1.3.0` moest zijn maar ik zei dat het in principe alleen maar content changes zijn voor de gebruiker en dit voegt verder geen extra features toe en daar was hij het mee eens. 
  <!-- [screen shots] -->

  #### Code enviroments & andere tools

  Bij Onetribe gebruiken ze Bitbucket en Github om hun code op te slaan. Dit verschilt per project door de fusering met noProtocol. 

  - Jira -> Issue boards
  - Sentry -> debug, errors etc?????
  - Algolia -> search functies ???
  - Dato, Craft cms -> content management system
  - Heroku -> Database?
  - Extra widgets zoals FOYS of localfocus -> hiermee komt vaak de klant mee aanzetten. Hier kiest Onetribe dus niet perse voor, en hebben dus ook vaak problemen door bugs bij de andere partij.
  - Buddy.works om websites te deployen

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

## Analyse feedbackformulieren 

## Reflectie

## Bijlagen




