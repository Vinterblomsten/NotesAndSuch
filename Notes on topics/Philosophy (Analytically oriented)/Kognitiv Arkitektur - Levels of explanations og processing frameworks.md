#Representation #Cognition #PredictiveProcesseing #CognitiveArchitecture #Modelling 
## Forklaring i Kognitionsvidenskab - Og eksempler derpå

**Explanans** er det der forklarer **explanandum** (Det der skal forklares)
- Hvorfor er der **røg - explanandum**? Det er på grund af **ild - explanans**.
#### Forklaringsretninger
- **Horizontal forklaring** - Forklaring på samme niveau
	- Kausale sammenhænge inden for **samme ordforråd**
	- Ex.: Psykologisk - "Hun **ønsker at spille på rød**, fordi hun **tror** at kuglen lander på rød, og hun **ønsker** at vinde"
- **Vertikal forklaring** - Forklaring af fænomen med underliggende struktur
	- **Højre niveau fænomen** er muligt givet det **lavere niveaus struktur**
	- Mereologisk dekomposition, konstituerende dele og deres **temporale, spatiale, og kausale relationer**
		- **Mekanistiske** forklaring - Lavere niveau af fysisk bestandele
		- **Funktionelle** forklaringer - Lavere niveau af algoritmiske bestandele - Sub-funktioner
	- Det er en vertikal forklaring hvis det lavere niveau **illuminerer** det højere niveau
	- Ex.: Psykologisk - "Hun **ønsker at spille på rød** (Niveau 1), fordi hendes valuerende system har vurderet denne mulige handling med den højeste interne værdi, **givet den indre model** (Niveau 2), som lader sig gøre givet **aktiviteten i det orbito-frontale og ventromediale præfrontale cortex** (Niveau 3)"

I Kognitionsvidenskaben er den mest brugte vertikale forklaringsmodel **Marrs forklaringsniveauer**
- **Computationelt niveau:** Abstrakt Funktionel Rolle
	- Job-description - Hvad er typen af funktion der passer på den givne adfærd
	- Ex.: **Maximere samler reward over tid**
- **Algoritmisk niveau:** Hvordan kan en abstrakt algoritme producere adfær?
	- Beskrivelse af **repræsentationel** input og output, samt transformationsfunktionerne
	- **Metodologisk** - Formuleret gennem computationelle modeller - **medium-uafhængight**
	- Ex.: Kombineret RL og Intern Markov chain model af omgivelserne **beregner og minimere prediction error** for præcist at estimere værdi
- **Implementations niveau:** Hvordan kan det fysisk implementeres
	- Det konkrete biologiske mekanismer, der skal til for at realisere "algoritmen"
	- **Metodologisk** - Læsionsstudier, fMRI, TMS
	- Ex.: Nucleus Accumbens koder for **reward prediction error**, mens præfrontaler områder koder for **state prediction errors**, og orbito frontalt cortex koder samlet værdi

#### Explanatory Gap
- **Personal level** - Common-sense psykologien, mentale repræsentationer, computationalt niveau
- **Sub-personal level** - Algoritmisk implementation, og neural implementation 

**Leibnitz Mølle**
Hvis vi forstørrede hjernen således at vi kunne gå ind i den og kigge lidt rundt, så ville vi kunne kunne se alle mekanismerne arbejde (neurale netværk), men vi ville ikke kunne udpege entiteter af repræsentationer, følelser og tanker

Dette leder til **the gap** - Hvordan kan **sub-personal** niveau mekanismer **illuminere** repræsentationelt indhold, eller sagt på en anden måde
- Hvordan kan **fysiske og syntaktiske** egenskaber forklare **semantiske og mentale egenskaber** 

Har de **semantiske egenskaber** (content) nogen form for **explanatory power**, hvis det er **neural syntaks**, der gør alt det kausale arbejde? - Det mener Dennett!

#### Dennetts stances
Dennett er **instrumentalist** / **pragmatisk realist** ift. mental states - de spiller en vigtig rolle i forudsigelse og forklaring, men er **ikke reelle kausale entiteter** (Modsat Fodor, som er realist omkring mental states). 

Han mener at det er **evolutionær** udvikling, der har lagt fundamentet for rationaltet og dermed intentional stance muligheden.

Han enerkender **LOT** som en teori for implementationen af intentional stance, men ser den ikke som en logisk nødvendighed.

En **True Believer** er et system, som kan forudsiges ved brug af repræsentationelle (common-sense psykologiske) forklaringer - **Intentional Stance**

