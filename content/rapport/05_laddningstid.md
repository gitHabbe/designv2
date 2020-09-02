# Laddningstid och användbarhet

I denna rapport kommer jag analysera och granska hur tre stycken hemsidor beteer sig under normal andvändning. Planen var att inspektera hemsidor som vi använder vangligtvis några gånger per år som vanliga användare, men ändrade mig och fortsätter med samma urval som min rapport för design gör. Du kan hitta den rapporten via [denna länk](rapport/fargschema). Anledningen kring valet var på grund av ren nyfikenhet. Alla tre hemsidor är riktade mot webbutvecklare och därmed borde dom erbjuda resultat som lutar mot bra prestation. Det är inte alltid enkelt att tillfredsställa alla krav som Google ställer på hemsidor för att nå en hög poängnivå. Som vi senare kommer ta en titt på så kan Google själv inte nå denna typ av framgång, men det gäller fram för allt att erbjuda en bra erfarenhet för besökaren själv.

Vi kommer ta en närmare blick på W3schools, Nodejs och Syntaxfm. Du har säkert hört talas om dom med eventuellt ett undantag för den sistnämnda. Målet med hemsidorna är att lära ut om webben och dom verktyg som vi har för att koda dom. Node och W3schools utnyttjar mestadels text men Syntaxfm använder ljud-filer. Det hade varit intressant om en av sidorna nyttjade video, men tyvärr kommer det inte inkluderas i denna rapport.

# Verktyg

För att samla data om webbapplikationerna så använder jag både Google Page Insight tillsammans med Google's network tool. Eftersom informationen ibland variera så visas det genomsnittliga resultatet. Detta kan bero på en mängd olika saker, men min personliga gissning är uppkoppllingar,klienter tillsammans med server delegering och skalning. Eftersom webbutveckling förändras så otroligt snabbt så valde jag att inte använda andra verktyg då resultatet föråldrat om inte analysen är anpassad mot dom nya teknologirena.

Google Insight och Network Tool mäter både snabbhet och storlek så jag förlitar mig på att dom uppdaterad till den nya standarden. Vi kommer bland annat att titta på när dokumentet är laddat och sedan fylld med information. Mått om hur lång tid det tar innan man kan klicka på något på hemsidan kommer attt ignoreras även fast det är viktig data. Andledning till detta är för att jag inte tror att hjärnan har hunnit tagit ett beslut, följt av muspekaren klickat på ett element under mellanskillnaden från att elementen syns på skärmen. Med ett litet undantag för Syntaxfm som nämns senare i rapporten.

# Excel

Här kan du se en överblick på resultatet för mätningarna i form av ett Excel-dokument. Det finns både en länk till arket och en bild eftersom källan till dokumentet kan komma att förändras eller försvinna i framtiden. Notera som stora skillnaderna i storlek medans laddningstiderna är relativt lika varandra. När det finns 2 värden tillsammans i en cell separerade med ett snesträck "/" så det första värdet desktop och det andra mobile. Detta för att minska på antalet rader och kolumner i dokumentet.

