Tags: #Ethics, #AlgorithmicBias, #Fairness, #Epistemology, #AI

Tsamados et al. beskriver i artiklen seks typer af bekymring inden for de etiske rammer af algortimer (specielt ML-algoritmer). De fleste af problemerne er i min optik variationer af de tre store: **Transparens**, **Garbage-in garbage** out og **Ansvar**

![[Screenshot 2025-10-27 at 08.46.53.png|400]]
##### Manglende forklaring (Inconclusive evidence)
Modellerne er kun det, modeller, og de bygger deres konklusioner på probabillistiske beregninger og statistiske korrelationer - der er ingen kausalmekanismer på spil. Derfor ender irrelevante korrelationer, der er et udtrykt for tidligere sociale uligheder, med at spille en forklarende rolle i modellen. 
**Ex**: Prædiktiv politiovervågning - modellen udleder større grad af kriminalitet i udsatte områder grundet tidligere overrepræsentation af politiaktivitet i området

##### Utydelig evidens (Inscrutable evidence)
Algoritmer og modeller, som deep learning networks, er ofte designet som en "black-box", hvor en række input leder til output, og vi som udgangspunkt ikke har nogen form for mulighed for at forstå modellens rute fra A til B. Altså er det meget svært at sætte spørgsmålstegn ved modellens resultat, for man kan ikke pointerede ud hvilke datapunkter der leder til det endelige output. 
**Ex:** En algoritmer der bestemmer renterne på et lån vil kunne udvise systematisk diskriminerende resultater, men det vil være meget svært at vise, da vi ikke kan pege på de enkelte datapunker, som kunne agere proxy-værdier uden at kende beregningen. 
(Man burde kunne opstille et indbygget evaluerende værktøj, der for hvert output også fortælle hvilke datapunker, der hiearakisk spillede den en rolle for resultatet)

##### Dårlig data (Misguided evidence)
Modellen er kun så god som den data den er trænet på. Modellen vil altid afspejle eksisterende sociale biaser og diskriminatoriske tendenser, også selvom man skjuler sensitive datapunker - proxy-problemet. 
**Ex:** En model til at læse ansøgninger trænet på tidligere ansattes ansøgninger, vil afspejle en tidligere tendens til at prioriterer mandlige ansøger, for selv om vi skjuler køn som en parameter, så finde den blot proxy-værdier, såsom sproget, fritidsaktiviter, tidligere arbejde, som "afslører" de mandlige ansøgere.'

##### Unfair udfald
Dette afsnit hænger lidt sammen med de overstående og beskriver problemet med fairness som en helhed. Der er mange forskellige definitioner og dele af fairness, og ofte hænger de ikke sammen.
- **Anti-klassifikation** er at fjerne sensitive attributter og deres proxy værdier fra datasættet
- **Fejlrater** - Sørge for at falsk positive og falsk negative fejlrater er ens på tværs af grupper
	- Umiddelbart den løsning jeg er mest tilhænger af - man kan ikke blot fjerne værdierne og så regne med at århundreders social, for slet ikke at snakke retsmæssig, ulighed ikke skinner igennem
**Ex:** Hvis man fjerner alle former for sensitive attributter og proxyværdier, så mister vi drastisk præcision, som i sidste ende resulterer i unfair udfald i sig selv: Hvis man lader prøveløsladelse være baseret på en model uden nogen proxyværdier for køn, så vil det resultere i at kvinder får meget mere afslag, selv om de har langt lavere sandsynlighed for at udfører kriminalitet igen. 

##### Transformativ effekt
Vi er også nødt til at overvejer den effekt, som disse systemer kommer til at have på systemet som helhed, ikke blot for individerne. Hvis AI kommer til at sidde i smørhullet mellem dataindsamling og beslutningstagen på et bredere plan, så kan det medføre systematiske ændringer i de sociale dynamikker og magtstrukturer - den epistemiske virkelighed forandres sammen med vores forståelse for autonomi, privathed og fairness. 

##### Problemet med ansvar
Implementationen af modeller i beslutningsprocedurer slører et allerede mudret bureaukratisk rod om ansvarstagen. Hvis en beslutningstager kan offloade ansvaret for deres beslutning til en "selvbestemmende" model, er det så ikke bare en ren ansvarsfraskrivelse? Noget som politikkere og virksomhedder ellers er ret gode til i forvejen. 
Dette punkt eksemplificerer virkelig tungt, hvorfor den etableret elite kæmpe for at AI skal spille en større rolle, for det er ansvarsfraskrivelsens bedste ven.
**Ex:** Den selvkørende bil selvfølgelig - Hvem er ansvarlig for at bilen kører en familie på fem ned en almindelig tirsdag? Producenten? Programmøren? Chaufføren? 
