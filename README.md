# Stage verslag Onetribe
## _Jop Molenaar, 500880472, CMD Amsterdam_

    Functie: Front-end developer
    Docentbegeleider: Kevin van der Wiel
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

<!-- 
Wat heb je concreet gedaan. Een uitgebreide beschrijving van de
jouw werkzaamheden en van jouw gemaakte beroepsproducten. Laat afbeeldingen
zien van wat je hebt gemaakt en het proces erachter. TIP: Gebruik hierbij het logboek
dat je tijdens je stage hebt bijgehouden.

- uitgebreide beschrijving van 
-- mijn werkzaamheden
-- jouw gemaakte beroepsproducten (afbeeldingen + proces)
-->

Ik heb tijdens mijn stage meegewerkt aan meerdere projecten waaronder Peakz padel, Oba congres en oba leef en leer. Vista hypotheken, De Rijke Noordzee, en natuurlijk het grootste project van de hele stage waaraan ik heb gewerkt: Patiëntenfederatie. 

Aan het begin van de stage werd ik op Peakz padel gezet dat in zijn laatste fase zat van de development fase. Hier kon ik nog de laatste features bouwen en vooral bugs oplossen en inkomen in het leren van een nieuw framework namelijk vue.js/nuxt.js, maar ook alle andere systemen en flows waar Onetribe gebruikt van maakt. Hierbij kwam ik ook als eerst in aanraking met standups met verschillende disciplines bij elkaar. Voor Peakz padel heb ik veel contact gehad met andere disciplines om het product dat bijna zou worden opgeleverd nog iets beter te maken. Zo heb ik bijvoorbeeld ook input kunnen geven bij problemen zoals het weinig ruimte over hebben in de navigatiebalk nadat de Duitse vertalingen van peakz padel .de binnen kwamen. Maar op dit project heb ik ook wat kunnen bijdragen aan het verbeteren van de user experience van de formulieren om events aan te vragen via de website. Op de website waren namelijk knoppen die naar hetzelfde formulier gingen, maar wel de gebruiker al een keuze liet maken over een bepaalde vraag in het formulier. Dit werd alleen nog niet meegenomen in het formulier zelf. Na wat research naar Noteforms kon ik deze feature implementeren en zorgde ik ervoor dat de manier waarop de klant dit later zelf kon doen duidelijk was. Dit ben ik ook nog een keer nagegaan bij een project manager. 

![](images/keuzeFormPeakz.png)

![](images/preFilledFormPeakz.png)

![](images/lastBreakPointPeakzDe.png)

Bij Oba leef en leer heb ik mijn nieuwe vue kennis kunnen toepassen op wat complexere problemen. Zo heb ik mij bijvoorbeeld kunnen verdiepen in een bug waar een afbeelding op bepaalde breakpoints super klein werd.

![](images/smallImageLEL.png)

Maar ook kunnen bezig houden aan een probleem met de filter functie op locaties op de website. Bij een filter optie op de website lukte het niet om op bepaalde filters te filteren. De website van Onetribe handelde alles goed af, maar het lag juist aan de service die werd gebruikt om te filteren. Die gaven namelijk niet de goede url terug van de kaart met alle gefilterde locaties. Om verwarring voor de gebruiker te voorkomen heb ik in de code de betreffende filters uitgecommend (zodat dit niet opnieuw moet worden geschreven door een developer), en een comment erboven toegevoegd over waarom het is uitgecommend. 

![](images/obaFilters.png)

Daarna heb ik nog wat aanpassingen gedaan zodat:

- De gebruiker niet verward raakt als er filters verdwijnen en nog in de url staan. 
- De kaart altijd resultaat krijgt, ook al wordt een gebroken error gebruikt. 
- De gebruiker terug kan gaan naar zijn originele filters op de andere pagina (geschiedenis onthouden)

Hier moest ik wat voor experimenteren om het met zo’n klein mogelijke en goede aanpassingen voor elkaar te krijgen. 

Uiteindelijk heb ik hiervoor een aparte functie gemaakt. Deze functie controleert of er andere filters in zitten die de map niet kan hendelen. Deze haalt hij er zo nodig uit. Daarna geeft hij de uiState weer terug. Echter had ik wel de oude uiState nodig om de geschiedenis te behouden. Dit heb ik in de updateUrlPath functie gewijzigd. 

Ook heb ik de functie gebruikt om de uiState te cleanen zodat het niet wordt gebruikt voor gebroken filters om de map daarop te zetten. Als er bijvoorbeeld dan een alleen staande gebroken filter is dan laad de kaart niks.

Ik had er ook voor kunnen kiezen die uit de functie te verwijderen. Maar aangezien ik toch al een functie had gemaakt om deze eruit te filteren (mede om de url en geschiedenis goed te krijgen) kan ik deze ook gewoon gebruiken. 
Wel heb ik de filterblokken op de pagina uitgecomment voor het geval dat ze straks wel gaan werken. 

En ik heb comments toegevoegd. Dit leek mij wel zo netjes en handig 

![](images/codeObaFilters.png)

Halverwege mijn stage kreeg ik de opdracht om de logica van een formulier voor vista hypotheken werkend te krijgen en te verfijnen. Er was namelijk een verzoek vanuit de klant om een structuur wijziging in het formulier door te voeren, hiervoor was een vraag in het formulier nodig die drie keer genest werd en dat kon het formulier niet aan, dus moest daar nieuwe logica voor geschreven worden. Hiervoor moest ik goede oplossingen bedenken die de user experience aanzienlijk zouden verbeteren. Waar ik onder andere rekening mee moest houden was: extra lagen toevoegen aan het formulier en die velden kunnen tonen, de extra velden kunnen valideren voor onder onder andere meerdere type vragen (radios, checkboxes, text) in de diepere lagen, geneste antwoorden kunnen verwijderen als je een laag erboven iets veranderd en error meldingen voor die geneste velden kunnen laten zien. Ook moest ik rekening houden met de validatie dat als gebruikers zich bedenken, antwoorden kunnen zijn ingevuld op plekken waar dat niet moet. Deze moet ik dus tijdens het invullen van het formulier in de gaten houden en verwijderen als het nodig is. 

![](images/drieLagenDiepVista.png)

---

Door de hele stage heen heb ik aan meerdere projecten gezeten en dit betekende ook dat ik meerdere verschillende projecten lokaal heb moeten opzetten om er aan te kunnen werken. Dit ging niet altijd heel soepel en hier had ik vaak hulp bij nodig. Meer hierover heb ik beschreven onder het kopje "Opzetten projecten", te lezen in de bijlagen. Projecten moeten op bepaalde momenten ook gedeployed worden zodat het live komt te staan. Dit heb ik ook een aantal keer mogen doen voor Oba congres en de Rijke Noordzee. Na een GO van de klant mocht ik samen met een andere developer alle stappen doorlopen die nodig waren om de website op de juiste manieren volgens de standaarden van Onetribe te deployen. Meer hierover en over de versienummers van de website en de deploy stappen staan in de bijlagen onder "Git flow" en "Git flow deployment".

![](images/releaseObaCongres.png)

Maar waar ik mij het grootste deel van de stage bezig mee heb gehouden is het actief meedoen aan een groot project voor Patiëntenfederatie. Ik werd hier op gezet toen het nog vol in de design fase zat, en kwam bij meetings te zitten waar werd besproken wat voor tech stack het zou krijgen, wat de bedoeling zou zijn, wat er allemaal qua functies was verkocht en wat de prioriteit was vanuit de klant. Ook konden we ons al inlezen in het design en vragen stellen over bepaalde onzekerheden. 

Uiteindelijk kreeg ik de opdracht om de content blokken, waarmee de contentbeheerders straks zelf een pagina mee kunnen samenstellen, te templaten en te stylen volgens het design. Dit was helemaal nieuw voor mij, zeker in de tech stack die was gekozen namelijk het Craft cms met het .twig templating language en tailwind + tailgrids voor de styling. De bedoeling zou zijn dat de klant zo snel mogelijk content zou vullen zodra het mogelijk was om te gaan vullen. Pixel perfect design was dus nog niet aan de orde, dat kwam later.

