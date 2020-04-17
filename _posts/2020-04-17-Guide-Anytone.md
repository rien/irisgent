---
layout: post
title: Setup AnyTone AT-D878UV
---

Een korte setupguide voor de AnyTone AT-D878UV, hierin bespreek ik een paar van mijn ondervindingen.

# Benodigdheden

- *Een AnyTone AT-D878UV.*
- Een computer die Windows draait (met spijt in ons hart).

# Updaten

## Firmware downloaden

Een van de site die de meeste softwareversies aanbiedt, is [http://www.wouxun.us/category.php?category_id=93](http://www.wouxun.us/category.php?category_id=93),
deze bevat zowel de oudere als nieuwste software.

## Baseband updaten
Deze stap en de volgende kunnen worden omgewisseld.
De eerste stap is controleren wat je huidige softwareversie is. Dit kan je controleren op het apparaat onder `Menu > Settings > Device Settings`. Als deze hoger is dan 1.13, kan je deze stap overslaan. Indien dit niet het geval is, dan download je de software versie 1.14 en installeer je het meegeleverde `Base Band IC 3258 update/SetupSCT_PORT.msi`-programma. De meegeleverde guide bevat de exacte instructies. Als deze update is voltooid, kan je doorgaan naar de volgende stap.

## Firmware updaten

Firmware kan je direct updaten naar de nieuwste versie, op het moment van schrijven is dit 1.18. Download de software en installeer het meegeleverde CPS-programma (dit is anders voor elke versie en moet dus per versie geïnstalleerd worden). De map `D878UV_V1.18 FW` bevat dan de firmware en instructies hoe deze te installeren. Als dit gelukt is, kan je de portable beginnen installeren.

# Instellen portable

Voor het instellen van de portable raden we aan om van een bestaande codeplug te vertrekken. [Dit](/public/files/iris_codeplug.rdt) is mijn persoonlijke codeplug, deze kan je via de CPS uploaden naar je portable. Deze codeplug bevat repeaters, talkgroups en digitale contacten al reeds voorgeprogrammeerd. Het enige dat je moet doen voor het wegschrijven naar de portable is onder `Digital > Radio ID List` je DMR-ID in de lijst zetten. Zo'n ID kan je aanvragen op [https://register.ham-digital.org/](https://register.ham-digital.org/). Het kan wel een dag duren vooraleer deze in het systeem zit en dus vlot werkt. Om een DMR-ID aan te vragen heb je enkel een bedieningslicentie nodig. De contactenlijst update je ook best zodat de nieuwste DMR-ID's er ook inzitten. Dit kan je doen door de csv die je [hier](https://www.radioid.net/database/dumps) kan vinden te importeren in de CPS-codeplug.

Nu is je portable gebruiksklaar!

Verder configureren kan via de software of op het apparaat zelf. Bij problemen is [http://members.optuszoo.com.au/jason.reilly1/868mods.htm](http://members.optuszoo.com.au/jason.reilly1/868mods.htm) een goede bron van hulp.

Nu je portable werkt, horen we je graag op onze vriendenronde!

ON3DOT<br>Francis