---
Title: Load
Description: This is my load page.
Template: analysis
---

Load
================

I denna rapport kommer tre webbplatsers laddningstid att mätas och eventuell förbättringspotential med avseende på det att undersökas.

Urval
-----------------

För den här undersökning har jag valt att titta på webbplatser från olika branscher och även olika länder. Målet var att försöka få ett urval av webbplatser med olika design, mål och bakgrund och består av en sida som dokumenterar webbteknologier, en nätbutik som fokuserar på friluftsliv och
en arrangör av motionslopp:

* [developer.mozilla.org](https://developer.mozilla.org/en-US/)
* [outnorth.se](https://www.outnorth.se/)
* [kagoshima-marathon.jp](https://www.kagoshima-marathon.jp/)
<br>
<br>

Utöver startsidorna undersöks även två slumpvis valda undersidor för varje webbplats.

Metod
-----------------

Alla mätningar har gjorts i webbläsaren firefox i ett privat fönster så att ingen eventuell sparad
data ska kunna påverka resultaten.

Prestandan är mätt med hjälp av [PageSpeed Insights](https://pagespeed.web.dev/) och övrigt med
hjälp av webbläsarens inbyggda utvecklingsverktyg under fliken nätverk. Alla mätningar har gjorts
tre gånger och resultaten som presenteras det Google Sheet som finns nedan är snittet av dem.

Resultat
------------------

<div class="sheet-embed">
    <iframe class="sheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSa1Id_tblGN-sNyUUq3PBjj7T14ONZMqPnIFjsJX8kNmbzB3wXGLgsR22ETuj14eBmMbFicugEPRpa/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>

### developer.mozilla.org

<a class="reportlink" href="%base_url%?image/mdn.png">![Screenshot av developer.mozilla.org](%base_url%/image/mdn.png?w=250&crop=1920,1920,0,0 "mdn") {.small}</a>

Som förväntat så går det snabbt för MDN att ladda och webbplatsen får bra prestandabetyg. Sidorna innehåller varken stora eller många filer så det är ingen stor mängd data som behöver överföras.
De förslagen som PageSpeed Insights ger för förbättring är "Eliminate render-blocking resources" och i mobilt läge även "Reduce unused JavaScript".

### outnorth.se

<a class="reportlink" href="%base_url%?image/outnorth.png">![Screenshot av outnorth.se](%base_url%/image/outnorth.png?w=250&crop=1920,1920,0,0 "outnorth") {.small}</a>

För Outnorth går det tyngre. Här finns mycket filer som behöver hämtas och många element som behöver renderas. 
Även här föreslås "Eliminate render-blocking resources" och "Reduce unused JavaScript" både i desktop och mobile, men i mobile tillkommer också "Reduce unused CSS", "Enable text compression", "Minify JavaScript", "Defer offscreen images" och "Preload Largest Contentful Paint image".

### kagoshima-marathon.jp

<a class="reportlink" href="%base_url%?image/kagoshima-marathon.png">![Screenshot av kagoshima-marathon.jp](%base_url%/image/kagoshima-marathon.png?w=250&crop=1920,1920,0,0 "kagoshima-marathon") {.small}</a>

Just startsidan för Kagoshima Marathon är klart större än alla andra sidor som undersökts vid detta tillfälle men trots det är den ändå inte den långsammaste.
Enligt PageSpeed Insights så är "Reduce unused JavaScript" den klart största potentiella förbättringen både på desktop och mobile. Övriga förslag som ges är "Eliminate render-blocking resources", "Serve images in next-gen formats", "Properly size images", "Reduce unused CSS", "Defer offscreen images", "Enable text compression" och "Minify CSS".


Analys
------------------

Alla webbplatser hade två gemensamma förbättringsförslag: "Eliminate render-blocking resources" och "Reduce unused JavaScript". Gemensamt för alla var även att prestandan i mobile är i nästan alla fall klart sämre än i dekstop och fler förslag till förbättring ges. 

Baserat på mätresultaten så ser rangordningen av webbplatserna som sådan:

* developer.mozilla.org
* kagoshima-marathon.jp
* outnorth.se
<br>
<br>

MDN spelar i en egen liga och det är väldigt jämnt mellan de andra två. Dock så tycker jag personligen inte att själva användarupplevelsen speglar ordningen mellan andra och tredje plats.
Kagoshima Marathon har en laddningsanimation som visas innan varje enskild sida vilket gör att det tar extra tid innan de visas och outnorth känns klart snabbare att använda.

Själv så upplever jag nog webbplatser som långsamma om de tar runt 1 sekund att ladda färdigt och med det i åtanke är det bara MDN av dessa som jag skulle säga är snabb när jag klickar runt på måfå. Outnorth går rätt bra att ladda nya sidor men det krävs ofta ett litet "hopp" innan allt har laggt sig helt på rätt plats.

Referenser
------------------

[PageSpeed Insights](https://pagespeed.web.dev/).

Övrigt
------------------

Rapporten är skriven av Philip Hébert-Wegmann.