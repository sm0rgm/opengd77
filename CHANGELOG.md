# Changelog

## 2025-05-xx (SM0RGM)

* Anpassad för CPS/FW R2025.03.23.01

## 2025-05-04 (SM0RGM)

* Ändrade kanaler per zon:
    * Simplex
        * +APRS ISS 145.825 MHz FM

## 2025-03-09 (SM0RGM)

SM0RUX/Pontus är silent key. Tänk gärna på Cancerfonden tel. 010-199 10 10

## 2024-10-04 (SM0RGM)

* Ändrade kanaler per zon:
    * SM0
        * +Haninge 4 434.6375 MHz SK0NN-2

## 2024-04-15 (SM0RGM)

Release som "BETA 4". Ändringar:

* Alla kanaler har nu effektläge "Master" utom kanalerna för hotspots.
* Latitude och Longitude hämtade för de flesta repeatrar från SK6BA.
* APRS 1, APRS 2 och APRS US har nu APRS1 aktiverad.
* För radioapparater som har stöd för teman finns nu temat SM0RGM.gtm.

## 2024-04-07 (SM0RGM)

Release som "BETA 3". Ändringar:

* Effektlägen följer nu kodpluggen till Anytone:
    * Low -> P1
    * Mid -> P3
    * High -> P5
    * Turbo -> P9
* TG list = Default, Contact = None för alla kanaler (man kan antingen ha TG List eller Contact vald, inte både och)
* TalkerAlias = Text för både TS1 och TS2 för samtliga digitala kanaler (hämtar Line 1 och Line från Boot screen).
* Longitude och Latitude satt till 0 och 0 för samtliga kanaler för att förhindra att radion rapporterar avstånd till repeatern (i framtida versioner kommer verkliga positioner att läggas in för repeatrar om dessa är kända).
* Brottby 2 434.800 FM 77 Hz subton

Stort tack till SA0BUX Lars och SM0IKR Göran för tester, synpunkter, tips och rapporter.

## 2024-04-06 (SM0RGM)

Release som "BETA 2".

* Boot screen -> Line 1 satt till N0CALL och Line 2 till Myname då dessa används som Talker Alias

## 2024-04-05 (SM0RGM)

Release som "BETA 1"

## 2024-04-03 (SM0RGM)

Första version för OpenGD77.