Het bouwen van de blokken ging erg soepel en daar heb ik veel van geleerd. Wel bleek de keuze van tailwind en tailgrids niet de juiste te zijn geweest voor dit project. Deze tools zouden ook zijn gebruikt in figma waardoor het soepel en snel te stylen zou moeten zijn. Maar al snel kwam ik erachter dat de tailgrids components kopieren en aanpassen naar het design voor de developers niet echt handig was. De figma blokken verschilde te veel van de tailgrids blokken waardoor ik alles moest verwijderen en eigen styling moest toevoegen. Ook waren veel blokken met position absolute gestyled waardoor het niet responsive was als je elementen uit de blokken haalde. Het opzetten van de `tailwind.config` hebben we vooral gedaan met de aparte figma tabs zoals typography en colors. Maar uiteindelijk bleek dat het design van de homepagina daar niet helemaal op aansloot. Dit zorgde alsnog voor extra typografie styling op de html elementen.

Waar ik het meest van heb geleerd is de samenwerking met design in aanloop van de start van zo'n project. Ik had dit namelijk nog nooit gedaan en had dus ook niet de gedachte gehad om te kijken wat design nou precies had gemaakt. Dit leverde later wat onenigheid op dat de website nog niet pixel perfect was, en om dit te herstellen moest ik dus pixel perfect het design gaan inspecteren en hierdoor kwamen er een hoop vragen en opmerking naar boven over consistentie, welke versie nou de laatste was en over bijvoorbeeld semantiek. Uiteindelijk is dit rechtgetrokken door hier extra op te letten, drie dubbel te checken, en meetings in te plannen samen met design om door de test-linkjes heen te gaan om te kijken of ze nog afwijkende dingen zagen. 

Verder heb ik meer kunnen doen dan alleen blokken templaten en bouwen. Toen ik namelijk een beetje het Craft cms onder de knie kreeg en begreep, kon ik features toevoegen aan blokken voor UX redenen en structurele wijzigingen aan paginalayouts toebrengen om de website en straks het beheer aan de website te verbeteren. Wat belangrijke punten waren om rekening mee te houden tijdens het developen van deze website waren vooral de edge cases en het in de gaten houden van de accessibility en snelheid van de website. In dit laatste konden we makkelijk inzicht krijgen door de tool "pagespeed". Dit heb ik vaak gebruikt om de website te analyseren en te verbeteren. 

<!-- Afbeeldingen -->

---

Dit is natuurlijk een beknopte versie van wat ik allemaal heb gedaan en heb geleerd. Bepaalde overkoepelende processen die ik tijdens mijn werkzaamheden heb geleerd zoals de gitflow, het opzetten en deployen van projecten, nieuwe code environments & andere nieuwe tools kan je lezen in de bijlage. 

