#Cognition #FreeWill #CognitiveArchitecture #AI #Neuroimaging 
### Intro/Disko
Forlængelse af Libet's paradigme - undersøgelse af det temporale forløb af frit valg
- I modsætning til Libet er det en **Abstrakt** og **ikke-motorisk** beslutning
- Interesseret i **spatielt** og **temporalt** forløb
- Bruger frit valg i matematisk operation (abstrakt valg) uden motoraktivitet (på samme tid)
Hovedspørgsmål
- Former neural aktivitet et abstrakt valg forud for bevidstheden uafhængigt af motoraktivitet
- Er der separate neural systemer for "hvad" og "hvornår" vi vælger
- Ses neurale beslutningssignaler samtidig med default mode state?
### Metode
Pilotstudie udvalgte 22 (5 senere ekskluderet) deltagere, med balanceret valg af addition/subtraktion - uden fMRI
##### Figur 1 - 17 deltagere
Deltagerne observerede afslappet en sekvens af stimuli - 1000 ms hver
- Hvert stimuli har et centralt tal og bogstav, samt et tal i hvert hjørne
- Når en deltager **spontant** beslutter at udfører en operation (plus/minus) husker de bogstavet (Frame 0)
- I de to næste stimuli udfører de den valgte operation på de respektive to centrale tal
- På frame 3 vælger de resultatet blandt de fire hjørne-tal (En rigtig for hver operation, og to forkerte), med en af fire knapper
- På frame 4 vælger de bogstavet fra frame 0 blandt 4 muligheder (Bevidst timestamp - 97%)

Deltagerene ligger i fMRI med måling hvert 2000 ms

### Resultater
- 17.8 sekunder per beslutning - 12.2 beslutning per run

#### Figur 2
Metode - **Multivariate Pattern Classification**
- 14 timestamps mellem -8 og 18 s
- For hver timestamp - **searchlight approach**, opdeling i grupper af voxels (50-100), hvis værdier gemmes som en tilsvarende vektor (I stedet for at kigge på en voxel af gangen)
- For hver gruppe blev en **classifier** trænet (SVM) til at **forudsige** addition eller subtraktion
- En test på resterende fMRI (udenfor træning) giver en endelig accuracy (præcision) - hvis denne ligger over 50%, er der indkodet information

Graferne viser accuracy på y-akse og tid ift. frame 0 på x-aksen
**Precuneus / posterior cingulate** og **Medial frontopolar** er signifikant over 50% før bevidsthed
- Både ved -4 og -2 s
- Separate analyser - viser at begge områder er prædiktive selvstændigt
- Den abstrakte intention om valg af operation er biased allerede før bevidstheden
- Ingen signifikant BOLD signal før beslutning - kun classification mønster (derfor metoden)
**Angular gyrus** er signifikant over 50% efter bevidsthed
- Ved 4 s - men **hemodynamic delay**, så nok allerede omkring beslutning
- Forberedelse og selve beregningerne formentlig
- Også et signifikant BOLD signal, men ingen forskel mellem de to opgaver

#### Non-figur
- Searchlight analyse for **motor-respons** - SMA 6-10s efter Beslutning
	- Ingen information om abstrakt intention dog, **hverken efter eller før beslutning**
	- Modsat - ingen information om motor-respons i områderne for den abstrakte intention
- Searchlight analyse for **hvornår** beslutningen finder sted - **pre-SMA** med 72% præcision
	- Indikerer den funktionelle dissociation - Passer med **Anterior-posterior gradient**
		- Frontopolar og PCC/precuneus - "What"
		- Pre-SMA - "When"

#### Figur 3
- Aktivitet i DMN er typisk størts "off-task" (Afslapning, tankevandring)
- Intention-forudsigelsområder ligger tæt op ad DMN

ICA - Independent Component Analysis, er en dimensionsreduktionsteknik
- Finder statistisk uafhængige komponenter (Systemer) på tværs af tid og rum
- DMN blev udvalgt visuelt ud af 15 uafhængige komponenter
- Aktiviteten af DMN over tid blev beregning
Analysen blev lavet på denne data og **tidligere data fra motor-intention-forsøg**

**A.** 
	DMN overlapper med abstrakt-intention i **anterior-medial-PFC**
	DMN overlapper med motor-intention i **medial parietal cortex**

**B.** 
	DMN aktivitet peaker samtidig som classification-accuracy for abstrakt intention
	- Dog tidligere og længere bølge

Det betyder at vi ser "off-task" lignende aktivitet i DMN, samtidig med at der er ubevidst information parietalt og præfrontalt - Støtter op om at det er en **spontan** beslutning og ikke længere planlægning

### Disko/Perspek
- Det er ikke kun motor-intention som i Libet, men selv abstrakte intentioner er forberedt før bevidst beslutning
- Frontopolær og PCC/precuneus er aktive for intentioner generelt, både motor og abstrakt
- Der er en tydelig opdeling af "when" (Pre-SMA) og "what" (PCC, MFP) - Anterior-posterior gradient
- DMN er indikeret i at tage del i ubevidst formning af beslutning
- Rimelig anti fri vilje
	- Men hvorfor skal fri vilje være koblet til fænomenologien (epifænomenal)  - frit valg kan være kausal for oplevelsen og konsekvensen neuralt - **fri != bevidst**
	- Samme problem som med RP - stokastisk støj akkumuleres, betyder ikke at valget er taget på forhånd

- Hierarkisk comparator model / Optimal control theory
	- Aktiviteten kan være en **forward model**, der forudsigere aktiviten på en højere plan
	- Cortico-ganglian loops kan vise parallel beslutningstagen om abstrakt valg mere anterior, mens beslutningen om selve handling findes mere posterier (pre-sma) 
	