**Physical Stance:**
- At danner forudsigelser om et systems "adfærd" ud fra det fysiske bestanddele, og de fysiske love - ren fysisk kausalitet
- Ex.: Forudsige billiardbordets "state" baseret på ballernes fysiske bevægelse
**Design Stance:**
- At danne forudsigelser om et systems "adfærd" ud fra dets funktionelle rolle - dets design
- Ex.: Forudsige at bilen bevæger sig fremad, givet at du klikker på speederen - selv uden viden om motorens komposition
**Intentional Stance:**
- At danne forudsigelser om et systems "adfærd", som en **rationel agent**
	- Vi antager **overbevisninger (Beliefs)**, baseret på dets perceptuelle evener og miljø
	- Vi antager **ønsker (Desires)**, baseret på dets funktionelle egenskaber (både teleologisk - overlevelse, reproduktion, social status - og mekanisk - sult, kulde)
	- Vi antager **rationalitet** - at agenter handler ud fra kombination af ønsker og overbevisninger
- Hvis disse forudsigelse er præcise og konsistente, så definere vi systemet en **True Believer**
- Ex.: En termostat har en "overbevisning" om temperaturen og et ønske om en optimal temperatur - handler rationelt for at sænke eller hæve temperaturen derefter

**Super-fysiker-marsmanden**
Dennett præsentere en super fysiker, som forudser menneskers opførsel baseret på interaktion af neuroner, celler og atomer (**Physical stance**)
- Denne misser ud på **objektive facts** om verden i form af **mønste**
- De kan formentlig forudse at du sælger Novo-aktier efter en ozempic-skandale, men de ser ingen sammenhæng med at du købte dem tilbage efter et dyk i værdi - de misser et **reelt mønster**

### Neurodata i Kognitionsvidenskab
Kan sjældent sige noget om kausal-mekanismerne, men
- Vi kan lokalisere kognitive funktioner med dissociations analyser
- Dette kan have forklaringskraft for at dissociere kognitive funktioner - på et algoritmisk niveau også

## Kognitiv Arkitektur

#### Fodors Modularitet
Hvordan er sammenhængen mellem perceptuelle mekanismer og den centrale kognition?

- **(Wicked) Behaviorisme** - Perception er "dumb", ren reflex uden behandling og ekstra information (**non-inferential**) og uafhængigt at overbevisning (**encapsulation**)
- **(Handsome) New-look Cognitivisme** - Perception er "smart", en **integreret del af kognitionen**, både inferentiel og ikke-indkapslet - **Top-down process**
	- Mønter bliver opfattet som forskellig i størrelse af fattige og rige børn (wild eksperiment)

**Firestone and Scholl - Fejlslagen metodologi**
- Argumentere for at de **empiriske beviser for Top-down processering** blot er metodologiske fejl, hvor det ikke er selve outputtet af modulerne, men senere repræsentationer, men arbejder med

Fordor står et sted i midten
- Perception er **inferential** (I et automatisk begrænset omfang) men **Encapsulated** - det er ikke direkte påvirket af viden og overbevisninger
- Vi bliver snydt af optiske illusioner, **også når vi kender til sandheden**

Fodors arkitektur - To typer af "faculties"
- **Horizontal Faculties** - Funktionelt separerbare, men operere på tværs (i samarbejde)
	- Hukommelse, Værdisætning, Forestillingsevne
- **Vertical Faculties** (Moduler) - Både **funktionelt og operationelt separerede** uden interfakultært samarbejde på tværs af domæner
	- Visuel perception, Audidativ perception, etc.
	- Disse moduler er ifølge Fodor
		- **Indkapslede** - Informations processeringen i modulet kan ikke påvirkes af information tilgængelig for resten af sindet
		- **Inferentielle** - De har stadig computationelle egenskaber til at fortolke input, baseret på modules egne informationer
			- Dette tillader for eksempel visuelle illusioner
		- Derudover også - **Automatiske, Hurtige, Bundet til neurale strukture, Basale outputs**
Den samlede arkitektur
- **Transducers** - Sanseorganer, omdanner fysiske energi til signaler
- **Input moduler** - Omdanner signaler til basale repræsentationer
- **Centrale systemer** - Integrere output repræsentationerne med global information, overbevisninger, for at igangsætte planlægning og handling

**Central kognition** er utrolig svær at undersøge ift. moduler, da den er
- **Isotropisk** - Der er ingen *a priori* grænser for, hvilke informationer og overbevisninger der er relevant til en beslutning
- **Quinian** - Vores **belief system** er hollisitisk - **et net af kohærens** - hvis vi møder kontradiktorisk information til vores overbevisning, er der utallige måder, hvorpå vi kan ændre overbevisninger, for at dette inkorporeres

Vi må derfor for at forstår central kognition
1. Reducere det til moduler (Massive Modality)
2. Undersøge alternative frameworks til at modellere det
3. Opgive det hele...

