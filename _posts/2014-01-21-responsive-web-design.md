---
ID: 343
post_title: Responsive Web Design
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2014/01/21/responsive-web-design/
published: true
post_date: 2014-01-21 10:59:40
---
<img class="alignnone size-large wp-image-350" src="http://simonpedersen.no/wp-content/uploads/2014/01/Content-is-like-water-1980-1024x768.jpg" alt="Content-is-like-water-1980" width="1024" height="768" /> Responsive web design beskriver design som tilpasser seg forskjellige skjermer (mobiler, netbrett, PC-er osv) slik at alle får en god opplevelse av nettsiden. 
## 70 % av mobilene er smarttelefoner Husker du hvordan mobiltelefonene våre ikke støttet HTML i gamle dager? I begynnelsen hadde de jo ikke en gang en nettleser. Men etter hvert begynte de å støtte et eget mobilt markupspråk som hette WAP. Heldigvis varte denne perioden ganske kort tid, og vi fikk raskt mobiler med god kapasitet. I dag er mobilene så kraftige at hovedbruksområdet ikke lengre er å snakke i telefonen, men digitalt konsum. Allerede i slutten av 2012 var andelen smartmobiler på det norske markedet kommet opp i 70 % (jeg spurte Telenor og Netcom). Som du vet er det også kort avstand mellom nettbrettene i Norske hjem. 

## Innholdskonsumenter vs. innholdsprodusenter Vi surfer på mobiler, nettbrett og (stasjonære)/laptopper med forskjellig hensikt og til forskjellige tider. Du har sikkert selv fisket frem mobilen i køen på Rimi, rett etter du våknet om morgenen, i et skikkelig kjedelig selskap (vær ærlig nå) eller på do. Så mobiler bruker vi til raskt informasjonskonsum og når vi måtte føle det for godt. Nettbrett bruker vi i sofaen. Når vi skal slappe av. Noen ser på film, andre surfer, leser nettaviser, ser på bilder. Og mange av oss bruker nettbrett til læring (TED, app-er for barna, NRK...) Nettbrett inviterer til konsum av innhold med mer lengde enn mobiler. Så hva da med laptopper og stasjonære maskiner? Laptopper har vi ennå, men stasjonære maskiner på vei vekk. Uansett representerer maskiner med skikkelig tastatur og relativt stor skjerm 

*innholdsprodusenter* i større grad enn *innholdskonsumenter.* 
## Knotete referat Jeg skal være den første til å innrømme at jeg har prøvd å skrive møtereferat på en iPad. Spesielt da den var ny. Den var så annerledes og kul og representerte en helt annen angrepsvinkel enn de tunge, gamle laptoppene. Vi hadde ingenting som hette 

[*ultrabook *][1]den gangen, så å knote på en iPad var liksom litt elegant. Nettbrett er best for innholdskonsument og ikke for produksjon av innhold. Selvfølgelig finnes det tastatur du kan klipse på nettbrettet, og det finnes nettbretthybrider som Microsoft Surface, som kommer med tastatur, og det finnes mange mennesker som produserer innhold på nettbrett, men på generelt grunnlag er nettbrett for konsumenter og ikke for produsenter. 
## Let's get down to business Nå er vi endelig inne på kjernen av Responsive Web Design (RWD). Hvordan kan vi tilpasse innholdet på en nettside, slik at det utnytter skjermbredden på alle de forskjellige enhetene? En mobil er jo fryktelig mye smalere enn en laptop. Responsive Web Design bruker noe som heter Media Queries til å plukke opp bredden på skjermen og så tilpasse innholdet på siden tilsvarende. Strukturen endrer seg men innholdet endrer seg ikke. 

## Hvilke enheter er relevant Når jeg tar ut oversikten over antall sidevisninger på kryss av en mengde norske nettsteder, får jeg følgende enheter, rangert etter mest brukt (disse enhetene utgjør 22 % av den totale traffikken): 

1.  Apple iPad - 50 %
2.  Apple iPhone - 25 %
3.  Samsung (Galaxy Tab 2, Galaxy S2, S3 og S4) Jeg har også tilgang til data som viser omsetning i nettbutikker pr. enhet, og også her følger enhetene samme rekkefølge som i listen over. Med andre ord er det Apple som er den store lederen i Norge, med Samsung på en OK andreplass. Alle de andre er ikke verdt å nevne. Dette kan riktignok forandre seg over ganske kort tid, men sjansen er stor for at Apple eller Samsung/Android vil være blant de største også om noen år. 

## Tilgjengelig på alle plattformer Så hvordan påvirker dette RWD og strategi for store organisasjoner som en kommune? En kommune har ennå større krav til å være tilgjengelig for alle brukere enn det en kommersiell side har. Du kjenner kanskje til 

[Direktoratet for forvaltning og IKT sine krav til universell utforming][2]? Fra 2013 gjelder de også kommersielle nettsider, men i praksis er det kun offentlige organisasjoner som i dag har et visst press på å følge retningslinjene. Tilgjengelighet via RWD handler mer om å tilgjengeliggjøre informasjon på andre enheter enn å nå alle brukertyper. Du må fremdeles følge kravene til universell utforming, men du når målgruppen i andre situasjoner enn foran PC-en. 
## Adaptive Web Design Den alternative måten å levere enhetstilpasset innhold heter Adaptive Web Design (AWD). I stedet for å levere samme HTML til alle enheter, leveres spesialtilpasset HTML til to eller flere type enheter. En AWD-metode som brukes hos oss i 