## Leerdoelen

  ### Samen ontwerpen

  **CMD’ers betrekken teamleden, gebruikers, domeinexperts en belanghebbenden in het ontwerp. Ze begrijpen de verhoudingen en zorgen dat iedereen zich gehoord voelt in het proces.**

  #### Mijn leerdoelen

  Wat ik wil leren en doen tijdens mijn stage dat aansluit aan de competentie “Samen ontwerpen” is meewerken aan projecten in een multidisciplinair team. Dit betekent meedoen aan stand-ups, input geven, feedback vragen en geven en bijvoorbeeld werk van andere functies te gebruiken om zo mijn taken te kunnen doen. 
  Ik ga ook vooral focussen en oefenen op communicatieve vaardigheden om de code goed over te kunnen brengen aan mensen die er niets of minder van weten dan ik. Dit helpt met mensen kunnen laten weten wat ik bijvoorbeeld heb gedaan en is bijvoorbeeld belangrijk voor klantencontact en stand ups met andere functies erbij. 

  #### Uitwerking

  Tijdens mijn stage bij Onetribe heb ik veel kunnen samenwerken met verschillende stakeholders binnen een team. Aan het begin werd ik op een project genaamd Peakz padel gezet, dat in zijn laatste development fase zat voor de officiële livegang. Wat voor mij meteen nieuw was, was het samenwerken met verschillende projectmanagers (voor development, klantcontact en contact met externe partijen), designers, backend developers, developers en lead developers. Ook begon ik hier een nieuw framework te leren en heb ik veel feedback gekregen. Aan het begin hadden we soms een standup maar naarmate het eind in zicht kwam werd dit iedere dag een standup waar de progressie even kort werd besproken. 

  Wat mijn focus was aan het begin van de stage was het focussen op de communicatie tussen mij en de project managers. Tussen de communicatie tussen developers en pmrs heb ik geleerd dat je duidelijk moet zijn over de status, recht toe recht aan in de communicatie en niet in detail treden op technische dingen. Een beetje kan wel maar niet te veel. Ook communicatie tussendoor is handig, tickets in jira goed up to date houden en meteen iets melden of vragen als je ergens tegenaan loopt waar extra informatie of dingen voor nodig zijn. 
  Ook kwam ik een aantal keer tegen iets aan in development waar een update van nodig was vanuit een externe partij. Ik ben niet degene die dit communiceert, maar aan mij is wel de taak dat de projectmanager een kloppend verhaal stuurt naar de betreffende partij. Dit heb ik onder andere gedaan voor een trengo issue bij Peakz padel (een hulptool met vragen, die niet werkte in het Duits). Maar ik heb ook een keer een bepaalde manier van iets instellen in het cms uitgelegd aan de pm'er om te kijken of dit te begrijpen was. Ook heb ik zo'n bericht moeten schrijven voor oba leef en leer, maar deze moest wel wat technischer. Dit moest namelijk doorgezet worden naar de develop omgeving bij de externe partij. Na mijn bericht 3 keer te laten reviewen door mijn bedrijfsbegeleider, kon ik hem doorzetten naar pm die het bericht zou sturen. 

  Ongeveer halverwege de stage mocht ik meewerken aan een project dat nog in de design fase zat maar alvast rustig naar de development fase ging. Hier heb ik veel meetings van bij mogen wonen. Input geven in deze meetings vond ik lastig omdat dit allemaal nieuw was en ik niet precies wist wat het proces zou zijn. Naarmate ik meer informatie kreeg en ik dit kon plaatsten, kon ik ook meer input geven en specifieke vragen stellen. Dat dit lang duurde vond ik wel jammer want dit had wel veel vragen en problemen tussen development en design kunnen verminderen in de toekomst. Er bleken namelijk wel wat haken en ogen te zitten in het proces van de designers dat moeilijkheden en onduidelijkheid zou opleveren. Namelijk bijvoorbeeld tailgrids en hoe dit werd gebruikt, versies van blokken, inconsistentie van dezelfde blokken op verschillende pagina's en soms onjuiste afmetingen uit de sidebar (de sidebar van figma als je een blok inspecteert met de waardes van de padding en margin bijvoorbeeld.)

  Halverwege kreeg ik ook feedback om meer te focussen op mijn communicatievaardigheden. Harder praten en meer input geven in meetings, meer initiatief nemen, vragen stellen en materiaal leveren om andermans werk, opdrachten of keuzes makkelijker kunnen worden gemaakt waardoor het nog fijner samenwerken is met mij.

  Door aannames van development dat design alles volgens het boekje had gedaan en dat de opdracht voor development was om eerst ruig blokken te bouwen zodat de klant het kon invullen was (en daarna zwakte dat af naar wel pixel perfect werken), was de website niet pixel perfect toen design er naar ging kijken. De opdracht voor development toen was om het recht te trekken en letterlijk screenshots over elkaar te moeten doen om er vanuit te kunnen gaan dat het pixel perfect was. Nadat ik hiermee bezig was geweest heb ik zelfstandig meetings aangemaakt met de designer om er nog een keer doorheen te gaan en het allemaal te checken. Dit heb ik voorbereid door middel van het maken van test-linkjes van pagina's waar ik dezelfde content had ingevuld in het cms als wat er in de figma stond. Dit gaf een veel beter beeld en de mogelijkheid om de meeting gestructureerd en overzichtelijk te laten verlopen. Terwijl de designer er doorheen ging had ik alle feedback punten opgeschreven en dit later gemeld aan de pm'er en verwerkt. 

  Terugblikkend op dit proces zou het veel soepeler zijn gegaan als ik dit allemaal had geweten, kon checken en kon inschatten. Maar ik heb hier in ieder geval veel van geleerd, met name met de samenwerking tussen development en design. 

  Verder heb ik tijdens mijn stage meerdere interessante meetings kunnen bijwonen zoals na elke sprint van Patientenfederatie een retrospective. Hier hebben we elkaar feedback gegeven en gekregen. Qua feedback dat ik kreeg is dat ik soms nog iets te veel elementen nest in de .twig. En dat ik de volgende blokken extra goed meteen op het design moet letten en pixel perfect moet werken. Design zelf zat niet bij deze meeting maar hierover hebben we een aantal dingen gezegd wat ons leven van de developers een stuk makkelijker kan maken volgende projecten. Zo zou het handig dat ze in figma in branches gaan werken, wat resulteert in minder design tabs. Verder is het de bedoeling dat als je een blokkendoos wilt bouwen, consistent bent in met components. En er zou een bepaalde manier zijn hoe je een blok aanpast, alle values via de values invullen en niet soms slepen. Ook zou het makkelijk zijn voor ons om een pagina te hebben me alle afmetingen en cases waarom die afmetingen kunnen verschillen. Als die logica al klaar ligt hoeven wij dit alleen te implementeren in de code en kan hier niet verder over getwist worden. En semantisch werken is ook erg op waarde gestelt, basiskennis over html en hoe het zich moet gedragen zou hier handig zijn.   

  Ook hadden de developers onder elkaar ook een meeting over hoe wij meer structuur kunnen brengen in ons werk, en zo winstgevender kunnen worden. Hier kwamen wel wat interessante punten uit zoals ons meer houden aan de gitflow, project branches omzetten naar een naam die overal wordt gebruikt, code schoon houden en aanvullen met comments. Uren inschatten om te bouwen + testen + deployen + laten reviewen. Ons meer houden aan wat er in gepland is i.p.v klusjes tussendoor en reviewen op een bepaald tijdstip waardoor je minder snel uit je flow wordt gehaald en tijd kwijt bent om het project op te starten en in te lezen in wat er gedaan zou moeten zijn. 

  ### Prototypen en uitwerken

  **CMD’ers zijn in staat om concepten vorm te geven en te concretiseren in prototypes. Ze kunnen hun ontwerp inpassen in geldende standaarden en het productportfolio van het bedrijf.**

  #### Mijn leerdoelen

  Wat ik wil leren en doen tijdens mijn stage dat aansluit aan de competentie “Prototypen en uitwerken” is meewerken aan projecten die gebruik maken van het voor mij nieuwe Vue.js/Nuxt.js framework. Hierbij pak ik issues op om bugs op te lossen en components of features te maken. 

  #### Uitwerking

  Tijdens mijn stage bij Onetribe heb ik op veel projecten mee mogen draaien op het gebied van front-end development. Om het Vue.js/Nuxt.js framework te leren heb ik mij ingelezen in het framework, een online cursus met oefeningen gedaan en daarna geholpen op het project Peakz padel waar ik bugs kon oplossen en meer inzicht te krijgen in hoe zo'n project in elkaar zit. Hier heb ik de basis van vue en nuxt goed onder de knie gekregen. (Hierover kan je meer lezen onder het "Vue.js/Nuxt.js Onetribe" kopje in de bijlagen). Op dit project heb ik goed de standaarden van het bedrijf kunnen inzien en mijn code zo kunnen schrijven dat het niet onder doet ten opzichte van andere developers. Dit is steeds verder in de stage goed te zien en ook terug te lezen in onder andere de feedbackformulieren. 

  Nadat ik de basiskennis onder de knie had, heb ik dit verder kunnen gebruiken en verdiepen in andere projecten zoals Oba leef en leer en Vista hypotheken. Hier werden de problemen en features waar ik aan kon werken steeds complexer en met behulp van veel vragen, trial en error, desk research en feedback vragen kon ik de meeste binnen de tijd goed oplossen binnen de standaarden van het bedrijf. Dit ging steeds soepeler en hierdoor kon ik steeds betere oplossingen bedenken omdat ik steeds beter wist wat er mogelijk was binnen dit framework. 

  Uiteindelijk vanaf halverwege tot het eind van de stage ben ik druk bezig geweest met Patiëntenfederatie. Hier was de tech stack anders dan in de andere projecten waaraan ik had gewerkt en kreeg ik de verantwoordelijkheid om concepten vanuit het design, en verwachtingen van de klant te concretiseren in een echte website. Ook hier weer heeft veel feedback, vragen stellen, nieuwe systemen gebruiken zoals pagespeed en browserstack mij veel geleerd over dit vak en heeft gezorgd dat ik erg ben gegroeid in deze competentie. 

  ### Evalueren

  **CMD’ers zijn in staat resultaten, die tijdens verschillende stadia van het ontwerpproces ontstaan, herhaaldelijk te toetsen op hun waarde en belang voor gebruikers, stakeholders en maatschappij.**

  #### Mijn leerdoelen

  Wat ik wil leren en doen tijdens mijn stage dat aansluit aan de competentie “Evalueren” is tijdens mijn werk steeds kritisch kijken naar mijn eigen werk en hiermee het product verbeteren of in goede kwaliteit houden. Ook wil ik issues kritisch evalueren met behulp van evaluatiemethoden en kijken hoe ikzelf en de code kan worden verbeterd. Ook wil ik feedback vragen op gemaakt werk.

  #### Uitwerking

  Tijdens mijn stage heb ik geprobeerd door het hele proces te blijven kijken naar wat er opgeleverd is en wat er nog moet worden verbeterd voor wie daar belangen bij heeft. In andere competenties lees je vooral dat ik ook kritisch ben geweest tijdens het maken van oplossingen. Maar ik heb ook aan het begin van het proces van Patiëntenfederatie kritisch gekeken naar het design om vragen en feedback te geven aan de designers. Hier kon ik semantische en algemene foutjes en inconsistentie uithalen waar ik weer naar kon vragen zodat het minder verwarring zou opleveren tijdens het developen.
  Hoe ik dit evalueerde was door middel van deskresearch door in de fimga op zoek te gaan naar afwijkende dingen. Verder kwam dit ook veel naar voren in het development proces zelf, wat weer leidde tot vragen en check-ins bij de designers.

  Nadat ik een issue heb opgelost heb ik deze stage geleerd dat je het altijd nog even moet nakijken op github in de pull-request, of je nog gekke dingen ziet. Dit voorkomt dat je sowieso een 'changes requested' status krijgt op je PR terwijl je ook zelf die fouten had kunnen weten en zien. Dit heeft mij in ieder geval erg veel geholpen om kritisch te zijn en een goed beeld te scheppen van wat ik nou allemaal had gemaakt. 

  ![](images/checkChangesGithub.png)

  Wat ik ook langzamerhand zorgvuldiger ging doen tijdens de stage was het lokaal testen (en dan vooral de vele edge cases) en als het op staging of een andere omgeving was gedeployed, dat ik het nog een keer ging testen voordat de project manager het ging bekijken en het ticket ging afronden.

  Verder heb ik tijdens het maken van issues veel vragen proberen te stellen aan mede developers als ik niet precies wist hoe of welke kant ik op zou moeten gaan. Hierdoor heb ik meer kennis opgebouwd van wat de mogelijkheden überhaupt zijn met de bepaalde technieken die werden gebruikt voor het project. Hierdoor kreeg ik het ook steeds meer onder de knie om zelf uit te kunnen vogelen wat een goede oplossing zou kunnen zijn. Maar aan het einde van mijn stage maakte ik alsnog een fout door niet goed genoeg research te hebben gedaan naar de mogelijke oplossingen. 
  Voor Patiëntenfederatie had ik namelijk een bepaald blok dat ik onderaan de pagina over de hele breedte moest vastzetten terwijl content daarboven maar half zo breed was. Ik had gezocht naar een goede oplossing maar die kon ik net zo snel vinden. Uiteindelijk had ik een manier gevonden en koos ervoor om dat bepaalde blok (als het werd gebruikt op de pagina) vast te zetten onderaan de pagina. Ik wist dat dit niet de beste oplossing was dus bleef wel zoeken naar een nieuwe. Toen ik eindelijk de mogelijkheid had om het te vragen, bleek er een veel makkelijkere optie klaar te liggen die logisch was, makkelijk te begrijpen was voor de klant, en de code netjes zou houden. Alleen had ik hem gewoon niet zelf gezien omdat ik daar niet naar had gekeken. Dit was namelijk een extra los blokje toevoegen aan de pagina in het cms waar de content beheerder zelf kan kiezen of hij het blok gaat gebruiken, en wat hij er dan in gaat zetten. Zo heeft de beheerder alsnog de vrijheid om het lees meer blok (de styling waarin het blok zou moeten worden gestyled) te gebruiken tussen de normale blokken op zo'n artikel pagina. 

  ![](images/vacatureBlock.png)

  ### Oriënteren en begrijpen

  **CMD’ers kunnen de context van het probleem, de wens van de gebruiker, doelstelling van de opdrachtgever, de belangen van belanghebbenden en de mogelijkheden van de technologie in kaart brengen en begrijpen.**

  #### Mijn leerdoelen

  Wat ik wil leren en doen tijdens mijn stage dat aansluit aan de competentie “Oriënteren en begrijpen” zijn issues met de wens van de gebruiker en doel van de opdrachtgever te begrijpen en hiervoor een passende oplossing vinden, ook als ik al een oplossing heb gevonden blijf ik kijken of er een betere is om zo de kwaliteit van het product te verbeteren en mijn kennis te vergroten. 

  #### Uitwerking

  Tijdens mijn stage heb ik aan veel projecten gewerkt waar problemen en vraagstukken naar voren kwamen die ik kon oplossen. Door goed aan de opdrachtgever en gebruiker te denken heb ik voor veel een passende oplossing bedacht in de bijbehorende techniek, en op een nette manier. Ik heb bijvoorbeeld aan het begin van de stage een probleem moeten oplossen voor Oba leef en leer. Bij een filter optie op de website lukte het niet om op bepaalde filters te filteren. De website handelde alles goed af, maar het lag juist aan de service die werd gebruikt om de gefilterde resultaten te laten zien. Die gaven namelijk geen goede url terug van de kaart met alle gefilterde locaties. Om verwarring voor de gebruiker te voorkomen heb ik in de code de betreffende filters uitgecommend (zodat dit niet opnieuw geschreven hoeft te worden door een developer), en een comment erboven toegevoegd over waarom het is uitgecommend. 

  Op deze website heb je twee pagina's waar je kan filteren met de filters. Op een pagina doet alles het wel, en op de andere pagina doet een deel het dus niet. Hiervoor heb ik nog wat aanpassingen gedaan zodat:

  - De gebruiker niet verward raakt als er filters verdwijnen en nog in de url staan. 
  - De kaart altijd resultaat krijgt, ook al wordt een gebroken error gebruikt. 
  - De gebruiker terug kan gaan naar zijn originele filters op de andere pagina (geschiedenis onthouden).

  Hier moest ik wat voor experimenteren om het met zo’n klein mogelijke en goede aanpassingen voor elkaar te krijgen. Uiteindelijk heb ik hiervoor een aparte functie gemaakt. Deze functie controleert of er andere filters in zitten die de kaart niet kan afhandelen. Deze haalt hij er zo nodig uit, en geeft de nieuwe actieve filters weer terug, maar ik heb wel de oude filters opgeslagen om de geschiedenis te behouden.
  Alles wat eerst wel werkte heb ik uitgecomment voor het geval dat ze straks wel gaan werken, en ik heb comments toegevoegd om de rare situatie duidelijk te maken.

  ![](images/codeObaFilters.png)

  ---

  Halverwege mijn stage was ik druk bezig met content blokken bouwen voor de klant Patiëntenfederatie. Op de website moest ook een slider kunnen worden geplaatst maar hiervoor was geen passend blok dat bestond in tailgrids. Na wat brainstormen en deskresearch naar een goede slider kwam ik uit op het gebruiken van scroll snap samen met Alpine.js om de knoppen werken te krijgen. 

  ![](images/pfedSliderPijlen.png)

  Na nog een keer naar het design te hebben gekeken zag ik dat op het mobiele formaat van de website er status puntjes onder moesten komen die ook als links zouden moeten kunnen functioneren. Dit probeerde ik ook te implementeren met Alpine.js maar het bleek al snel dat dat daarvoor niet echt was gemaakt. Ook werd de twig code hier erg onoverzichtelijk van. Na wat te hebben overlegd met mijn mede developer op dit project, kwamen we erachter dat het misschien wel beter was om alles om te schrijven naar normale javascript, zonder het gebruik van tailgrids of Alpine.js. Dit bleek al snel een hele goede keuze te zijn geweest. Tijdens het opnieuw bouwen van de slider kwamen er namelijk allemaal extra user experience verbeteringen in mijn hoofd op die ik met deze manier van werken meteen makkelijker kon tackelen. 
  De grootste reden dat we waren geswitched was dat je op desktop dan niet perse de knopjes zou moeten gebruiken maar ook normaal kan scrollen in de slider op desktop formaat. Ook kon ik makkelijker de gedisablede knopjes en de status van de status-puntjes op mobiel bijhouden en dit gelijk laten lopen (ook tijdens het scrollen met gestures). Verder kreeg ik het voor elkaar allebei de knoppen te disabelen als alle items in het beeld zijn. En als je naar het eind van de slider hebt gescrolled en alle laatste items al in beeld zijn, dat de knop die naar die richting zou scrollen disabled wordt. De normale en actieve kleuren aanpassen van de knoppen wanneer de achtergrondkleur hetzelfde zou zijn als een van de default kleuren. 

  ![](images/sliderDotsPfed.png)

  ![](images/afbeeldingCarouselBrand80.png)

  En met javascript werd het linken van de puntjes op mobiel naar de juiste kaart ook een heel stuk handiger. Eerst gebruikte ik html links (`<a></a>`) die achorde op de list items. die kwamen wel dan altijd aan de top van de viewport, en dit was erg lelijk en bijna niet te gebruiken. Dit kon ik oplossen door op een item die er boven zweefde te tageten maar dit gaf wel wat scroll issues. Met javascript verdwenen deze problemen allemaal meteen en kon ik gewoon `carousel.scrollLeft += scrollAmount;` en `carousel.scrollLeft -= scrollAmount;` gebruiken zonder dat er iets versprong in de viewport. 

  Hiervoor zijn we van het voorgeschreven plan en design afgestapt om de belanghebbenden te helpen met een goed functionerende feature, waar de eerder gekozen technieken niet de juiste bleken te zijn. 

  Tijdens mijn stage heb ik veel problemen kunnen oplossen en heb geprobeerd kritisch te blijven kijken naar de oplossing die ik had bedacht in de betreffende technologie. Ook is mijn kennis verbreedt qua wat er allemaal mogelijk is met de nieuwe technieken die ik aan het leren was. 

  ### Verbeelden en conceptualiseren

  **CMD’ers bedenken ideeën en ontwikkelen concepten voor digitale interactieve producten, diensten, en belevingen. Ze vinden nieuwe wegen om tegemoet te komen aan wensen van gebruikers, doelstellingen van de opdrachtgever en andere belangen.**

  #### Mijn leerdoelen

  Wat ik wil leren en doen tijdens mijn stage dat aansluit aan de competentie “Verbeelden en conceptualiseren” is om kritisch te blijven kijken naar oplossingen of problemen die zijn aangekaart in issues. Hiervoor is voor mij de uitdaging om zo goed mogelijke oplossingen te bedenken die de stakeholders ten goede komen. Dit ga ik doen door te experimenteren en gebruik te maken van andere bijpassende methodes. Ook wil ik eigen ideeën voorstellen, deze onderbouwen en voorstellen aan collega’s. 

  #### Uitwerking

  Aan het begin van mijn stage heb ik op Peakz padel gewerkt die bijna live ging. Peakz padel kreeg 2 websites, een duitse en een nederlandse. Met dezelfde codebase hoefde alleen de vertalingen nog worden toegevoegd door een vertaler. En aangezien .nl eerder live ging dan .de kwamen de vertalingen ook best laat in het proces. Dit zorgde ervoor dat er in de navigatiebalk weinig ruimte overbleef voor andere knoppen zoals je account knop door de lange duitse woorden. Belangrijk was wel dat de button het meest van zijn tekst behoudde want dit gaf juist aan of je in je account zat of dat je nog moest inloggen. Een aantal oplossingen die ik voorstelde was het gebruik van ellipsis (doorlooppuntjes), het wrappen van de navigatiebalk of woorden in de navigatiebalk als die te lang worden en of alleen de voornaam tonen in plaats van de volledige naam. 

  ![](images/loginKnopPeakz.png)

  Dit hadden we besproken in de standup en hier is een lijstje uitgekomen, maar ik mocht even kijken wat het beste en genoeg zou zijn. Het wrappen van de woorden op bepaalde breakpoints scheelde al heel veel en zag er ook niet heel verkeerd uit. Dit was ook de kern van het probleem, namelijk duitse lange woorden. Uiteindelijk is hier een combinatie ontstaan van het wrappen van woorden en ellipsis gebruik vanaf een bepaald punt voor je account button.

  ![](images/lastBreakPointPeakzDe.png)

  Halverwege mijn stage had ik dus ook de opdracht gekregen op het klantbeeldformulier op de website Vista hypotheken te verbeteren na een verzoek van de klant. Hierbij heb ik erg veel rekening gehouden met de gebruiker, maar ook met de wensen van de klant. Validatie en user experience waren daarom erg belangrijk en werden door mij voortdurend getest.

  Na vista ben ik mee gaan werken aan de website voor Patiëntenfederatie. Uit Patiëntenfederatie kwam het verzoek om ook een rss feed te maken. Deze hebben ze ook nog op hun oude website en sommige externe partijen gebruiken deze feed nog. Om hun websites niet kapot te laten gaan moest ik de rss feed zo bouwen dat het nagenoeg hetzelfde werkt, alleen dan met andere content. Ik had nog nooit een rss feed gebouwd en al zeker niet in zo'n omgeving waar de website er technisch uit ziet als een blokkendoos. Uiteindelijk kostte dit wat onderzoek door middel van deskresearch en trial and error om dit te maken en daarna wat onderzoek door middel van vergelijken om het op dezelfde manier op te zetten als de rss feed die ze al hadden. 

  In deze competentie ben ik zeker gegroeid door verschillende ideeën te bedenken en aan te bieden in een professionele omgeving waar de wens van gebruiker en klant extra meetelt. 

