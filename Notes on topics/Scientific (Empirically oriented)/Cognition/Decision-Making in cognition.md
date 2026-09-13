#Cognition #Logic #Representation 
### Perceptual
The process of interpreting (noisy) sensory information to choose between possible actions
**Noise** being
- Environmental noise
- Sensory noise
- Neural noise

Experimentally investegated using **Two-alternative forces choice** (2AFC)
- Such as **Random Dot Kinematogram**

#### Signal Detection Theory - for analysis of 2AFC og Binære task
To overlappende fordelinger repræsenterer de to "noisy" muligheder
- **sensitiviteten - d'** er givet ved forskellen på de to middelværdier delt med variationen ($\frac{\mu_1-\mu_2}{\sigma}$)
- **Beslutningskriteriet** (response bias) - placeret "frivilligt" et sted mellem de to
Fittes ud fra data med **hit og miss (og false alarm og correct rejection - ved binary tasks)**

**d' er bedre end accuracy** da den er uafhængig af **response bias**
- Dog mangler SDT et tidskomponenet - reaktionstid og speed accuracy trade-off

#### DDM - Drift Diffusion Model
Akkumulationen af noisy evidence over tid 
- Giver en account for både **valg**, **reaktionstid** og **response bias**
**Parametre**
- Drift rate (v) - Raten for akkumulering af neural evidens
- Boundary separation eller threshold (a) - speed/accuracy trade-off
- Response bias (z) - startpunkt for akkumuleringen
- Non-decision time ($t_0$) - Både encoding af stimulus og motor handling ikke relateret til beslutningen
- 
**Neural opbakning**
- **Aber udviser DDM- lignende respons** ved 2AFC, hvor motorrespons ses ved samme neurale threshold, uagtet tidsperioden dertil
- Tilsvarende for **mennesker** med EEG over **Centro Parietal** 
	- Akkumulering
	- Threshold
	

### Metacognition
The ability to reflect on and evaluate our own thoughts and actions
- Begge veje - Både monitorering og control

World (Sensory information) -> Judgement about the world (**type 1)** -> Judgement about judgement **(type 2)**

**Confidence** - Det betingede "sandsynlighed" for dit svar, givet din overbevisnings "fordeling"

**Metodologi i confidence** - Finde metacognitive sensitivity (**meta d'**)
**1** - Explicit **self-report** af confidence
- Problem: Antager tilstedeværelsen af det vi prøver at måle

**2** - Korrelation med performance på tværs af deltagere
- Problem: tager ikke højde for metacognitivt bias

**3** - Korrelation med egen performance mellem trials / blokke
- Problem: smal skal giver bias

**4 - Computational Modeling**
Vi udvider **signal detection theory** - inkludere nu to kriterier på hver side af midten, som skiller høj confidence (kanter) og lav confidence (midten) - **distancen mellem er meta-d'**
- For at finde **metacognitive efficiency** deler vi med performance-d'
- m-ratio = meta-d' / d'
Problemet er at det ikke modellere bias eller reaktionstid ergo:

**Post-decisional process**
Vores confidence over tid afspejler valget 
- Ved en fejl falder confidence
- Ved et hit stiger confidence
- Implicere post-decisional evidens akkumulering

**Evidence accumulation model of post-decisional confidence**
DDM - Fortsætte efter at ramme threshold og beslutningen er taget
- Ved confidence-målingen bliver det "aflæst" gradueret af en sigmoid funktion
- Tre parametre i modellen
	- **v-bias**: Post-decision drift rate (Større eller mindre end pre-decision)
	- **a-bias**: additiv bias af sigmoidfunktionen - forskudt op/ned
	- **m-bias**: multiplikativt bias - bredere/smallere forvridning
- Forskningen viser 
	- **Angst**: Negativt v-bias og a-bias (Lavere confidence overall og over tid)
	- **Kønsforskel**: Mænd har lavere a-bias end kvinder (Højere confidence til start men flader ud)
![[Screenshot 2026-01-04 at 11.51.12.png|300]]

**Neural evidens**
- Rat OFC opfører sig som en form for post-decisional confidence
- Anterior præfrontal cortex er korrelaret med confidence, men ikke performance

### Value based
Hvordan vælger vi mellem to muligheder - præferencer
En ting er den objektive værdi, men ting har meget forskellig subjektiv værdi (utility) baseret på kontekst og præferencer
- Implicere en **common currency for value**

**Komponenter i VBDM**
![[Screenshot 2026-01-04 at 14.00.06.png|400]]
For hver beslutning 
- overvejer vi Interne og Externe states og mulighederne derefter (**Representation**)
- forudsigere værdien af disse muligheder, betinget af interne og eksterne states (**Valuation**)
- tager et valg baseret på dette (**Action selection**) 
- Evaluere udfaldet og bruger dette til at opdatere de tre foregående processer.

**Tre systemer for værdi** 
- **Pavlovian** - Det basale stimulus-respons læring
	- Necessities of survival - Fjern hånden fra komfuret, det er varmt
- **Habitual** - Trial-and-error **model-fri** læring
	- Drik en kaffe om morgenen - Stimulerende
- **Goal-Directed** - Værdien af en handling er givet ved action-outcome assiciationerne - 
	- **model-baseret**
	- Vælg en bog på biblioteket - Ny spændende underholdning

Valget mellem værdier
- **Expected utility theory** - Værdien er absolut værdi x sandsynlighed
- **Prospekt theory** - Værdien er den relative værdi til et refferencepunkt x sandynlighed
	- Temporal discounting
	- Loss aversion
	- etc.

##### Hvordan lærer vi værdi?

Ved **Reinforcement Learning** - to måder

**Model-frit** - Trial-and-error
Ligegyldigt hvordan det virker, hvis det virker
- Direkte **Caching** af værdier til en handling
- Computationelt billigt og hurtigt
- Ikke fleksibelt
To Skridt
- **Reward Prediction Error** forskellen mellem udfaldet og den forventede værdi
- Opdatering af den forventede (Cachede) værdi proportionelt med en **læringsrate**

**Model-baseret** - Simulator
- En intern model eller "kognitivt kort" over states og transitions
- Cacher ikke værdier, men beregner/simulerer dem i den enkelte situation
- **"If-then" search tree** - transitions og udfald
- **State Prediction Errors**
- Computationelt dyrt, men helt fleksibelt fra situation til situation

**Action-selection**
- Kan repræsenteres som **Drift Diffusion Model** med værdi-forskel som driftrate
- Softmax med **temperature** kan beskrive sandsynligheden for lav-value-choice

#### Neurobiologien
**Orbitofrontal cortex (OFC)** og **Ventromedial præfrontal cortex (vmPFC)** korrelere med værdivurderinger af alle mulige typer
- Støtter ideen om en **common currency**

##### Dopamine og Reward Prediction Error
Dopamin centres aktivitet korrelere med RPE ved pavlovian learning
- Forventning + Reward -> Ingen spike
- Forventning + Ingen reward -> Negativ spike
- Ingen forventning + Reward -> Positiv spike

**Model-based** - Fractal Reward Association tasks
- **Stokastiske** transitions og state spaces - n-step tasks
- **State Prediction Errors (SPE)**  indkodes uafhængigt af reward

Normalt bruges en hybrid af model-fri og model-baseret
- Både SPE og RPE

Gennem dopaminsystemet bliver det **backpropagated** tilbage til striatum og præfrontale områder (Opdatering af værdisætningen)
- **Ventral Striatum indkoder RPE (Model-frit)**
- **Lateral præfrontal og Intraparietal indkoder SPE (Model-based)**

