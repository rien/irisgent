---
layout: post
title: Generieke (DMR) Radio Setup
---

Er bestaat reeds een [blogpost over hoe je een AnyTone AT-D878UV](/2020/04/17/Guide-Anytone/) kunt instellen met _codeplugs_ en _DMR_ radio. Maar omdat er steeds meer leden zullen zijn met exotische andere radio's condenseer ik hier wat generieke informatie over DMR. Zo kun je, onafhankelijk van het model van je radio, toch proberen om de juiste instellingen te vinden om je eerste QSO te maken over DMR.

Eerst geef ik een korte introductie tot DMR, maar als je dat al weet kun je [springen naar de setup](Je radio instellen).

# Wat is DMR?

**D**igital **M**obile **R**adio is een digitale manier om met andere operators te communiceren. Waar dat analoge radio een relatief primitieve modulatie zoals FM gaat gebruiken, gaat DMR geluid doorsturen in digitale vorm. Heel gelijkaardig aan de muziekradio is DMR een beetje zoals de DAB+ in vergelijking met de klassieke FM-radio. Het heeft ook dezelfde voor- en nadelen: als je elkaar ontvangt zat dat in goede kwaliteit zijn. Maar wanneer het signaal te zwakt wordt hoor je elkaar helemaal niet meer, waar bij analoge radio de tegenpartij zware ruis zou hebben.