## Observatieopdrachten

<!--
Beschrijf kort welke observatieopdrachten je hebt
uitgevoerd. (denk aan het documentje Observatieopdrachten). Geef aan wat je hebt
geleerd en hoe dit heeft geholpen bij het behalen van je leerdoelen. 
-->

Voor de drie observatieopdrachten wilde ik onder andere stand-ups bijwonen, een livegang bijwonen en een kick-off/ start development proces van een project bijwonen. Dit is allemaal gelukt. 

### Standups

Ik heb veel standups bijgewoond waar verschillende functies bij aanwezig waren. Daarbij heb ik goed opgelet, geluisterd en input gegeven. Daarnaast vinden er ook veel gesprekken op de werkvloer plaats waar dingen worden besproken over projecten, volgende moves en statussen. Deze heb ik ook gezien, bijgewoond, en zelf gestart. Hierdoor heb ik een goed beeld gekregen over de samenwerking en communicatie op de werkvloer binnen het team en hieraan zelf ook meegedaan en zelf geoefend. Communicatie is key, je kan beter iets te veel zeggen dan te weinig. Wel is het handig om de tijd van een ander te respecteren en bijvoorbeeld meerdere vragen tegelijkertijd te stellen face to face of in de mail. Hierdoor wordt de persoon niet onnodig meerdere keren uit zijn eigen flow gehaald. 
Wat er besproken wordt in de standups is vaak of er nog meer informatie is van de klant, statussen van tickets van de developers naar de pm'ers.
Ik heb niet alleen goed opgelet tijdens standups en op de werkvloer, maar ook tijdens andere meetings. Hierdoor heb ik veel meegekregen, nieuwe dingen te weten gekomen en op nieuwe vragen gekomen die ik later kon stellen. 

