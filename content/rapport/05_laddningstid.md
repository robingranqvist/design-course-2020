---
---
Laddningstid
=========================
Denna rapport går ut på att utvärdera tre olika webbplatsers laddningstid samt ge förslag på förbättringar.

## Urval

Denna rapport kommer att utvärdera tre olika nordiska länders diabetesförbunds webbsidor, dels p.g.a. att det kan vara intressant att se om denna typ av förbund verkar ha spenderat tid på att optimisera sina webbsidor, samt dels för att jag som skriver denna rapport har typ 1 diabetes och besöker dessa typer av webbsidor relativt ofta. Urvalet har skett genom en Google-sökning av diabetesförbund som verkar i länderna Finland, Sverige samt Norge.

## Metod

För att kunna analysera laddningstider samt få förslag på förbättringar har Google PageSpeed Insights använts. Dessutom har Chrome Devtools använts för att ta reda på antalet requests samt sidornas filstorlek. Google Sheets har använts för att dokumentera resultaten i analysen.

## Resultat

[Klicka här för att komma åt min Google Sheets innehållande rådata](https://docs.google.com/spreadsheets/d/13BrzydtVSlWXyRMRlBC8ggOT9JngzpsL6iRxl9J1apQ/edit?usp=sharing)

##### Diabetes.fi

Diabetes.fi är det finländska diabetesförbundets officiella webbsida. Analysen har gjorts på [förstasidan](https://diabetes.fi), en allmän sida om diabetesinformation [diabetesinformation](https://diabetes.fi/diabetes) samt en sida om [gemenskapen](https://diabetes.fi/yhteiso).

![Diabetes.fi](../htdocs/img/diabetes.fi-min.png)

Dessa sidor fick en Google PageSpeed Insight poäng på mellan 73-79 för mobilversionen samt 99 för datorversionen. Antalet requests låg mellan 35 - 36 och filstorleken var mellan 1.9MB till 2.2MB för de tre sidorna. 
Tid för webbsidan att nå ett interaktivt tillstånd låg i medeltal på 6.5 sekunder på mobilen samt 0.8 sekunder på alla tre sidor på desktop, vilket tyder på en optimeringsskillnad mellan de två versionerna.

Google PageSpeed Insight gav en hel del förslag för att optimera webbsidan ytterligare. Alla tre sidor skulle kunna ändra sina filformat från JPG och PNG till modernare JPEG 2000, JPEG XR och WebP, vilket skulle öka komprimeringen och minska filstorlekarna. Dessutom bad den om att optimera bildernas storlek mellan desktop och mobilversionen av webbplatsen. Ett tredje förslag som förekom var att skjuta upp inläsning av bilder som inte visas på skärmen och ge dessa bilder någon form av “lazyload”-funktion i mobilversionen av webbplatsen.


##### Diabetes.se

På det svenska diabetesförbundets webbplats analyserade jag 3 olika sidor, först den [förstasidan](diabetes.se) sedan en informationssida om [förbundet](diabetes.se/om-oss) och till sist en allmän [informationssida om diabetes](https://www.diabetes.se/diabetes/).

![Diabetes.se](../htdocs/img/diabetes.se-min.png)

Denna webbplats fick Google PageSpeed Insights-poäng på mellan 58-72 för mobilversionen samt mellan 87-95 för desktopversionen. Tiden till interaktivt tillstånd för mobilen låg på mellan 7,0s - 8,3s respektive 1,2s - 1,8s för desktopversionen. Antal requests låg på mellan 31 - 36 samt filstorlekarna på sidorna låg mellan 1.4MB - 1.7MB. Dessa resultat tyder alltså på en något sämre optimering än den tidigare finlänska diabeteswebbsidan, trots mindre filstorlekar samt färre requests.

Google PageSpeed Insights gav även här en del förslag på förbättringar. Alla sidor borde minifiera sin javascriptkod samt likt den finska sidan ändra sina bilder till modernare filformat. Den gav även förslag på att använda rätt storlekar för mobilversionen av sidorna.


##### Diabetes.no

Den tredje och sista sidan som har analyserats är det norska diabetesförbundets webbplats, diabetes.no. Här har [förstasidan](diabetes.no), en allmän [informationssida om diabetes](https://www.diabetes.no/om-diabetes/) samt en sida om information för [lokala diabetesförbund i norge](https://www.diabetes.no/fylkeslag/) analyserats.

![Diabetes.no](../htdocs/img/diabetes.no-min.png)

Mobilversionerna av sidorna fick en Google PageSpeed Insights-poäng på mellan 52-59, medan desktopversionerna landade på mellan 90-97. Tiden till ett intraktivt tillstånd hamnade för mobilversionerna på mellan 8,1s - 8,6s respektive 1,7s - 2,2s för desktop. Antal requests låg på mellan 42 - 67 och filstorlekarna låg på mellan 3.5MB - 6.9MB, vilket är en ganska rejäl skillnad mot de två tidigare analyserade webbplatserna.

För denna webbplats gav Google PageSpeed Insights en hel del förslag på föbättringar. Även här bad de att använda modernare filformat på bilderna samt att använda dem i rätt storlek mellan mobil- och desktopversionerna av webbplatsen. De gav även en del varningar om att man borde minifiera både javascript samt CSS, och till slut gav den ett förslag som inte fanns på de andra tidigare analyserade webbplatserna; nämligen att optimisera animationer på alla tre sidor. När jag kollade närmare såg jag att de hade några GIF-animerade reklamer på sidan, vilka borde laddas upp i t.ex. WEBM-format istället.


###### Analys

Alla dessa tre webbplatser var faktiskt rätt väloptimerade jämfört med vad jag trodde från början. Som vi kan se i resultatet är det Finlänska diabetesförbundets webbplats den snabbaste att laddabåde för mobil samt desktop. Detta är den trots att den använder sig av flera requests samt större filstorlekar än t.ex. den svenska sidan. Orsaken till detta beror troligen på den icke-optimiserade javascriptkoden som förekom som en av de större bovarna till dålig laddningstid på både den svenska och norska sidan. Enligt dessa resultat skulle jag vilja rangordna dem i följade ordning; Finland, Sverige och till sist Norge.

Det allmänt största problemet som alla tre webbplatserna verkar ha gemensamt är ändå bildoptimiseringen, speciellt för mobilversionen. Både genom att ändra filformat samt att ändra storlek på bilderna för mobilversionen av webbplatsen skulle de kunna spara mellan 2-5 sekunders laddningstid på alla de tre sidorna. För mig skall nog en webbsida ladda inom 3-4 sekunder innan jag blir lite otålig. Alla dessa tre webbplatser laddar snabbare än detta, åtminstone på desktopversionerna. Det kändes inte som en jättestor skillnad i laddningstid mellan dessa tre.

Det var ändå roligt att se att alla tre länder verkar ha spenderat tid på att få till en någonlunda snabb laddning och därmed bättre upplevelse för användarna. Jag funderade lite på varför just Finlands webbsida verkar vara mest optimiserad, och hittade då en lista över vilka länder där åtminstone typ 1 diabetes är mest förekommande. Där var Finland i topp med 57.6 diabetiker per 100,000 invånare. Sverige kommer på andra plats med 43.1 respektive Norge på fjärde plats med 27.9. Kanske Finlands webbplats har mera besökare och man därför har använt mera tid till att snabba till den?


## Referenser
* [Diabetes.fi](Diabetes.fi)
* [Diabetes.se](Diabetes.se)
* [Diabetes.no](Diabetes.no)
* [Lista för diabetesfrekvens i länder](https://www.diabetes.org.uk/about_us/news_landing_page/uk-has-worlds-5th-highest-rate-of-type-1-diabetes-in-children/list-of-countries-by-incidence-of-type-1-diabetes-ages-0-to-14)


## Övrigt

Denna rapport är skriven av endast mig, Robin Granqvist.