Het voordeel van DMR is dat deze genetwerkt is. Er staan overal in België (en de wereld) **repeaters** die de digitale signalen gaan ontvangen en kunnen doorsturen naar andere repeaters via het internet. Zo kun je de repeater in Gent ([ON0GRC](https://brandmeister.network/?page=repeater&id=206101)) een QSO'tje maken met iemand die verbonden is met de [W6GRC](https://brandmeister.network/?page=repeater&id=310709) repeater in Californië in de VS. Dat allemaal met je 5 Watt portabeltje.

Maar om dat te kunnen doen moet je enkele achterliggend concepten begrijpen:

## DMR ID

Een DMR ID is een identificatienummer die gekoppeld is aan een operator. Het is een soort telefoonnummer of IP-nummer waarop je te bereiken bent. Die heb je nodig om DMR te kunnen gebruiken, maar kun je vrij gemakkelijk aanvragen (als je een bedieningsvergunning en een callsign hebt tenminste) op de [registratiesite](https://register.ham-digital.org/).

## Praatgroepen

Praatgroepen of **T**alking **G**roups, is de voornaamste manier om DMR radio te gebruiken. Je kunt het zien als een groepsgesprek waar andere operatoren naar kunnen gaan luisteren of kunnen versturen. Een praatgroep heeft ook een DMR-id, die van Iris is 2060253.

Wanneer een praatgroep actief is op een repeater, dan zal die repeater alles wat die ontvangt gaan doorsturen naar andere repeaters waarop die praatgroep actief is Ook alles wat binnen die praatgroep gezegd wordt op andere repeaters wordt terug uitgezonden door die repeater. Zo kan iedereen met de dichtste repeater verbinden, maar toch binnen eenzelfde praatgroep met elkaar communiceren.

DMR ondersteund twee simultane verbindingen tegelijkertijd, door middel van [TDMA](https://en.wikipedia.org/wiki/Time_division_multiple_access). Hierdoor kunnen er twee praatgroepen actief zijn op dezelfde repeater. Meestal is dat één van die slots vast en de andere dynamisch. Dat wil zeggend dat je op die dynamische timeslot kunt uitzenden en dat je dan dat timeslot eventjes claimt voor die praatgroep. Wanneer er eventjes (10 minuten) niets gezegd is geweest dan wordt die timeslot weer vrijgegeven.

## Het BrandMeister netwerk

[BrandMeister](https://brandmeister.network/) hét DMR-netwerk waarop de meeste repeaters aangesloten zijn. Je kunt er zoeken op repeaters en je kunt er een historiek van gesprekken zien.

# Je radio instellen

Wat de precieze instellingen van je radio zijn om met DMR te kunnen omgaan dat verschilt natuurlijk van radio tot radio. Maar hieronder volgt een generieke uitleg die je wel op weg zou moeten helpen (in combinatie met de meegeleverde handleiding en wat youtube-tutorials). Niet alle radio's kunnen ook DMR aan (ondergetekende heeft moeten een goedkope analoge radio inwisselen voor een iets minder goedkope DMR-capable radio).

## Codeplugs

De instellingen van je radio (op welke frequenties repeaters zitten, met welke offset etc.) kun je meestal met een programma inladen op je computer, opslaan, aanpassen en terug opladen naar je radio. Deze bestandjes noemt men _codeplugs_. Het is handig om die bij te houden als backup of om te delen met andere operatoren met dezelfde radio. Meestal is het ook net iets aangenamer om die instellingen in te geven op een computer dan op een klein LCD-schermpje.

## Je DMR ID instellen

Om jezelf identificeerbaar te maken moet je eerst je DMR ID instellen in je radio. Dit zit waarschijnlijk ergens in een menutje. Als je niet kunt vinden waar dan kan het zijn dat je dat via software moet doen.

## Contacten bijhouden

Een radio heeft meestal een contactenboek. Hierin kun je een DMR id van een operator of talkgroup opslaan met een zelfgekozen alias.

## Kanalen aanpassen

Daarnaast kun je ook kanalen gaan bijhouden. Een kanaal kun je zien als een instelling van de radio zelf: op welke frequentie moet er geluisterd en uitgezonden worden, welke modulatie, welk timeslot, etc. Je kunt bijvoorbeeld een kanaal 'IRIS Vriendenronde' hebben waar je instellingen direct juist staan om mee te doen met onze vriendenronde (analoog RX/TX op 145.1337 MHz), of je kunt een kanaal maken voor een specifieke repeater.

Hier even een voorbeeld hoe je zo'n kanaal op je radio zou instellen voor de [ON0GRC](https://brandmeister.network/?page=repeater&id=206101) repeater in Gent:
- **RX frequency** dit is de frequentie waarop je luistert naar de repeater, dit moet overeenkomen met de **TX frequency** van de repeater. In dit geval dus **439.0875 MHz**
- **TX frequency** dit is de frequentie waarop je stuurt naar de repeater, dit moet overeenkomen met de **RX frequency** van de repeater. In dit geval dus **431.4875 MHz**
- **Color Code** dit is meestal **1**.
- **Time Slot** dit is het timeslot die je wilt gaan gebruiken. Momenteel gebruiken wij het dynamische timeslot **2**.
- Tot slot is er nog een manier nodig om een praatgroep (**TG**) te koppelen aan een kanaal. Dit verschilt enorm per radio en kun je soms enkel via software op je PC instellen. Een specifieke handleiding voor je repeater kan je hier op weg helpen.

Eens je een kanaal hebt aangemaakt kun je die eens uittesten. Als je even kort op de PTT-knop van je radio drukt kun je vaak al op je scherm zien of dat lukt of niet. Op de BrandMeister site van de repeater kun je ook bij 'Last Heard' zien of je oproep is binnengekomen of niet. Is dat niet het geval dan loont het de moeite om eens de **RX** of **TX** frequency om te draaien.

## Troubleshooting

Mogelijke oorzaken waarom DMR niet zou werken:

- Je squelch (**SQL**) staat te hoog.
- Je hebt de **RX** en **TX** frequenties omgewisseld.
- De informatie over een repeater die je online hebt gevonden is outdated.
- Je hebt de DMR id van de praatgroep verkeerd ingesteld.
- Het dynamisch tijdsslot van de repeater is bezet waardoor je niet via die praatgroep kunt praten. Je kunt altijd proberen de praatgroep van het statische tijdsslot in te stellen om te kijken of DMR daar werkt.

Het kan ook helpen om je radio op **monitor** modus te zetten. In DMR modus zal dit meestal alle digitale communicatie gaan beluisteren (en wordt er dus niet enkel geluisterd naar de ingestelde **TG**). Als je daar mensen hoort op prate van je **TG**, dan staat die **TG** niet goed ingesteld op jouw radio.

Wat je ook altijd kunt proberen is met een SDR gaan kijken of je je radio ziet uitzenden (en of je de repeater af en toe kunt horen). Als je radio heel kort uitzend dan wil dat zeggen dat die geen ontvanger vindt (m.a.w. de repeater zit op een andere frequentie).

# Tot slot

DMR is een prachtige manier om andere operatoren te bereiken met een kleine handheld device. Zolang er een repeater in de buurt is kun je de hele wereld bereiken!

Maar het kan toch wel wat tijd innemen om je radio juist in te stellen. Repeaters in je buurt vinden en die aan de praat krijgen kan heus monnikenwerk zijn. Vergeet niet om plezier te blijven hebben in je hobby, en als het niet direct lukt kun je altijd om raad vragen bij Iris-leden of op de Iris **TG**.

o7

Rien - ON3EEE
