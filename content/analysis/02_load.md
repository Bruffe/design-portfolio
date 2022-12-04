Analys av laddningstider
=======================

I denna rapport kommer jag analysera laddningstiden för tre olika hemsidor.

Urval
-----------------------

Jag har valt att analysera YouTube, Twitter och Facebook. Min tankegång var att de alla tre är väldigt stora sociala medier och det kan vara intressant att se om någon av hemsidorna är bättre anpassad än de andra.

Metod
-----------------------

Min metod var att jag gick in på [PageSpeed Insights](https://pagespeed.web.dev) och testade hemsidorna jag valt. Sen skrev jag ner tiden "Time to Interactive" (laddningstid) för både mobil och dator. Det verktyget loggar inte in på hemsidan vilket skapade lite problem när jag testade Facebook eftersom man måste vara inloggad för att se det mesta. Därför valde jag att testa prestandan på ett specifikt inlägg. 

Utöver det använde jag Dev-tools på varje hemsida genom att göra en full reload, så att alla filer skickas från servern. Med hjälp av Dev-tools tog jag fram information om laddningstid och filstorlek. Jag mätte fram tills absolut allt var inladdat, därför kan mina siffror vara något högre än de från PageSpeed. Alla siffror jag tagit fram presenteras i min Google Spreadsheet.

Resultat
-----------------------

<div>
<figure style="margin: 0 auto">
<figcaption style="text-align: center"><a href="https://www.youtube.com">YouTube</a></figcaption>
<img src="%base_url%/image/youtube.png" alt="YouTube" style="width: 50%; display: block; margin: 0 auto; margin-bottom: 1rem">
</figure>

<figure style="margin: 0 auto">
<figcaption style="text-align: center"><a href="https://www.twitter.com">Twitter</a></figcaption>
<img src="%base_url%/image/twitter-02.png" alt="Twitter" style="width: 50%; display: block; margin: 0 auto; margin-bottom: 1rem">
</figure>

<figure style="margin: 0 auto">
<figcaption style="text-align: center"><a href="https://www.facebook.com/photo/?fbid=811984878912042&set=a.105451242898746">Facebook (ett inlägg)</a></figcaption>
<img src="%base_url%/image/facebook-02.png" alt="Facebook (one post)" style="width: 50%; display: block; margin: 0 auto; margin-bottom: 1rem">
</figure>

<figure style="margin: 0 auto">
<figcaption style="text-align: center"><a href="https://www.facebook.com">Facebook</a></figcaption>
<img src="%base_url%/image/facebook.png" alt="Facebook" style="width: 50%; display: block; margin: 0 auto; margin-bottom: 1rem">
</figure>
</div>

<div style="display: flex; justify-content: center">
<iframe style="width: 47.5%; height: 13rem" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSL3vSxjlogrCXxpIdv2yb_c8GREfNJaPWV5hSkO1aKHMW0OV371-t-9pEnUgego-O9xRno0CFL0GXI/pubhtml?widget=true&amp;headers=false"></iframe>
</div>

<!-- Dokumentera dina resultat från din studie. Berätta vad du kom fram till, vilka resultat du hittade och observerade. -->

Analys
-----------------------

<!-- Diskutera och analysera de resultaten du fann. -->

YouTube's laddningstid var den sämsta utan tvekan enligt PageSpeed, speciellt på mobilen. Där tog det 10,6 sekunder för sidan att ladda och PageSpeed uppskattar att det går att förbättra det med cirka 5,5 sekunder. Mer än hälften av den minskningen består av att ta bort oanvänd JavaScript och CSS. På datorn tog det istället 6,1 sekunder med en möjligthet att förbättras 2,5 sekunder, främst genom att ta bort oanvänd kod och minska serverns svarstid.

Twitter's laddningstid på mobilen var 7,1 sekunder där cirka 3,5 sekunder tas upp av oanvänd JavaScript, enligt PageSpeed. På datorn däremot gick det mycket snabbare, endast 1,6 sekunder med en potentiell ökning av 0,6 sekunder genom att ta bort oanvänd JavaScript.

Facebook's laddningstid enligt PageSpeed hamnade på 1,7 sekunder på datorn och 2,7 sekunder på mobilen. Trots denna korta tid i jämförelse med de andra hemsidorna så påstår PageSpeed att de kan spara cirka 0,9 sekunder på datorn genom att ta bort oanvänd kod. På mobilen är chanserna ännu större, där påstås det möjligt att spara ungefär 2,5 sekunder. Nackdelar med hemsidan för mobilen består av oanvänd kod, bilder i fel upplösning och gammal JavaScript-kod.

Den största boven för dessa hemsidors laddningstider verkar utan tvekan vara oanvänd kod, speciellt JavaScript. Vinnaren står mellan Twitter och Facebook om man tittar laddningstider. Enligt mig är Twitter den klara vinnaren med tanke på att hemsidan laddar in ett flöde med inlägg medan mätningen på Facebook endast var ett inlägg, på grund av problem med inloggning som jag tidigare nämnt. Twitter hade dessutom minst antal problem. Att Twitter's hemsida kunde halvera sin laddningstid till mobilen och var så seg jämfört med på datorn kan bero på att den inte är lika bra underhållen eftersom det finns en app till mobilen. 

När man även jämför antal filer som laddas in (requests) på sidan ser man att Twitter har 104 stycken som tar upp 7,4 MB. Facebook hade minst antal requests och data om man tittar på raden i min spreadsheet där jag inte var inloggad och endast tittade på ett bildinlägg. När jag däremot var inloggad på Facebook och kunde se flödet av inlägg blev det 269 requests på totalt 21,9 MB. Ännu en anledning till att Twitter är vinnaren. När man såg flödet på alla tre hemsidor hade YouTube färre requests, men större filstorlek än Twitter och nästan lika stor som Facebook. Utöver det hade YouTube mycket värre laddningstider och poäng på PageSpeed jämfört med Twitter.

Utifrån det jag lärt mig i denna analys skulle jag säga att en laddningstid på 5 sekunder på mobilen är väldigt bra, något som endast Facebook-inlägget klarade. Däremot fick Twitter 65 av 100 poäng med 7,1 sekunder som enligt PageSpeed är okej. Runt 7-9 sekunder är min gräns där det är för långsamt på mobilen. På datorn däremot tycker jag att allt som är snabbare än 2-3 sekunder är bra, 1 sekund är väldigt bra. Twitter hade som sagt 1,6 sekunder. Gränsen för vad som är dåligt ligger runt 5 sekunder för mig, YouTube hade 6,1 sekunder tyvärr, väldigt oimponerande. 

Referenser
-----------------------

<div style="display: flex; justify-content: center">
<ul>
<li><a href="https://pagespeed.web.dev">PageSpeed Insights</a></li>
<li>Google's Devtools</li>
</ul>
</div>

Övrigt
-----------------------

Skriven av Gabriel Rahm.