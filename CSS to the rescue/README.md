# CSS-to-the-rescue

Week 1: opdracht keuze en idee.
Ik heb gekozen voor een console panel voor de opdracht.
Mijn idee is om een spel te maken in de vorm van een duck shooter van een kermis.
- Er komen dan 3 lagen met verschillende groten eendjes
- De eenden bewegen heen en weer.
- misschien is er een knop om de doelwitten de versnellen om het moeilijker te maken.
- je gebruikt je muis door te klikken op de doelwitten om erop te "schieten".
- Er moet een teller zijn of een ander beeld, dat laat zien hoeveel punten er gescoord zijn of wat de prijs is.

Inspiratie heb ik van het plays.org spel: duck shoot
<a>https://plays.org/duck-shoot/</a>

<img src="inspiratie/Duck shoot.png" alt="Duckshootfoto">

met verschillende doelwitten niet alleen eenden en ook doelwittend die niet geraakt mogen worden, of die meer punten geven.




Week 2: Oefenen met animaties en de transform.
Ik ben deze week begonnen in CodePen met de animatie van de de doelwitten die heen en weer bewegen, het omvallen van de doelwitten als erop geklikt wordt. Hier is de collectie te zien van alle oefeningen.
https://codepen.io/collection/RPPqYx

De animatie heb ik gemaakt met keyframes zoals hieronder te zien.

<img src="Readme.afbeeldingen/keyframes.png">

Deze animatie zorgt ervoor dat de doelwitten heen en weer bewegen, op 50% draaien en op 100% weer terug draaien en dat allebei buiten beeld.
Ook zijn de doelwitten input type radio. Dit zorgt ervoor dat wanneer de doelwitten geraakt worden deze omvallen en niet nog een keer geklikt kunnen worden.

De doelwitten kunnen alleen gereset worden met de reset knop onderaan het scherm.

Ik heb ook in illustrator de eendjes gemaakt met een doelwit erop en deze in twee verschillende kleuren.

<img src="Afbeeldingen/Geel-eendje.png"> <img src="Afbeeldingen/Groen-eendje.png">

Tot nu toe ziet het er zo uit en bewegen de twee fieldsets op verschillende snelheden heen en weer.

<img src="Readme,afbeeldingen/Week2-stand-van-zaken.png">

Volgende week wil ik beginnen met uitzoeken hoe ik een counter kan maken voor hoeveel doelwitten er geraakt zijn.
en misschien beginnen aan het ontwerp van de rest van het kraampje van het spel.




Week 3: Counter, oude mannen knop, kraampje.....

Onderzoek:
https://www.hongkiat.com/blog/count-html-state-change/

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters

https://codepen.io/una/pen/NxZaNr?editors=1100

Nils kwam met het idee om de eendjes een klein beetje op en neer te laten gaan, naast dat ze heen en weer bewegen. Hij had hier een voorbeeld van 
die hij gemaakt had op 9elements, waarbij hetzelfde gebeurde met een vogel.
https://9elements.com/blog/speed-vs-duration-a-use-case-for-mixed-unit-division/

https://codepen.io/enbee81/pen/xxNzJem 

Ik heb toen gekeken naar de codepen welke delen nodig waren voor het op en neer gaan en derest verwijdert en toen in een andere codepen gekeken hoe dat bij mijn html en css aansluit. 
https://codepen.io/Jamie-Hart/pen/azbLZGM?editors=1100 

Ik moest een aantal dingen aanpassen zoals de variables: amplitude( Deze heb ik lager gemaakt zodat de beweging kleiner werd en, nu binnen de fieldset bleef), de variable voor de top van de eenden( Zodat deze boven bleven en de onderste rij niet bij het console uitsteekt tijdens de beweging)

En omdat ik de animatie van op en neer gaan in de label css had gezet, ging mijn oude mannen knop ook op en neer wat natuurlijk niet de bedoeling is. Dus moest ik voor div label {} animatie op none zetten en omdat de top die stond in label {} ook invloed had op de positie ervan moest ik de top zetten op 0.25em, zodat deze weer gelijk stond met de andere vakjes in de console. 

<img src="Readme,afbeeldingen/bewegend label.gif.gif" alt="label-op-en-neer">