### Livegang

<!-- - Ook wil ik graag een sprint voor de livegang en de livegang zelf bijwonen. Zo kan ik antwoord krijgen op hoe gaat dit in zijn werk, hoe werkt iedereen voor een bepaalde deadline, hoe gaat de communicatie tussen de klant, externe stakeholders, project managers en developers. Komen er nog veel dingen bij als je eenmaal live bent gegaan, dingen waar klanten nog op komen of niet chill vinden nadat ze live zijn gegaan.  -->

Een livegang van een bepaalde website heb ik ook zeker gezien, en zelfs zelf kunnen doen. De grootste livegang was die van peakz padel. Deze website zat in totaal al een jaar in het development traject en aan het einde is er steeds meer focus op gekomen. Dit kwam onder andere doordat er een definitieve datum was wanneer er banen kwamen in Duitsland, en voor die tijd moest de website af. Uiteindelijk is die in de 5de week van mijn stage live gegaan. Eerst Nederland (deze was het spannendst) en daarna Duitsland (dezelfde code, alleen andere content). Dit ging makkelijker dan verwacht. Voor de livegang was er nog een spoedoverleg omdat er performance issues waren (over onnodig dataverkeer). Dit zou ervoor zorgen dat de site er snel uit zou liggen als er veel bezoekers zouden komen. Uiteindelijk is ervoor gekozen om de livegang alsnog door te laten gaan en in Heroku (waar de website wordt gehost) een quick fix te doen waardoor de server scalable is en deze hoeveelheid dataverkeer dus aan kan. Dit kwam wel met een kostenplaatje van ongeveer 3500 euro per maand dus dit moest snel gefixed worden. Colin en Wiebe hadden de laatste dingen naar master gemerged. En Tim en Stef gingen het stappenplan van Job (de backenddeveloper) doorlopen om de website op productie te krijgen en te koppelen aan de DNS records. Na de livegang zaten de pm'ers op te letten of de website het goed deed en hielden contact met de klant. Ondertussen waren Colin en Wiebe de website aan het optimaliseren en ik was andere bugs aan het oplossen. Een aantal dagen later was dit allemaal opgelost en kon Duitsland live. 
Deze livegang heeft mij geleerd om tijdens het proces nauwkeurig de gegevens van de website in de gaten te houden zodat je niet voor verassingen staat als het opeens snel binnenkort live gaat.

<!-- - En het liefst zou ik een kick off van een project bijwonen, een beginnend project in kijken of de start van het development traject willen bijwonen of aan mee werken. Zo krijg ik meer inzicht over hoe het vanaf het begin in zijn werk gaat, door welke handen zulke projecten gaan voordat het live gaat.  -->

### Kickoff

