#Cognition #MusicalCognition #PredictiveProcesseing  #Neuroimaging 
### Intro/Disko - Hvorfor er det overhovedet interresant?
- To dimensioner af forsøget
	- Musik forestilling (Imagery) - Hvordan sammenlignes de neurale mekanismer ved at lytte til musik, med at forestille sig musik
	- Expectation - Hvordan spiller forudsigelighed af musikken en rolle for denne dynamik?
- I et  perspektiv af predictive-coding og free-energy principle, kunne den musiske forestilling spille en rolle som forudsigelse - hvilket i det paradigme vil betyde, at vi kan forvente en modsvarende respons, i stedet for en tilsvarende respons
### Metode
- 21 ansatte og studerende fra det Parisianske konservatorium
- 4 melodier fra Backs korarrangementer (kun sopran/melodi stemme) - 30s hver
- Før eksperiment - øve på klaver og kontrol med klaver og sang til perfektion / rytmisk og tonalt
- Taktil-metronom (vibration), for fastsat tempo
- 88 trials - 2 betingelser x 4 melodier x 11 gange - Shuffeled
	- Listening - Lytte mens man læser noderne
	- Imagery - Læse noderne og forestille melodien i tempo med metronomet

**Figur 1**
- IDyOM - Information Dynamics of Music (Kender fra Cheung et al.)
	- Bruger både short-term og long-term moduler
	- Trænet på både pitch of tonelængde
	- Beregner "Expectation Gain"  (Information content) for hver tone i melodierne
- Onset vector - Timesteps med node 1 ellers 0
- Expectation Vector - Onset vector moduleret for expectation
- TRF (Temporal Response Function) - Lineær mapping fra henholdsvis Onset og expectation vector til EEG respons, for timesteps -100 til 500, for hver af de 64 elektroder. 
	- Bruges til at forudsige en EEG repsons, fra en given tone
	- Null Models (For onset - shuffled trial order / rytmer) (For expectation - shuffled expectation signal, men samme rytme) - 20 permutationer / blandinger for hver
	- Disse modeller sammenlignes, ved at beregne korrelationen mellem forudsigelse og reel EEG, fratrukket de 20 null-model korrelationer, for hver deltager - to distributioner, som kan statistisk sammenlignes
	- (TRF Kernel er vægten / den lineære transformation, for hver elektrode for hver timestep)
- (vend tilbage til D senere)

### Resultater

Figur prio:
- 

**Figur 2** - Onset
- A. Fordelingen af TRF-forudsigelserne for Onsets korrelationer med EEG er signifikant forskudt ift. control fordelingen - **både listening og imagery**  
	- Man kan forudsige EEG ud fra onset vector bedre end chance
- B. Signifikant for 17 ud af 21 deltagere på deltageniveau
- C. Elektrode Cz - TRF vægte over tidsskridt -100 til 500, for Imagery og Listening 
	- Positiv peak for listening omkring 170 ms, mens negativt peak for imagery omkring 300 ms - Kunne tyde på invers polaritet
- D. **IKKE ERP - men korrelation** - Korrelation mellem de to, lokationen er nogenlunde ens (Relativt central parietal til frontal), selvom der er temporal forskel

**Figur 3** - Taler ind i predictive coding paradigmet
- A. Forudsigelse af EEG ved listening med TRF baseret på imagery - ingen signifikans for Onset > Control
- B. Samme som A, men med omvendt polaritet for TRF - Er signifikant større end kontrol
	- Vi ser dog ikke signifikans den anden vej rundt -  EEG ved imagery med invers TRF baseret på listning - Formentlig grundet amplitudeforskel
- C. Topografi af TRF (Ikke korrelation, men vægte) ved peak tidspunktet respektivt (170 og 300)
	- Imagery invers nederst, hvor de er meget ens (r=0.9)
- D. Lineær mapping af de enkelte vægte fra listening til imagery - trænet på n-1 og testet på den sidste
	- Signifikant forudsigelse

**Figur 4** - Expectations
- A. Fordelingen af TRF-forudsigelserne for Expectation korrelationer med EEG er signifikant forskudt ift. control fordelingen - **både listening og imagery**  
	- Man kan forudsige EEG fra expectation vector bedre end chancen
- B. Signifikant for 12 ud af 21 deltagere på deltagerniveau
- C. Topography af korrelationen - Meget korreleret mellem listening og imagery (r=0.9)
	- Kunne tyde på at de samme neurale mekanismer udfører "musical grammar"-high level processering, Frontalt latteralt

**Figur 5** - Kort
- Viser tidligere analyse for tre intervaller af EEG-frekvenser medtaget i korrelationen
	- Alle er signifikante og det temporale aspekt på Cz er tilsvarende onset-TRF, men topografien er svagere i de frontale latterale, ved frekvens over 1 hz

**Figur 6** - Control - Undersøgelse af short-term vs long-term modulet i IDyOM
- A&B - Både short og long term har signifikant forklaringsgrad 
	- TRF trænet på henholdsvis short term og long term expectation vector 
- C.  Short term og scrambled long term vs begge dele - viser at long-term har signifikant forklaring
- D. Expectation vector + low level features og Shuffled expectation vector + low level fatures
- E. Viser at expectation signifikant forbedre forudsigelse, selv med low-level features tage i betragtning

**Figur 7** - ERP analyse
- A. ERP for tone over Cz
	- Forventelig lighed med TRF-kernel
- B. ERP sammenligning for toner med 20% mest surprisal og 20% mindst
	- Indikerer stærkere respons (højre peaks) for high suprisal, men **ikke signifikant**
- C. ERP-topografier på tværs af deltagere, for tre tidspunkter
	- Indikerer denne inverse polaritet mellem listening og imagery

**Figur 8** - Mind reading, fortæl resultat, ikke metode medmindre spurgt
- Viser klar signifikant forudsigelse af melodi med EEG og metode beskrevet herunder - Mind reading
- For hver melodi, blev et 128 prediktorer produceret 64 elektroder x 2 vektorer
	- Ved et givent EEG signal, bliver det, for hvort punkt, korreleret med de forskellige prediktorer og den med højest r-værdi bliver valgt. Den melodi der bliver valgt flest gange, er forudsigelsen til sidst

**Figur 9** - Universalitet
- Tilsvarende figur 4, men med **leave-one-out** metoden, der forudsiger en deltagers EEG med TRF trænet uden denne deltager - Signifikant for både Listening og Imagery
- Individuelt er der lidt færre signifikante resultater end i figur 4.

**Figur 10** - Sammenhæng med AMMA (Auditional capabilities)
- Korrelation mellem forskellen på onset-modellen og control per deltager og AMMA score
	- Ikke signifikant, heller ikke for expectation-modellen

### Disko
- Klar lighed mellem de neurale mekanismer i listening og imagery
- Imagery udviser også modulerede neurale response for niveauer af "overraskelse", selvom man selv forestiller sig det
- Der er stærk indikation for en form for omvendt polaritet ved imagery ift. listening, hvilket taler ind i predictive-coding paradigmet, om at det er en prediction error respons. 
- Cheung et al. - Nydelse ved musikken er i forbindelse til denne prediction error, hvilket i sammenhæng med at vi udviser prediction error ved forestilling, forklarer hvorfor vi kan finde nydelse i at "afspille mental musik"
- Hage ved at det er profesionelle musikere - måske deres imagery er radikalt inderledes end vores