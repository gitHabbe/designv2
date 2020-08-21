# Styling på webben

Denna rapport kommer handla om designval som utvecklare har valt att göra kring hemsidor som är webbrelaterade.

## Urval

För denna rapport valde jag att analysera W3school, Nodejs och Syntaxfm för att se vilka val dom gjort i designen för att locka folk att återvända till deras hemsidor. Alla tre är inom kategorin webbutveckling vilket jag tycker passar in på temat och dom har ett utseende som gör att man vill komma tillbaka för att hitta det senaste inom ämnet. Alla tre webbsidor har olika färgteman så det går att finna skillnader mellan dom vilket gör undersökningen och resultatet mer intressant. Ofta känns det som en mörkare design förväntar sig att en användare återkommer tycker jag personligen eftersom ljusare färger kan vara jobbigt för ögonen. Samtidigt är ljust tema välkomnande och bjuder in läsaren mycket mer eftersom det också känns mer bekant. Jag valde att hålla mig borta från hemsidor som GitHub och StackOverflow då jag kan tänka mig att många andra studenter valt dom i sitt arbete.

https://w3schools.com/
https://nodejs.org/en/
https://syntax.fm/

## Metod

Mycket av min undersökning kommer baseras på dom artiklar som jag personligen kommer överens med och som jag finner mest intressant. Några utav dom tycker jag gick lite för djupt och skriver om designval som besökare inte kommer hinna uppskatta eller ens märka (medvedet eller omedvedet) vilket inte är väl spenderad tid eller pengar.

Tillsammans med referenser till artiklarna används Adobe's färgpalett vilket är ett väldigt bra verktyg för att komma igång med ett tema enligt min åsikt. Genom att ange liknande färgvärden som hemsidorna använder sig utav så kan man försöka hitta vilken kombination av färger som utvecklarna jobbat med för att uppnå rätt design.

## Resultat

[FIGURE src="image/w3.png?w=600" class="left" caption="W3school"]

W3school hade en väldigt intressant färgkombination för sin applikation. Vid första glans ser det ut som nyanser av grönt men efter att ha inspekterad med Chrome's utvecklingsverktyg så är alla element samma typ av grönfärg. Till och med knappar till bakgrundsfärg på navigeringsmenyer använder exakt samma färgkod. På någon sorts nivå så känns det som om det har valt färger som är enkla att skriva i hexa-decimaler istället för att specifikt välja en färg. Nästan som en fonetisk palindrom men inte helt riktigt. Dom har fokuserat på att använda olika typer av grått istället för grönt för att undvika att sida ser tråkig ut.

**h1 - h6: Segoe UI.**

<p style="font-family: Segoe UI,Arial,sans-serif">Segoe UI text exempel.</p>

**Brödtexten: Verdana.**

<p style="font-family: Verdana,sans-serif;">Verdana text exempel.</p>

<table style="border-spacing: 4px; border-collapse: separate">
    <tr>
        <td style="height: 50px; width: 50px; background-color: #4CAF50">
        <td style="height: 50px; width: 50px; background-color: #616161">
        <td style="height: 50px; width: 50px; background-color: #F1F1F1">
    </tr>
</table>

[FIGURE src="image/nodejs.png?w=600" class="left" caption="Nodejs"]

Nodejs är inne på liknande tema med den gröna färgen. Till skillnad från W3shool så använder dom ett monokromatiskt färgschema där det används väldigt mörka och ljusa versioner av grönt. Båda hemsidorna är designade att se platta ut vilket är en trend i dagens webbutveckling. Nodejs är inte lika minimalistisk som W3 vilket är fullt förståeligt eftersom det krävs med information på sidorna vilket gör det mycket svårare. Likt hemsidan Frêres d'Encre från nngroup-artikeln så gråskalar dom sina huvud och sidomenyer för att splitta upp innehållet och navigeringen.

**h1 - h6: Source Sans Pro.**

<p style="font-family: Source Sans Pro,Open Sans">Segoe UI text exempel.</p>

**Brödtexten: Lato.**

<p style="font-family: Lato,sans-serif;">Lato text exempel.</p>

<table style="border-spacing: 4px; border-collapse: separate">
    <tr>
        <td style="height: 50px; width: 50px; background-color: #026e00">
        <td style="height: 50px; width: 50px; background-color: #43853d">
        <td style="height: 50px; width: 50px; background-color: #EAF5E9">
    </tr>