# Detaljar
[https://www.w3schools.com/](https://www.w3schools.com)
[FIGURE src="image/w3.png?w=600" class="left" caption="W3schools"]

Syntaxfm har helt klart den största hemsidan bland dom som analyserats. Eftersom dom valt att lägga näst intill all sin information på framsidan, vilket är på både gott och ont. Dom försöker urskilja sig från hemsidor där man ser en större lista på dom alternativ som man har som användare och därifrån klicka på det man vill besöka. Trots den enorma vertikala ytan så laddar hemsidan snabbt och tvingar inte användaren att vänta på resultatet. På något vis som jag inte vet om så hindrar dom element från att laddas för att spara på användarens bredband och tid. Allt som man navigerar nedåt så kan man övervaka nätverksfliken och se hur hemsidan växer hela vägen till 600% av sin egen storlek.

[https://nodejs.org/en/](https://nodejs.org/en)
[FIGURE src="image/nodejs.png?w=600" class="left" caption="Nodejs"]

Storleken på sidorna enligt Google stämmer relativt bra med vad Network tools säger. Båda räknar med den komprimerade filerna och låter klienten packa upp det på egen hand. Det verkar som Google's verktyg väljer att inte ränka med den mp3-fil som automatiskt laddar när man besöker Syntaxfm. Även fast dom inte laddar alla episoder i form av element direkt så laddas stora json-filer som innehåller datan som ska målas ut på dokumentet.

[https://syntax.fm/](https://syntax.fm)
[FIGURE src="image/syntax.png?w=600" class="left" caption="Syntaxfm"]

Nodejs är extremt mån om att nå snabba laddningstider vilket man märker direkt. Nästan all deras data är text och det antar jag är ett medvetet val att undvika media-element. Om man rör vyporten ner mot footern så laddas bland annat några väldigt små bilder. Om man inspekterar koden så syns ingen lazyloadattribut, men man ser helt klart hur dom sparar på bredband tills man faktiskt når den delen av applikationen. Att lägga energi och tid på dena typ av optimering är imponerande.

[FIGURE src="image/excel.png?w=600" class="left" caption="Statistik resultat"]


# Sammanfattning

Det är oklart varför samma data laddas flera gånger i form av json på Syntaxfm's hemsida. Eftersom deras applikation redan är så stor så borde dom helt klart jobba på att optimera laddaningen av dessa filer. W3schools änvänder också `document.write()` vilken straffa besökerna som spenderar sin tid på en långsamma uppkoppling. Ibland får hemsidorna dåligt betyg i "Cumulative Layout Shift (CLS)" vilket jag tror beror på dom strikta regler som dykt upp det senaste året angående cookies. Webbplatserna måste ge användaren en chans att ange vilken data som får sparas och därmed dyker ett fönster upp. Detta fönster kan blockera eller flytta element som skrivits ut tidigare och skapar irritation. Det kan även bero på att Nodejs till exempel läser av vilken typ av enhet som man besöker hemsidan ifrån och därefter skriver ut annorlunda information för att anpassa installationer åt utvecklaren.


# Ranking

1. Nodejs
2. W3schools
3. Syntaxfm

Utan några större bekymmer så tar Nodejs kronan för bästa hemsidan bland kandidaterna. Det är nästan så att jag vill att W3schools och Syntaxfm tar en delat andra plats trots skillnaden i statistiken eftersom det är mycket svårare att hantera mängden data som Syntaxfm gör. För vissa kan det kännas smartare att dölja dom ändra avsnitten men själv så uppskattar jag att allting syns. Eftersom jag inte utnyttjar någon typ av podcastspelare så tvingas jag ladda ner avsnitten manuellt. Detta blir drygt väldigt snabbt så jag utvecklade ett pythonskript som nyttjar BeatifulSoup4 och laddar ner dom avsnitt jag vill ha automatiskt. Detta hade inte fungerat lika bra om skriptet var tvungen att navigera runt på hemsidan och vänta på ny data.

# Egna tankar

Standarden för hur länge man vill vänta på att den hemsida ska ladda klart förändras väldigt ofta. Sist hörde jag 1 sekund innan användaren blir uttråkad och börjar fundera på vad ska händer härnäst. Personligen tycker jag att det verierar beroende på om jag är en återvändade läsare eller är där för första gången. När man nyttjar en applikation flertal gånger per månad så är det jobbigt att vänta på att data ska fyllas och en irritation skapas, men om jag surfar på något okänt för att utforska eller söka kontakt inforation så har jag inget emot att vänta lite extra. Runt 4 - 5 sekunder finner jag acceptabelt, men om jag ska tollerera mer så måste besöket vara så oviktigt att jag inte har något emot att titta bort från skärmen och prata med någon annan under tiden. Det betyder mer eller mindre att testet har misslyckats och inte når upp till mina krav.

Som tidigare nämnt i introduktionen så kan Google till och med vara på den lata sidan. När man läser en av deras artiklar om nätverkstabben så laddas en stor mängd bilder som både flyttar omkring texter och kan göra att man klickar fel. Inte nog med det, dom utnyttjar inte lazy loading på dom 40-tal bilder som laddas vilket inte sparar något alls på bredbandet. Detta visar mest att man kan inte bocka av alla punkter på checklistan även om man är ett företag värt flera miljarder kronor.

Alla dessa hemsidor når mina behov och låter mig inte vänta speciellt länge på information. Detta kommer nog inte till någon stor förvåning eftersom dom handlar om just webbutveckling och bryr sig om hur användaren uppfattar deras metoder.

# Övrigt

Det var en intressant uppgift att samla in all denna data. I framtiden ska jag försöka göra fler tester på mina egna sidor för att eventuellt lyckas bryta dåliga mönster som man plockat upp under utvecklingen. Det kan kännas stressigt, men man ska komma ihåg att verktygen existerar för att hjälp oss att förbättra våra dåliga vanor och lära oss hur man kan programmera effektivare.

Gruppmeddlemmar: Niklas Hallberg