[Avento][3], er å levere forskjellig malverk under samme adresse. Du slipper med andre ord den gamle videresendingen fra www.kunde.no/produkter til m.kunde.no/produkter (som jo har irritert mange av oss). Mange roter med begrepene [AWD og RWD][4], noe som er forståelig, siden det hele tiden dukker opp nye begreper for å beskrive den eksponensielle digitale utviklingen (jeg har også rotet med begrepene). Nå er du blitt en av de som skjønner forskjellen. 
## Gull og grønne skoger RWD er ikke bare gull og grønne skoger. Den "gamle" generasjonen webdesignere har fokus på realisme og fantastiske bilder. Det fungerer dårlig hvis du skal levere til alle plattformer. Det blir rett og slett for mye data for mobiltelefoner å laste ned. Skal du lage en responsiv nettside som fungerer godt, må du basere den på en UI-pakke med et grid-basert layout, slik som 

[Twitter sin Bootstrap][5]. Kort forklart så gjør grid-et en del av tilpassningsjobben for deg, så du slipper å legge inn så mange timer for å få de forskjellige enhetene til å vise nettsiden din skikkelig. [<img class="alignnone size-full wp-image-351" src="http://simonpedersen.no/wp-content/uploads/2014/01/web.jpg" alt="Grid system" width="957" height="643" />][6]   En nettside som bruker grid-basert layout trenger ikke å se ut som masse firkanter ved siden av hverandre. Det viktige er at elementene følger størrelsene til kolonnene, slik at de enkelt kan kolapses på smalere skjermer. 
## Mobile First For å kunne levere godt responsivt webdesign, må du bruke designere som skjønner den nye designretningen som kreves. I 2010 sa Eric Schmidt at Google fra nå av ville utvikle med Mobile First som motto. Han gikk så langt at han sa “I think it’s now the joint project of all of us to make mobile the answer to pretty much everything” (

[sitat][7]) Skal du lage godt responsivt design, lønner det seg å tenke mobile first, og skalere opp derfra. [caption id="attachment_352" align="alignnone" width="625"][<img class="size-full wp-image-352" src="http://simonpedersen.no/wp-content/uploads/2014/01/TheFutureIsMobile.jpg" alt="Credits http://www.digitalbookworld.com/" width="625" height="470" />][8] Credits http://www.digitalbookworld.com/[/caption] Poenget med mobile first er at du begynner med å laste inn det mest essensielle for de små plattformene. Dette gir oss en kjappere opplevelse av siden og tar vekk unødvendig lasting. Videre ressurser som trengs på større skjermer lastes kun når de trengs. Konklusjon Det finnes mange meninger og mye forvirring rundt responsiv vs adaptiv web design. Jeg skal ikke gi deg noen fasit, annet enn å si at mobiltelefoner og nettbrett også i framtiden vil utgjøre en stor og voksende del av innholdskonsumentet, så uansett hva du mener om RWD eller AWD eller hvilket buzzword som er det neste, må du forholde deg til at en stadig voksende del av brukerne dine kommer fra mobile enheter. Sjekk gjerne ut noen av referansesidene. De går dypere i materialet. Du kan også se på noen av eksemplene må RWD og AWD. 
## Referanser Les om forskjellen mellom adaptive og responsive web desing: http://www.techrepublic.com/blog/web-designer/what-is-the-difference-between-responsive-vs-adaptive-web-design/ Netlife Research om responsivt design: http://iallenkelhet.no/2012/01/25/responsiv-design/ Mobile first design: Why it's great and why it sucks: http://designshack.net/articles/css/mobilefirst/ Noen norske sider som bruker responsive web design 

*   Trondheim kommune: <http://www.trondheim.kommune.no/>
*   Universitetet i Stavanger: <http://www.uis.no/>
*   Skatteetaten (Mobile First) - <http://www.skatteetaten.no/> Noen norske sider som bruker adaptive web design 

*   Bodø Kommune: <http://bodo.kommune.no/>
*   Matprat: <http://matprat.no>
*   Stavanger Kommune: <http://stavanger.kommune.no/>   

##

 [1]: https://www.google.no/search?q=ultrabook&espv=210&es_sm=93&tbm=isch&tbo=u&source=univ&sa=X&ei=wBneUuCjA8fOygPh54GABQ&ved=0CG4QsAQ&biw=1717&bih=876
 [2]: http://uu.difi.no/regelverk/krav-til-nettlosninger
 [3]: http://www.avento.no
 [4]: http://www.techrepublic.com/blog/web-designer/what-is-the-difference-between-responsive-vs-adaptive-web-design/
 [5]: http://getbootstrap.com
 [6]: http://simonpedersen.no/wp-content/uploads/2014/01/web.jpg
 [7]: http://www.pcmag.com/article2/0,2817,2359752,00.asp
 [8]: http://simonpedersen.no/wp-content/uploads/2014/01/TheFutureIsMobile.jpg