</table>

[FIGURE src="image/syntax.png?w=600" class="left" caption="Syntaxfm"]

Till skillnad från dom andra hemsidorna så använder Syntaxfm en bakgrundsbild som inte verkar sammansmältas med något av innehållet annat än mediaspelarens färg och fonten på näst intill alla texter. Istället för att hålla sig till några få färger så vågar Syntaxfm använda regnbågens färger för att markera sina sociala medier. Eftersom dessa knappar är designade med lutande färger och några element är delvis transparent så får man inte känslan av att hemsidan ska vara platt.

**h1 - h6: Courier.**

<p style="font-family: courier,Open Sans">Courier  text exempel.</p>

**Brödtexten: Rad.**

<p style="font-family: Rad,sans-serif;">Lyckas inte hitta fonten</p>

<table style="border-spacing: 4px; border-collapse: separate">
    <tr>
        <td style="height: 50px; width: 50px; background-color: #1D1D1D">
        <td style="height: 50px; width: 50px; background-color: #666666">
        <td style="height: 50px; width: 50px; background-color: #f1c15d">
    </tr>
</table>

## Analys

Alla 3 hemsidor använder sig av en sans-serif font vilket är väldigt bra enligt mig. Det är enklare att läsa och brödtexter får en mer luftig känsla. I kodexempel, och syntax rubriker, så utnyttjar dom också typsnitt som man är van vid i textredigerare vilket är standard och uppskattat för läsare. Personligen föredrar jag Cascadia Code från Microsoft men dom flesta fonterna ser näst intill likadana ut. Det kan ofta kännas motinbjudande med en mörk meny men eftersom både Nodejs och W3school gör en skarp kontrast mellan bakgrund och fontfärg så är det inte lika obekvämt som det brukar vara. Eftersom alla hemsidor innehåller relativt mycket information så går det inte att uppnå ultimata minimalistupplevelsen vilket är fullt förståeligt. W3school är helt klart närmast men när en applikations mål är att lära ut så finns det ytterst lite frihet att jobba med.

En unik egenskap som Syntaxfm har är emojis. Inte allt för länge sedan kunde det kännas barnsligt att använda smileys och figurer på en relativt seriös hemsida men i dagens samhälle kommer dom till nytta. Så pass mycket att dom till och med kan vara inkluderade i meddelanden för Git och ge en överblick för vad ett stycke text medför till ett projekt.

Det känns inte som Syntaxfm har spånat på någon palett som skulle kunna fungera för hemsidan. Nodejs har nog lagt energi på att hitta färger som går bra tillsammans, medans W3school förmodligen mest bara testat vilka gråfärger som fungerar ihop. Det är lite konstigt att Syntaxfm har en mörk färg på texter som även ligger ovanpå en bakgrund som är relativt mörk. Inte speciellt bra kontrast men det är inte riktigt något med lägger märket till om man inte tittar lite noggrannare. Anledningen till att dom gör det är förmodligen för att hålla det konsekvent, men personligen hade jag försökt göra om designen och färgerna så att det ser bättre ut.

## Referenser

[w3schools.com/](https://www.w3schools.com/)
[nodejs.org/en/](https://nodejs.org/en/)
[syntax.fm/](https://syntax.fm/)
[nngroup.com/articles/characteristics-minimalism/](https://www.nngroup.com/articles/characteristics-minimalism/)
[color.adobe.com/create/color-wheel](https://color.adobe.com/create/color-wheel)

## Övrigt

Allt som allt så tycker jag att alla tre hemsidor ser bra ut. Mest tillfredsställande är W3school på grund av sin font, utrymme mellan element och val av färger. Att använda en bild som bakgrundsbild är jag inte ett fan utav såvida det inte är tänkt att man ska återvända flera gånger på en månad. Syntaxfm kompenserar detta med en bra strukur på innehållet vilket är förvånande för en podcast-hemsida. Slutligen så uppskattar jag det stora typsnittet som Nodejs har valt att använda sig utav. Man känner sig mindre begravd i brödtexten vilket det finns väldigt mycket av på grund av all dokumentation som erbjuds.

Gruppmeddlemmar: Niklas Hallberg
