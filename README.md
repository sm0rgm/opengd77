# Min kodplugg till OpenGD77

## Copyright

© 2019-2024 by SM0RUX Pontus Falk

Filerna är tillgängliga under [GPLv3](https://github.com/sm0rux/opengd77/blob/master/LICENSE).

## Uppdatering av SM0RGM 

På grund av att Pontus SM0RUX av personliga skäl inte har möjlighet att uppdatera kodpluggen så har han och jag kommit överens om att jag övertar och uppdaterar kodpluggen. Kodpluggen är och förblir därmed "SM0RUX kodplugg" men underhållen av mig. Jag har skapat en fork av kodpluggarna och publicerat under mitt eget Github-konto och ändrat kontaktytorna i dessa filer, så kommentarer, ändringar och liknande lägger du som en issue på min Github eller kontaktar mig.

Även om man försöker vara minutiöst noggrann så kan det smyga sig in fel. Kodpluggen innehåller i denna version runt 600 kanaler. Så hittar du något fel eller har andra synpunkter, lägga gärna en issue eller skicka ett mail. 

Nacka februari 2024
SM0RGM Stefan Helander

## Syfte

Det här är en konverterad version av Pontus/SM0RUX kodplugg för Anytone AT-D878UV till OpenGD77. Kodpluggen till Anytone AT-D878UV underhålls och uppdateras av mig (SM0RGM) sedan en tid tillbaka. Eftersom ingen av oss äger en radio med OpenGD77 är vi beroende av synpunkter och rapporter från dig som använder den. 
Huvudsyftet med publiceringen av filerna här på GitHub är att förenkla för mig själv när det gäller uppdateringar. Jag har inget emot att dela med mig av filerna så att andra kan nyttja dem under förutsättning att de som återanvänder mina filer följer licensvillkoren i [GPLv3](https://github.com/sm0rux/opengd77/blob/master/LICENSE).

Om du vill bidra med något så är du naturligtvis välkommen att göra så antingen genom att skapa en Pull Request (kräver en del kunskap om hur GitHub funkar) eller genom att skapa ett [issue](https://github.com/sm0rgm/opengd77/issues).

## Vad ingår i filerna?

Alla repeatrar i Sverige som kan köra DMR eller FM är inkluderade (källa: [sk6ba.se](https://sk6ba.se/repeater/karta/)). Även repeatrar som kör exempelvis C4FM och FM finns med. Repeatrarna är indelade distriksvis. Tyvärr finns det så många repeatrar i sjätte och sjunde distrikten att alla inte får plats i scanning-listan (Anytone).

Dessa filer är testade med CPS Version: R2025.03.23.01

### Vad ändras vid konverteringen från Anytone till OpenGD77?

Vid konverteringen från Anytone till OpenGD77 så finns vissa begränsningar som man behöver ta hänsyn till.

* TG List i GD77 (motsvaras av Receive Group List i Anytone) är begränsad till 32 talgrupper så vi har valt de vanligaste i OpenGD77-versionen.
* Anytone har stöd för kanaler med både Analog och Digital sändning. I OpenGD77 kan en kanal vara antingen Analog eller Digital. Därför har vi konverterat dessa kanaler så här:
    * Anytone A+D TX A -> OpenGD77 Analog
    * Anytone D+A TX D -> OpenGD77 Digital
* OpenGD77 har en övergripande effektinställning som kallas Master. Den har valts för samtliga kanaler utom kanalerna för hotspots där lägsta effektläge (P1) har valts.
* Kanalnummer i OpenGD77 är begränsat till ca 1100 medan i Anytone är 4000. Däröför är kanalnummer i OpenGD77 bara löpande i stigande ordning medan de i Anytone börjar på jämna 100-tal för varje distrikt.

### Vilka radiomodeller är kodpluggen testad med?

OpenGD77 fungerar med en rad olika typer av radioapparater. Vi har fått rapporter om att kodpluggen är testad med följande radiomodeller:

* Radioddity GD77
* Retevis RT3S

Om du använder kodpluggen på en annan radiomodell än ovan, berätta det gärna för oss som en issue eller via ett mail till mig så lägger jag till det i listan. Ta också gärna en bild av radions display med kodpluggen och skicka med så kan vi få en uppfattning om hur det ser ut på olika radiomodeller.

### Vilka filer ska du hämta?

Jag rekommenderar att du hämtar filerna som jag har packat ihop i en [release](https://github.com/sm0rgm/opengd77/releases) istället för att hämta mina arbetsfiler!

### När filerna är hämtade... 

CSV-filerna kan du använda om du har en befintlig radio eller kodplugg som du vill uppdatera med kanaler, zoner, talgrupper etc. 

Om du snabbt och enkelt vill starta en ny kodplugg eller koda upp en ny radio så finns det en färdig fil med alla inställningar gjorda som heter N0CALL.g77.

Starta CPS-programmet och välj File -> Open och välj N0CALL.g77. Gå till fliken DMR ID and callsign och ändra Callsign och DMR ID till och dina egna. Gå också in i fliken Boot screen och ändra Line 1 till ditt callsign och Line 2 till ditt namn eftersom dessa används som Talker Alias. 
Sedan är det bara att skjuta i kodpluggen i radion.

Sedan vill du antagligen också gå till Extras -> Download callsign database och ladda ner callsigns från [radioid.net](https://radioid.net) för i alla fall region 240. Vill du ha fler regioner kan du gå till radioid.net, skapa ett konto och generera en kontaktlista över de regioner du önskar och instället importera dem med Import CSV.

Förmodligen vill du ändra på fler saker, men det överlåter jag till dig att fixa med själv.

### Om du inte kan importera CSV-filerna

Beroende på olika datorers inställningar för teckenkodning kan de resulterande CSV-filerna bli olika med avseende på tecken för decimalkomma mm (i vissa fall blir det "." och i andra "," i CSV-filerna. 

Om du får felmeddelande när du försöker importera mina CSV-filer, gör då så här:

* Starta CPS och läs in din radio
* Välj File -> Save och spara din nuvarande kodplugg som en .g77-fil
* Öppna filen N0CALL.g77 i CPS i din dator
* Välj File -> CSV -> Export och välj en lämplig mapp att spara CSV-filerna i
* Öppna din egen sparade kodplugg i CPS (.g77-fil)
* Välj File -> CSV -> Import och välj mappen där du nyligen sparade exporten

### Uppdatera befintlig kodplugg

Om du bara vill uppdatera din radio med kanaler, zoner och talgrupper men låta resterande inställning vara som de är kan du, istället öppna din befintliga kodplugg i CPS och sedan gå till File -> CSV -> Import CSV och välj sedan mappen CSV. 
## Suffix i repeaternamn

För att indikera typ av repeater eller vilket nätverk den är ansluten mot finns numera en eller flera bokstäver som suffix till repeaterns namn. Om repeatern är ansluten till Brandmeister för DMR eller är en lokal FM-repeater utan anslutning till reflektornätverk finns ingen bokstav angiven.

För att underlätta för instegsamatörer har numera kanalnamnet en indikering om kkanalen är 2m (V) eller 70 cm (U).

Bokstäverna betyder:

V = VHF 2m
U = UHF 70 cm
L = Link (simplex)
A = AllstarLink
S = SVXlink
E = EchoLink
H = Hotspot (DMR)
F = FreeDMR / FinDMR
+ = DMR+ / DMR Plus
I = IRLP / ircDDB
P = HAMphone

### Tema

För de radiotyper som har stöd för tema (f n MD-9600, RT-90, MD-UV380/RT3S, DM-1701/RT-84, MD-2017/RT-82) så har jag inkluderat mitt eget tema. Filen heter SM0RGM.gtm. Eftersom jag tycker det är mer vilsamt för ögonen med svart bakgrund har detta tema det och olika färger har använts för olika funktioner.

### FAQ 

* Varför är inte repeatrarnas benämning dess callsign, t ex "SK7ABC" utan de står med ortsnamn? Repeaterns callsign eller kanalnummer är praktiskt om du är på din hemmaort och känner till vilka repeatrar som finns. Kodpluggen är gjord för att man ska kunna använda den när man reser och kommer till en ny ort. Som SM0:a så säger mig SK7ABC ingenting men ortsnamnet "Helsingborg" t ex ger mig en geografisk indikation om att repeatern finns i närheten om jag t ex befinner mig i Helsingborstrakten.

#
### Tack

Stort tack till SA0BUX Lars för betatestning, tips, råd och inte minst för lån av en radio med OpenGD77 så att jag kunde testa kodpluggen!

Stort tack till SM0IKR Göran för betatestning, tips, råd och förslag.

## SM0RUX/Pontus silent key

Den 9 mars 2025 gick SM0RUX/Pontus silent key efter några års kamp mot cancern. Kodpluggen är och förblir "SM0RUX kodplugg" men underhålls fortsatt av mig, SM0RGM/Stefan. Kodpluggen är gratis att använda men vill du ge ett bidrag så tänk gärna på Cancerfonden tel. 010-199 10 10.

73's de SM0RGM Stefan

2025-05-04