#### The Bayesian Brain
The Bayesian Brain er en **funktionel hypotese** om at hjernen er en **bayesiansk inferens**-maskine, der repræsenterer sensorisk information stokastisk, og kombinerer prior-information og ny input for at beregne **uncertainty**
- **Weak Claim** - Nogle kognitive processer bruger uncertainty i computationer på en nogenlunde "Bayes optimal" måde
	- Passer med videnskabelig evidens! (Imagenary musik - omvendt polaritet)
	- **Fodors moduler** kan beskrives som bayesiansk inferens, med **prediction error** som output
- **Strong Claim** - *Alle* kognitive processer bruger uncertainty i computationerne
	- Alt hvad hjernen gør er bayesiansk inferens
	- Grand Unifying Approach (GUT)

#### Hierarchical Predictive Processing - Andy Clark
Hvor Bayesian Brain er funktionel, er PP en **algoritmisk hypotese**

**Den generative model**
- Hjernen danner generative modeller af omgivelserne - specifikt, hvordan de danner de sensoriske inputs
- Disse danner **forudsigelser** - Hvordan burde det sensoriske input være, givet den modellerede begivenhed
- **Prediction-error** er så forskellen på forudsigelsen og de reelle sensoriske inputs
- Modellen opdateres alt efter **hvilken "hypotese" minimerer prediction-error**

Det betyder altså at outputtet fra en kognitiv process er repræsenteret som **afvigelser fra vores forventninger** og ikke den fulde perceptuelle repræsentation
- Givet bayesiansk inferens repræsenteres **vores sikkerhed i forventningerne af styrken af vores priors** 

**Hierarkisk opdeling**
- De kognitive (og neurale) processer er organiseret i niveauer fra lav-niveau sensorisk fortolkning, til høj-niveau planlægning og reflektion
- Signaler sendes mellem niveauer i begge retninger
	- **Top-down** - Predictions (**Priors**) 
	- **Bottom-up** - Prediction errors (Surprisal)
- Det vil altså sige at en succesfuld forudsigelse **bortforklare**r input-signalet - **Ingen up-stream information**
	- Dette leder til en enormt **effektiv data minimeringsstrategi** i sammenligning med at skulle sende fulde perceptuelle signaler op og ned gennem systemerne

**Action-orienteret PP**
I Clarks PP er der **to måder at minimere prediction error**
- Revurdering og justering af interne generative modeller (**Change of belief**)
- Forandre de eksterne omgivelser til at matche forudsigelsen (**Aktiv inferens**)
	- Bruges til at minimere overraskelse både ved higher level "forudsigelse" (desires)
	- Bruges til at minimere usikkerhed ved aktivt at ændre verden, for at få mere information (Ved konkurrerende hypoteser)

Dette resulterer i en samlet teori for perception og handling (**Grand Unified Theory**)
- Hjernen forudser at vi drikker en slurk kaffe
- Det leder til at vi matcher forudsigelsen med at genere en lavere niveaue motorisk forudsigelse om at samle koppen op gennem aktiv inferens 
- Dette leder så til forudsigelse om konkrete motoriske handlinger, som udføres gennem aktiv inferens (I tråd med optimal controll theory)

Eksempel med malleri - Vi måler øjenbevægelser konsistente med aktiv inferens af forskellige high-level "forventninger" (ønsker) om hvad vi vil undersøge på billedet.
- Saccades kan anses sem "eksperimenter" for at vælge en blandt konkurrerende hypoteser

**The Dark Room Problem**
Hvis hele målet var at minimere prediction error, hvorfor kravler vi ikke ind i et mørkt rum, hvor vi kan have ingen forventninger og ingen inputs - ergo ingen prediction error?
- Men det er ikke hvad der sker - vi er nysgerrige, aktive, opsøgende, (sultne)

Andy Clark påstår **hyperpriors**
- "Stædige" high-level priors - utrolig stærke og rigide
- Forudser embodied-cognition kriterier såsom kropstemperatur, smerteminimering, anti-sult, etc.
- **The Crooked Scientist** - Ændre alt ved verden for at den lever op til deres hypoteser (Om overlevelse i sidste ende)
	- Men hvor kommer priorsne fra? Er de medfødte eller lærte? Kan de ændres?
- Fører os lige i retning af:
#### Free-Energy Principle - Friston
The grandest of unified theories - Ikke blot om kognition, men metafysisk princip
- Inspireret af termodynamik (Gibs fri energi) og statistisk fysik
- Gældende for enhvert **selvorganiserende system**, der forblive organiseret over tid 
	- Hjerner er blot et specielt case af et generelt biologisk princip
	- Systemerne **modarbejder entropi** og forbliver inden for levedygtige stadier **homeostase**

I FEP er entropi og disorder beskrevet som **(enbodied) surprisal** 
- Kroptemperatur på 37 grader er et low-surprisal state, mens 39 grader er et high-surprisal state
- Siden den reelle surprisal vil kræve alvidenhed, estimeres et **upper-bound** på surprisal kaldet **Variational Free Energy**