Ik heb ook een kickoff van een nieuw project bij kunnen wonen. Dit project begint aan zijn development traject nadat het door de discovery, concept en (bijna) de design fase is gelopen. Deze kickoff begon met een meeting onder de developers zelf samen met een pm'er om deze dingen te bespreken:

- Het concept
- Wat het is en moet gaan worden
<!-- **=>** (15 websites naar 1 website, veel content, geen lastige styling, blokken bouwen, wel veel clickouts) -->
- Welke tech stack
<!--  **=>** Craft blokken bouwen, twig templating language, styling tailgrid, (1 tool waar vue voor wordt gebruikt (alleen ingelanden op die pagina)) -->
- Wat belangrijk is (wensen uit de klant en gebruikers)
<!-- **=>** pagespeed, accessibility en de grootste uitdaging is het goed opzetten van de craft structuur zodat het voor de klant en content beheerders het makkelijk is om overizichtelijk content te beheren.  -->
- Taak verdeling
- Planning
- Deadline
- Eerste taken
- Doelen 

Verder werd er besproken hoe ze het willen bouwen, dit kwam uit op dingen zoals craft 5, tailgrids, algolia doe ook relatief nieuw waren voor veel developers. Uiteindelijk was voor mij de taak om alvast onderzoek te doen naar Tailgrids. Hoe werkt het en wat het heeft, hoe is het gebruikt door design en hoe gaan wij het straks kunnen gebruiken. Ook heb ik vragen kunnen stellen aan Colin over Craft en Algolia waardoor ik een iets beter idee kreeg waarover werd overlegd tijdens andere meetings. Er moest namelijk een solide plan op tafel komen hoe de website gebouwd zou worden. Hier werd een excel sheet voor gemaakt met alle soorten pagina's en soorten blokken waar content beheerders straks zelf pagina's mee kunnen samenstellen, op basis van de informatiearchitectuur. Ook werd er nog gekeken of alles in het concept technisch haalbaar was, en of dingen niet misschien anders zouden kunnen om meer marge in onze uren te creëren. 
Deze fase van het project heeft mij ontzettend veel geleerd over de samenwerking tussen de teams, waar je allemaal op moet letten, wat er beproken wordt, hoe de communicatie verloopt, en heeft mij ook meer kennis gegeven over het proces.

## Analyse feedbackformulieren 

<!-- 
Maak een analyse gebaseerd op de je
functioneringsgesprek en de feedbackformulieren van halverwege en het einde van
je stage. Wat valt je op? Hoe kijk je aan het einde van de stage terug naar je stageplan
en het functioneringsgesprek halverwege? 
-->

**Midden:**

- (+) Werkt goed door, haalt veel tickets binnen het bepaalde timeframe
- (+) toont technische vaardigheden, inzet en zelfstandigheid.
- (+) houdt constant rekening met de wensen van de gebruiker en klant met betreft accessibility en ux. 
- (+) neemt initiatief, is leergierig en flexibel
- (+) bijna geen onderscheid tussen code, pr's en branching vergeleken met collega's
- (-) nog wat afwachtend op pr's, mag wel wat meer vragen of iemand bijvoorbeeld iets wil deployen of reviewen.
- (-) kan iets kritischer zijn op styling in de fijne details
- (-) iets nauwkeuriger zero en error states testen.
- (-) Mondelinge communicatie aandachtspunt
- (-) Mag soms wel wat meer naar de voorgrond treden. 

**Functioneringsgesprek:** 

- Focussen op communicatie skills waardoor het nog makkelijker en leuker wordt om met mij samen te werken. Denk bijvoorbeeld aan dingen aanleveren samen met je vraag zodat de persoon waaraan je het vraagt bijvoorbeeld alleen hoeft te kiezen, ja of nee hoeft te antwoorden, of makkelijker je vraag kan beantwoorden. En ook meer proberen in te brengen in meetings. 

**Eind:**

- (+) Houdt rekening met verschillende stakeholders
- (+) Werkt goed door, haalt veel tickets binnen het bepaalde timeframe
- (+) Neemt initiatief met het aandragen van verbeterpunten
- (+) Kan goed zelfstandig werken, secuur en technisch bekwaamd genoeg voor technische tickets
- (+) Constructief en duidelijk gecommuniceerd -> collega's, standups, klanten 
- (+) aanvulling op het team
- (+) Haalt input waar nodig
- (-) opmerkingen in tickets waren soms een beetje onduidelijk.
- (-) iets te weinig naar voren treden in de vergaderingen.

### Wat valt je op?

Wat mij opvalt is dat ik nog zeker wel wat verbeterpunten had halverwege en dat het erg verminderd is richting het einde. Je ziet dat heb gefocust op het achterna gaan van mijn pr's en vragen waar nodig als ik iets nodig had. Ook heb ik geprobeerd kritischer te gaan kijken naar de zero en error states en gedetailleerde styling van blokken. En heb ik geprobeerd mijn mondelinge communicatie te verbeteren. Het enige wat bij beide feedback punten en het functioneringsgesprek nog naar voren kwam is het naar de voorgrond treden in meetings. Hier ben ik mij ook bewust van en staat nog steeds op mijn lijstje om te verbeteren. 

#### Hoe kijk je aan het einde van de stage terug naar je stageplan en het functioneringsgesprek halverwege?

Als ik zo terugkijk naar mijn stageplan heb ik denk ik best realistische leerdoelen geformuleerd die specifiek waren maar ook ruimte toelieten voor onvoorziene omstandigheden waarvan ik ook veel kon leren. Je weet namelijk nooit wat je precies allemaal gaat tegenkomen en doen op zo'n stage waardoor het extra lastig is om specifieke leerdoelen te stellen. Een groot leerdoel wat wel steeds terug kwam in de feedbackformulieren en het functioneringsgesprek waren de communicatieve vaardigheden. De mondelinge communicatie, communicatie naar collega's met weinig verstand van code, behulpzame communicatie om de andere partij minder te belasten en te helpen om jou te kunnen helpen en het naar voren treden naar de voorgrond op de werkvloer en meetings horen daar allemaal bij. 
Hier ben ik zeker in gegroeid, ik weet nu hoe ik bepaalde situaties moet aanpakken en als ik hier nog een tikje extra aandacht aan geef gaat het meeste gewoon goed. Het enige waar ik vooral nog tegenaan loop is het naar voren treden in meetings, maar hier vertel ik meer over in de reflectie. 

## Reflectie

Wat goed ging of zelfs beter dan verwacht was voornamelijk het leren van nieuwe systemen en programmeertalen, het kritisch kijken naar wat ik oplever, inleven in klant en gebruiker qua wat zij verwachten en zullen gaan begrijpen. Wat ik anders had willen aanpakken deze stage is denk ik toch wel iets eerder dingen vragen. Ik heb soms gemerkt dat ik iets te vaak in een probleem vast bijt terwijl er een developer in de buurt is die vaak snel het antwoord wel weet. Maar dit geldt ook voor meetings als ik bijvoorbeeld iets niet snap. 