<img src="Readme,afbeeldingen/goeie situatie.gif" alt="eendjes-bewegen-label-staat-vast">

Het enige wat jammer is is dat de eendjes niet apart op en neer gaan, maar ze gaan allemaal tegelijk op en neer.


Verder ben ik gaan werken aan het ontwerp van het kraampje. Met behulp van Gradients heb ik gordijnen gemaakt die aan de zijkant hangen en pilaren die aan de buitenkant staan om het dak omhoog te houden.

Tot nu toe zweven de eendjes nog over het scherm. Ze zitten nergens aan vast en bewegen los in de lucht. Ik moet dus nog bedenken hoe ik deze ga verbinden of dat ik ze ergens op ga neerzetten zoals de inspiratie, waarbij ze op water drijven.

Ik heb mijn zus het spel laten spelen en toen ging ze heel wild klikken op de eendjes en selecteerde ze steeds de img, dus heb ik user-select in css op none gezet zodat dat niet meer kan. 

Aan het eind van week 3 ziet mijn werk er als volgt uit.

<img src="Readme,afbeeldingen/EInd week 3.gif">

Volgende week(de laatste week) ga ik kijken hoe ik een timer kan toevoegen en dat er een scherm komt, dat aangeeft hoeveel punten er gescoord zijn binnen een bepaalde tijd.




Week 4: Responsiveness, status en feedback, new CSS architecture en responsiveness. 

Voor de laatste week moet ik de status van knoppen  nog in beeld brengen. Bij de oude mannen knop is dat makkelijk te doen door wanneer de checkbox gechecked is de achtergrond kleur te veranderen naar groen. Dat heb ik gedaan met een gradient, met een beetje wit in het midden dat lijkt op een lampje, waarbij een rood lampje uit staat en groen aan. 

Dan heb ik de counter een nieuw lettertype gegeven en een nieuwe achtergrond, waardoor het lijkt op een digitale teller.

Toen ben ik begonnen aan het eindscherm, waarop de gescoorde punten te zien zijn en de knop komt om opnieuw te beginnen. 
Inplaats van een submit knop voor de form, heb ik er nu een link van gemaakt, want een submit knop kan niet animaties resetten, dus was het beter om de hele pagina te resetten. 
De achtergrond van het scherm heeft dezelfde gradient als de gordijnen in het ontwerp, waardoor het lijkt op een gordijn dat omlaag komt en het spel bedekt. In de Div van het scherm zitten de text Game Over en de knop, en te counter die in de console van het spel zit, kon niet tellen als deze erin zat. 
Daarom moest ik de positie van de counter zo maken zodat het voor het gordijn blijft als deze omlaag komt met z-index en position: absolute. 
Het game over scherm ziet er als volgt uit uiteindelijk met de animatie.

<img src="Readme,afbeeldingen/Eindscherm.gif">


Voor het aftellen wilde ik het maken dat de user 20 seconden heeft om zoveel mogelijk te raken. Nils gaf van een college een voorbeeld van een css spel met hetzelfde concept.

https://codepen.io/elad2412/pen/wvabjXy 
https://www.youtube.com/watch?v=QVdWMbmXHjo&t=1700s 


Hierin telt het af van 100 naar 0 met animations. Dit heb ik dus omgezet van 100 naar 0, om van 20 naar 0 af te tellen. 
Ik moest twee animaties gebruiken, één voor ieder getal.

<img src="Readme,afbeeldingen/code for timer.png"> <img src="Readme,afbeeldingen/code for timer2.png">

De afteller heb ik dezelfde stijl gegeven als de score counter en ernaast gezet, op de plek waar eerste de reset knop zat. 

Het tweede wat ik deze week nog moest doen, is twee van de nieuwe css architecture features invoeren. Ik heb gekozen voor Css nesting en @layers.

Dan moest ik nog responsiveness in de hoogte maken voor het spel. Met media queries heb ik ervoor gezorgt dat als de pagina een bepaalde hoeveelheid px is, dan veranderd de display van de onderste fieldset naar none. Wordt het nog kleiner gemaakt, verdwijnt ook de tweede fieldset. Dit werkt ook voor de score counter als het eindscherm naar beneden is. Dan blijft deze in beeld als het scherm kleiner wordt.