FEP er sammenligneligt med PP hvor
- Det højeste niveau forudsigelse er den forsatte eksistens (anti-entropi)
- I stedet for at minimere prediction errors, så minimeres **expected free energy** (EFE)
	- Expected free energy kan opdeles additivt i 
		- **Expected ambiguity** - Den epistemiske værdi i en given state: højere ambiguity medfører **lavere forventet information** - Vi vil gerne have information for bedre interne modeller
		- **Risk** - Den pragmatiske værdi i en given state: Lavere risk medfører større sandsynlighed for at forblive i "orden" - minimere sult, sygdom, kulde, etc.
	- Det vil altså sige at EFE både repræsentere **exploration** og **exploitation** 
	- EFE er en forudsigende mekanisme, og operer altså ikke blot med den nuværende state
- FEP har dermed ikke samme Dark Room Problem som PP

#### Humean Minds - FEP og PP
Common-sense psykologien er **Humeanske**. Vi har både:
- **Beliefs** (Mind-to-world fit) - Vores beliefs tilpasser sig verden
- **Desires** (World-to-mind fit) - Vi tilpasser verden for vores desires
Problemet er at ifølge PP har er der ikke noget, som repræsentere desires, kun beliefs
- Dermed **anti-humean** - kan det reddes?
- Også lidt i forlængelse af Dark Room Problem - Hvordan opnår vi handling uden desire?

To versioner af PP (Ish)
- **Optimistic Predictive Processing** - Clarks version
	- "Desires" er blot optimistiske priors (beliefs), og vi kan altså ikke have en opdeling mellem de to mentale state - anti-humean
	- Kan ikke forklare **value-learning**, hvordan lærer vi nye præferencer, som ikke blot er præference for det vi oplever med højeste frekvens - hvilket det rent intuitivt ikke er
- **Preference Predictive Processing**  - En Implementationel version af FEP (Ikke teleologisk)
	- Givet opdelingen mellem expected ambiguity og risk, har vi en mulighed for at udpege desires i systemet - eller hvad Frederik, Jelle og Thor kalder **preferred outcomes**
	- Dette er givet ved **risk** netop defineret som en difference mellem **preferred outcome** og **expected outcome**
		- Matematisk givet ved en separat matrice, C, fra de to matricer som definerer **Markov Decision Processens** transitions mellem hidden og visible states (Forudsigelses processen)
	- Dette vil altså lede til en separering mellem
		- **Belief** - A-matrice, forventningen
		- **Desire** - C-matrice, den ønskede udfald
		- **Risk** - Forskellen mellem de to (ish)
	- Dette løser også **value-learning problemet** - at opdage nye handlinger (states) som leder til minimering af free energy
Dette leder os til at vælge i mellem **sparsomhed** (parsimony) og **forklaringskraft**

### Reinforcement Learning?

**Learning**
- Pavlov - Classical Conditioning (**Stimulus-response**)
- Operant Conditioning (**Trial-and-error**)

**Sekventiel beslutningstagen**
Ikke blot en one-step process, men transitionerne mellem en række states
- **Reward** er den umiddelbare værdi at et state, men **value** inkludere de forventede prospektiver (**reward** af de næste states - måske med en **temporal discounting**)
- **The Bellman Equation** - Formaliserer dette med et divide-and-conquer paradigme
	- Hver states værdi er givet ved **reward + værdi af den bedste næste state**
	- Løst baglæns **rekursivt**
- **Læring** - Hvor monte-carlo metoden først opdatere værdier til slut, lærer vi istedet med
	- **Temporal Difference Learning (TD)** - Sutton
	- Vi bruger tidligere forudsigelser, til at ændre værdier af states
		- Ex: Hvis man hører fødselsdagssang på gangen vil gangens værdi stige, da det leder til en støre forventning reward, selvom man slet ikke har sat tænderne i en kage (endnu)
	- Implementeret med **signal prediction errors** gennem **dopamin**

**Reward Paradox** - Modsat AI har vi ikke nogen intrinsisk værdi
- Den er altid infereret fra perceptuelle input (Kage er ikke lig 10 point, men infereres som en biologisk "præmie")
- Inutitivt er værdier infereret fra en række **højere-ordens mål** - ikke at sulte, ikke at fryse, men også social succes, underholdning og en følelse af selvrealisering (Hvad end det så betyder)
- **Men hvordan vælger vi mål?**
	- Den kan ikke være infereret fra reward - det vil være **cirkulært**

#### PP og RL - Unifying theories
- **Prediction-error/free-energy minimization** versus **reward optimization / value-learning**
- Samme problem, hvordan forklares **priors**/**value** i begge paradigmer?