Mijn grootste kwaliteit is dat ik zeer kritisch blijf op wat ik oplever, door zoek naar betere oplossingen en andere manieren en hiervan blijf leren. Dit kan negatieve gevolgen hebben, maar hierdoor werk ik wel erg secuur en dit komt vaak het product ten goede. Andere kwaliteiten die ik deze stage zag terugkomen zijn bijvoorbeeld dat ik fouten durf te maken, vragen te stellen en feedback te vragen en hier snel van leer. Mijn grootste beperking is toch nog wel mijn communicatie vaardigheden. Normale communicatie face to face of via chats gaat gewoon goed, maar in gesprekken met grotere groepen heb ik vaak nog moeite om er tussen te komen. Ik ben een hele rustige jongen die veel en goed kan nadenken maar het omzetten naar woorden gaat soms nog wat stroef en langzamer dan de rest. Hierdoor verlies ik vaak de kans om mijn mond open te kunnen trekken terwijl ik dat wel wil, omdat dit gewoon simpelweg te lang duurt. Het maakt het natuurlijk ook een stuk makkelijker als je het onderwerp waarover wordt gesproken goed kan plaatsen in de context. Tijdens de stage ben ik hier wel beter in geworden, heb ik dit vaak kunnen laten zien tijdens standups en soms tijdens development en design meetings. Maar dit heeft gewoon simpelweg meer tijd en oefening nodig dan ik had tijdens mijn stage. 
Wat ik wel heb kunnen verbeteren aan mijn communicatie vaardigheden is dat ik nu beter kan communiceren met functies die weinig afweten van code, en ik probeer het makkelijker voor mensen te maken als ik iets van ze nodig heb. Dit kan feedback zijn of bijvoorbeeld een vraag over welke richting ik op moet gaan. Dit laatste was een feedbackpunt vanuit mijn functioneringsgesprek en heb ik bijvoorbeeld kunnen laten zien tijdens een feedbackronde met een designer waar ik test-linkjes voor had gemaakt.

Tijdens mijn eerste stage zat ik bij een klein bedrijf waar je met z'n allen zogenaamd in een woonkamer zat te werken. Tijdens deze stage wilde ik juist een ander soort bedrijf vinden, eentje die groter zou zijn met veel meer verschillende afdelingen en functies bij elkaar. Deze keuze heeft mijn beroepsperspectief aanzienlijk verbreed. Dit gaf mij niet alleen inzicht in hoe grotere bedrijven in elkaar zitten maar ook de kans om aan meerdere projecten mee te kunnen werken. Ik kon actief meedoen aan meerdere fases van grotere projecten, en vaak deelnemen aan veelzijdige meetings met veel verschillende expertises bij elkaar. Dit allemaal heeft ook mijn kennis over projectmanagement en samenwerking vergroot. 

## Bijlagen

<!-- 
- Je stageplan
- Alle feedbackformulieren, dus die van het tussentijdse gesprek en die van het eindgesprek
- Eventueel in detail beschreven (deel)producten die je hebt gemaakt.
- Eventuele andere verslagen van vergaderingen, interviews, observaties of anderszins
- relevante stukken. Omvang: ca. 20-25 pagina’s exclusief de bijlagen. Let op dat je beknopt en bondig schrijft en maak goed onderscheid tussen wat bij je verslag hoort en wat een bijlage is.

