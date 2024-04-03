# Min kodplugg till Anytone OpenGD77

## Copyright

© 2019-2024 by SM0RUX Pontus Falk

Filerna är tillgängliga under [GPLv3](https://github.com/sm0rux/opengd77/blob/master/LICENSE).

## Uppdatering av SM0RGM 

På grund av att Pontus SM0RUX av personliga skäl inte har möjlighet att uppdatera kodpluggen så har han och jag kommit överens om att jag övertar och uppdaterar kodpluggen. Kodpluggen är och förblir därmed "SM0RUX kodplugg" men underhållen av mig. Jag har skapat en fork av kodpluggarna och publicerat under mitt eget Github-konto och ändrat kontaktytorna i dessa filer, så kommentarer, ändringar och liknande lägger du som en issue på min Github eller kontaktar mig.

Även om man försöker vara minutiöst noggrann så kan det smyga sig in fel. Kodpluggen innehåller i denna version runt 600 kanaler. Så hittar du något fel eller har andra synpunkter, lägga gärna en issue eller skicka ett mail. 

Nacka februari 2024
SM0RGM Stefan Helander

## Syfte

Det här är min kodplugg till min OpenGD77. Den är skapad utifrån den kodplugg som vi har tillhandahållit sedan ett antal år tillbaka. Eftersom ingen av oss äger en GD77 är vi beroende av synpunkter och rapporter från dig som använder den. 
Huvudsyftet med publiceringen av filerna här på GitHub är att förenkla för mig själv när det gäller uppdateringar. Jag har inget emot att dela med mig av filerna så att andra kan nyttja dem under förutsättning att de som återanvänder mina filer följer licensvillkoren i [GPLv3](https://github.com/sm0rux/opengd77/blob/master/LICENSE).

Om du vill bidra med något så är du naturligtvis välkommen att göra så antingen genom att skapa en Pull Request (kräver en del kunskap om hur GitHub funkar) eller genom att skapa ett [issue](https://github.com/sm0rgm/opengd77/issues).

## Vad ingår i filerna?

Alla repeatrar i Sverige som kan köra DMR eller FM är inkluderade (källa: [sk6ba.se](https://sk6ba.se/repeater/karta/)). Även repeatrar som kör exempelvis C4FM och FM finns med. Repeatrarna är indelade distriksvis. Tyvärr finns det så många repeatrar i sjätte och sjunde distrikten att alla inte får plats i scanning-listan (Anytone).

### Vad ändras vid konverteringen från Anytone till OpenGD77?

Vid konverteringen från Anytone till OpenGD77 så finns vissa begränsningar som man behöver ta hänsyn till.

* TG List i GD77 (motsvaras av Receive Group List i Anytone) är begränsad till 32 talgrupper så vi har valt de vanligaste i OpenGD77-versioner.
* Anytone har stöd för kanaler med både Analog och Digital sändning. I OpenGD77 kan en kanal vara antingen Analog eller Digital. Därför har vi konverterat dessa kanaler så här:
    * Anytone A+D TX A -> GD77 Analog
    * Anytone D+A TX D -> GD77 Digital

### Vilka filer ska du hämta?

Jag rekommenderar att du hämtar filerna som jag har packat ihop i en [release](https://github.com/sm0rgm/opengd77/releases) istället för att hämta mina arbetsfiler!

### När filerna är hämtade... 

CSV-filerna kan du använda om du har en befintlig radio eller kodplugg som du vill uppdatera med kanaler, zoner, talgrupper etc. 

Om du snabbt och enkelt vill starta en ny kodplugg eller koda upp en ny radio så finns det en färdig fil med alla inställningar gjorda som heter N0CALL.g77.

Starta CPS-programmet och välj File -> Open och välj N0CALL.g77. Gå till fliken DMR ID and callsign och ändra Callsign och dina egna. Sedan är det bara att skjuta i kodpluggen i radion (välj COM-port och sedan Write to radio).

Sedan vill du antagligen också gå till Extras -> Download callsign database och ladda ner callsigns från [radioid.net](https://radioid.net) för i alla fall region 240. Vill du ha fler regioner kan du gå till radioid.net, skapa ett konto och generera en kontaktlista över de regioner du önskar och instället importera dem med Import CSV.

Förmodligen vill du ändra på fler saker, men det överlåter jag till dig att fixa med själv.

### Uppdatera befintlig kodplugg

Om du bara vill uppdatera din radio med kanaler, zoner och talgrupper men låta resterande inställning vara som de är kan du, istället öppna din befintliga kodplugg i CPS och sedan gå till File -> CSV -> Import CSV och välj sedan mappen CSV. 
73's de SM0RUX Pontus / SM0RGM Stefan

2024-04-03