(Een bijlage is een aanhangsel aan het originele werk waarin je informatie vindt die
ondersteunend is maar in de hoofdtekst te veel zou afleiden.)
-->

 ### Git flow

  Om de versie beheer goed inzichtelijk te houden maken ze gebruik van git flow.
  Je zet `feature/`, `hotfix/` of `release/` voor de titel van je branch als je die cloned en de titel van je commit is eigenlijk vaak ook je issue nummer. Welke het meest wordt gebruikt is `feature/`.
  Voor de semantic release (het versienummer van je project die je automatisch kan updaten aan de hand van hoe je je commits opbouwt) moet je je commits beginnen met chore:, fix:, feature: of perf:. 
  voorbeelden:

  ![Git flow](images/gitflow.png)

  > Bron: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow 

  Ook zei Raoul dat niet iedereen zich aan de standaard van git flow houdt en vind dat je je gewoon aan de standaard moet houden en niet dingen er bij moet verzinnen die je dan eerst weer moet uitleggen. 

 #### Git flow deployment 

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

  De eerste stap was dus het aanmaken van een nieuwe versie tag door middel van semantic release, alleen dan handmatig. Daarna maakte Raoul een backup van de database, dit is belangrijk voor als de deployment fout gaat, dan kan je het namelijk altijd terug zetten. Nieuwe env's hadden we niet. PR hadden we ook gemaakt. We hadden geen nieuwe Node versie dus die konden we ook overslaan. Daarna heeft Raoul de `develop` branch gedeployed in BuddyWorks. 
  Terwijl het aan het deployen was liet Raoul mij Cypress zien waarmee je met bepaalde scripts heel snel websites (vooral de basis functionaliteiten zoals of zoeken werkt en of je geen lege lijst krijgt bij een bepaalde pagina) kan testen. Hij raadde mij dit wel aan om in te duiken. 
  Daarna was het geployed en konden wij `develop` naar `master` mergen. Daarna moesten we nog een backmerge doen van `master` naar `develop` om 100% zeker te zijn dat alle changes die in master zitten ook in develop zitten (denk aan hotfixes of iets dat nog niet is gemerged naar develop). 

  Na de deploy even gekeken of het allemaal goed werkte op productie, daarna weer doorgegeven aan Lars. 

  Content kon ik al toevoegen maar aangezien de klant juist de optie wilde om daar een video te plaatsen heb ik dat niet gedaan, Lars uiteindelijk wel. 

  Ook had ik een GO gekregen om oba-congres op productie te zetten. Hier heb ik een pr voor aangemaakt van `develop` naar `master`, en nadat Colin de pr goed heeft gekeurd, op buddy de deploy heeft gedraaid (Hier hoefde geen backups of iets voor gedraaid te worden aangezien het een single page website is zonder database of iets) kon ik een release aanmaken `v1.2.2`. Colin vroeg zich nog af of het niet `v1.3.0` moest zijn maar ik zei dat het in principe alleen maar content changes zijn voor de gebruiker en dit voegt verder geen extra features toe en daar was hij het mee eens. 
  <!-- [screen shots] -->

 #### Merge regel

   Bij Onetribe is er een regel dat je je eigen branch merged. Dit is een regel die bij mijn minor bij de HBO ICT het tegenovergestelde was. Daar gelde je merged meteen de branche die je hebt approved, als er iets fout is aan de changes, dan zijn jullie allebei verantwoordelijk. Aangezien degene die het approved en mergen goed had moeten testen en reviewen. 

   Bij Onetribe geld dat niet. Hier maak je een pr, deze wordt gereviewed, feedback gegeven of approved en dan mag je hem daarna zelf mergen. Dit geeft als gevolg dat de reviews niet uitermate wordt getest en vooral wordt gekeken naar de kwaliteit van de code. Wel is dit sneller qua reviewen, is alleen degene die het heeft geschreven verantwoordelijk maar geeft mogelijk wel meer kleine (over het hoofd geziene) issues later omdat 1 persoon mogelijk meer fouten maakt dan 2 mensen bij elkaar. 

   Wel is dit natuurlijk een professionele omgeving waar iedereen op een redelijk niveau codeerd en niet zoals op school waar een deel er niks van begrijpt en je juist van elkaars code ook wil leren.

 ### Code environments & andere tools

  Bij Onetribe gebruiken ze Bitbucket en Github om hun code op te slaan. Dit verschilt per project door de fusering met noProtocol. 

  - Jira -> Issue boards
  - Sentry -> Website monitoring (debug, errors)
  - Algolia -> Search
  - Dato of Craft cms -> content management system
  - Heroku -> Hosting
  - Akamai -> Cache
  - Screamingfrog -> SEO testing, (Maar voor peakz hebben ze een SEO man ingehuurd om tips te geven)
  - Extra widgets zoals FOYS of localfocus -> hiermee komt vaak de klant mee aanzetten. Hier kiest Onetribe dus niet perse voor, en hebben dus ook vaak problemen door bugs bij de andere partij.
  - Buddy.works tussen iets om websites te deployen/hosten

 ### Vue.js/Nuxt.js Onetribe

  Veel projecten maken gebruik van het Vue.js/Nuxt.js framework. Dit was helemaal nieuw voor mij dus dit was erg interessant. 
  Wat ik meteen al zag is dat dit erg component based wordt geschreven. Je hebt pages, en die bestaan uit components, en sommige components bestaan weer uit andere components. Door data door te geven en te kijken of bepaalde dingen moeten worden ingeladen als het nodig is, kun je dus met dezelfde componenten verschillende pagina's maken, zonder veel code duplication. Ook hebben deze componenten hun eigen component based styling en scripts. 
  <!-- meer voorbeelden en code hieronder -->

  Wat ik veel heb gebruikt in vue wat aansluit op de vue manier van code schrijven zijn:
  - Computed properties
  ```js
  const trueOrFalse = computed(()=> {
    return eenArray.lenght > 1;
  })

  console.log(trueOrFalse) // functie wordt uitgevoerd als je de variabele gebruikt, logt true of false
  ```

  - props doorgeven aan een component: 
  ```js
  <component
    :ditIsEenProp="trueOrFalse"
  >
  ```

  En in het component kan je dan zo de props inzien:

  ```js
    const props = {
      ditIsEenProp: boolean;
    }
    console.log(props.ditIsEenProp) // dit logt true of false
  ```

  - v-if en v-for 
  ```js
  <component
    v-if="ditIsEenProp" v-for="nestedGroup in groups"
  >
  ```

  - v-html
  - slot

  ```html
    <slot name="search-results" />
  ```

  en in het component erboven:

  ```html
    <template 
          #search-results
        >
          <ais-hits>
            <template #item="{ item }">
              <search-hits-item-learning-materials :item="item" />
            </template>
          </ais-hits>
    </template>
  ```

  Wat makkelijk hieraan is is dat je veel overzicht kan behouden in een file qua wat er allemaal in zit. Maar de logica en styling staat op het component zelf. Ook kan je op verschillende pagina's het component search-results gebruiken terwijl je er andere dingen in kan zetten per pagina. Dit scheelt logica in het component zelf. 

 ### Opzetten projecten 

  Tijdens mijn stage heb ik een hoop projecten moeten opzetten om daaraan te kunnen werken. Dit vond ik lastiger dan developen aangezien het vaak niet meteen werkt, niet alle error meldingen duidelijk zijn en je kennis nodig hebt om mogelijk te kunnen zien waar het aan ligt. Ook moet je alle stappen doorlopen en is dit niet altijd goed gedocumenteerd omdat ik vaak op edge cases terechtkom. Hier heb ik veel van geleerd, denk bijvoorbeeld aan hoe het werkt, de stappen die je moet doorlopen, errors herkennen, de benodigdheden weten (bepaalde talen, databases, lokale server). Door al dit vaak te hebben gedaan, veel hulp te hebben gekregen en vragen te stellen ging dit opzetten steeds soepeler en zelfstandiger, en snapte ik ook beter hoe die projecten in elkaar zaten. 

  De systemen die Onetribe gebruikt om servers op te zetten en databases te runnen zijn Laravel herd, DBengine en tableplus. Dit heb ik werkend kunnen krijgen met wat hulp voor het project Oba leef en leer waarvoor dit nodig was. Een tijdje later moest ik de rijke noordzee opzetten hiermee maar dat lukte niet zelfstandig. Uiteindelijk heb ik hier de hulp van Raoul voor gekregen. Maar Raoul gebruikt ddev (docker) en dat maakt twee docker containers voor de database en craft (cms). Uiteindelijk werkte dat voor de rijke noordzee maar bleek later dat laravel herd het niet meer deed, dit heb ik ook niet meer aan de praat gekregen met hulp van meerdere mensen. 

  Uiteindelijk heb ik alle projecten daarna draaiend gekregen met ddev, niet alleen, vaak met hulp. Dit kwam omdat ik dan tegen errors kwam waarvan ik niet wist hoe ik die kon oplossen. Hierdoor heb ik de stappen en benodigdheden vaak kunnen observeren en onthouden. En uiteindelijk had ik geen hulp meer nodig. De dingen waar ik op moet letten als ik een project op start zijn:

  - Alles in de env moet goed staan.
  - Craft moet eerst runnen want anders kan je de fe niet builden want nuxt voert queries uit om te kijken of alles kan wat die wilt doen en als dat niet kan gaat er iets niet goed. 
  - Je moet een database krijgen van je collega's anders kan de code niks vinden. 

  <!-- verdere feitjes: Nuxt draait op localhost nadat die is gebuild. 
  Craft kan headless maar hoeft niet. Headless: draait op een andere server. Kunnen elkaar wel bereiken, andere url. -->

  <!-- // TODO [Tekening maken] -->

  **Plug-in installeren in craft (cms)**

  Uiteindelijk moest ik een andere dag een plugin installeren in craft. Deze plugin zou moeten zorgen voor extra beveiliging wanneer je een wachtwoord aanmaakt. 
  Het project draaide al lokaal en na de documentatie te lezen probeerde ik de plugin te installeren. Dit lukte niet in een keer, ik wist niet precies waar ik het commando moest draaien en ik had wat database connection errors. Na een poos de containers uit docker uit te hebben gezet en weer aan te hebben gezet deed het commando het opeens wel. Dit had ik gepushed, maar zag dat niet alle files nodig waren om te committen. Ik had wat changes verwijderd maar raakte verstrikt tussen de verschillende versies van mijn branch en craft, ook na het opnieuw bouwen van het cms en de yaml files gelijk trekken zeurde het cms over changes die waren gemaakt in de database. Dat betekende maar een ding en dat was het project nuken en opnieuw bouwen. 
  Dit was een goede oefening om weer het proces van een project opzetten te doorlopen en het lukte meteen. Mijn stappen waren dit:

  ```
  $ make nuke
  $ ddev import-db --file=./oba-leef-en-leef.sql #importeer de database die ik aan het begin van de stage had gekregen. Deze heeft nog niet de changes van mijn geinstalleerde plugin. 
  $ ddev . make build-cms # bouw het cms in een docker container
  $ make build-web # bouw de front-end
  $ make run # host de front-end op localhost (geen docker container)
  ```

  Nadat het project opnieuw was gebouwd, checkte ik of de plugin in craft stond. Dit was niet het geval en kon ik dus weer opnieuw installeren. Om de database altijd te bereiken moest ik de host van mijn database uitgebreider opschrijven. Dus het werd niet `DB_DSN="mysql:host=db;port=3306;dbname=db"` maar `DB_DSN="mysql:host=127.0.0.1:3306;port=3306;dbname=db"`

  Dit kon ik zien door `ddev status` te draaien in de terminal want daar stonden dit soort gegevens. 

  Installatie van de plugin:

  ```
  $ cd cms
  $ ddev composer require "born05/craft-enforcepassword:^2.0.0" -w && ddev craft plugin/install enforce-password
  ```

  Dit lukte allemaal en installeerde alleen de benodigde files. Daarna heb ik nog een enforce-password.php file aangemaakt om de criteria van een nieuw wachtwoord te benoemen en zo nodig aan te passen. Colin wilde niet dat het wachtwoord na een aantal dagen zou expireren dus die hebben we op 0 gezet. En verder wordt alleen het laatste wachtwoord opgeslagen i.p.v de laatste vijf. Dit heb ik getest en het werkte. 

  ```
  $ ddev craft users/create --admin 
  Email: testtest@test.com
  Username: jopadmin
  Set a password for this user? (yes|no) [no]:yes
  Password: 
  Password should be at least 16 characters.
  ```

  **Andere projecten**

  Alle projecten die ik daarna heb opgestart gingen veel vlotter dan daarvoor. Het meeste waar ik nog tegenaan liep was dat de `.env` variabelen niet goed stonden. Hier heb ik de andere keren extra op gelet en naar gekeken. Zo was er bijvoorbeeld redis toegevoegd door de backend developer in het patienten federatie project die ik al draaiend had gekregen op mijn computer. Maar de nieuwe changes zorgde ervoor dat het het niet meer deed. Na wat research en de error meldingen te hebben gelezen kwam ik er achter welke variabelen en files ik miste. Dit waren de `docker-compose.redis.yaml` (die stond in de `.gitignore`), de redis variabelen in de `.env` en ik moest redis op mijn computer nog installeren. Na wat experimenteren zorgde `REDIS_HOST=host.docker.internal` in de .env er uiteindelijk voor dat de redis DB connectie geopend kon worden.   