#Bayesian #CognitiveArchitecture #Neuroimaging #Cognition
### Intro/Disko
Undersøgelse af brugen af model-fri versus model-baseret systemer i beslutningstagen
- Tidligere undersøgelser viser en opdeling af systemerne, det model-fri værende i ventrale striatum (**nucleus accumbens**) - dopamindrevet, moduleres af **Reward Prediction Error**
- Dette bliver undersøgt med en **two-step sekventiel opgave**, hvor en **model af state transitions** er krævet for at optimere udfaldet
- **Daw et el.**  undersøger med fMRI hvorvidt det ventrale striatum kan udelukkes fra model-baseret systemer, eller om det er aktivt i begge dele
### Metode - Figur 1
- 17 deltagere 201 trials hver - fMRI study
- two-stage bandit task / markov decision task
- Første step vælges en af to muligheder
	- Stokastisk transition leder med 70% til den ene (common) og 30% til den anden (rare)
- Andet step vælges en af to muligheder, med varierende sandsynlighed for payoff (gaussian random walk - mellem 0.25 og 0.75)

#### Figur 2 - Adfærd
- Alle - Sandsynligheden for at gentage 1. step valget, givet det tidligere valg er
	- Rewarded/unrewarded
	- "Sjælen" transition fra 1. state til 2. state eller ej
- **A.** Standart model-fri reinforcement model forudsigelse
	- Hovedeffekt af rewarded - hvis reward gentag valget (meget simpelt)
	- Ligeglad med transition
- **B.**  Model-baseret model forudsigelse
	- Kun interaktion - tager højde for sjælden transition og styrker kun valget ved common transition (ellers modsat)
- **C.** Reel data
	- Både signifikant **hovedeffekt for reward** og **interaktionseffekt** 
	- Viser at populationen bruger en blanding af model-fri og model-baseret
	- Individuel ananlyse viser main effekt for 14/17 og interaktion for 10/17
	- Top dollar vi bruger begge dele

#### Table 1 - Computational model
- I forlængelse af resulatet fra F2 er der lavet en **hybrid model**
- Modellen bruger et mix af model-fri og model-baseret, relationen kvantificeres individuelt med en vægt, **w, som siger hvor stor en "andel" er model-baseret**
	- Signifikant forskellig fra både 0 og 1, median 0.39 - vi bruger begge dele
- 92% sandsynlighed for at modellen fitter population bedst

**fMRI analyse**
To **time series** (sekvenser af værdier knyttet til de samme events) blev beregnet
1. Standart **RPE** beregnet som model-fri TD med for både first-stage transition og final reward
2. Ekslusivt model-baseret **RPE** (Ikke SPE, da det er værdien af stokastiske states) 
	- Beregnet med model-baseret RPE fratrukket standart RPE og **ortogonaliseret**
	- Således inkluderes nul-hypotese om model-baseret i striatum
#### Figur 3 & 4
- **A. (Begge)** Korrelation mellem standart RPE og BOLD signal
	- bilateral striatum og medial PFC
- **B. (Begge)** Korrelation mellem difference RPE og BOLD signal
	- ventral striatum og medial PFC
- **C. (Begge)** Konjuktionen viser netop overlappende aktivitet i ventral striatum
	- ventral striatum er involveret i både model-fri og model-based
- **D.** Med brug af de individuelle vægte ($w$) fra hybridmodellen fandt de en korrelation mellem brugen af model-baseret (højt $w$) og neural vægt med model-baseret
	- Højre ventrale striatum - mere brug af model-baseret  -> neural aktivitet vægtet mod model-baseret og ikke model-fri
- **F.** Scatterplot - Viser korrelationen mellem w og  den neurale vægt af model-based aktivitet i højre ventrale striatum

#### Figur 5 - Data-drevent
- Alternativ til computationel model-metode
- **A.** Viser aktiviteten i højre ventrale striatum ved et valg tilsvarende det tidligere
	- Opdelt efter udfaldet af de to stadier af det tidligere valg
	- Vi ser en klar hovedeffekt af reward ved det tidligere valg (standart RPE)
	- Tendens, men ikke signifikant interaktionseffekt (Model-baseret)
- **B.** Dog **signifikant korrelation** mellem størrelsen på de individuelle interaktionseffekter og de individuelle vægt w
- Bekræfter resultaterne fra figur 3 - Ventral striatum er både involveret i model-fri og model-baseret RPE

### Disko / Perp
I modsætning til tidligere viden - der er **ikke** separate, parallele neurale mekanismer for model-fri og model-baseret systemer
- Striatum er altså **ikke** et habit-zone, men et sted hvor de forskellige strategier interagerer

Daw et al. foreslår at det model-baserede system agerer som en form for "træner" for det model-fri system
- Interne modeller kan simulere udfald, som kan bruges til at **cache værdier** i det model-fri system, hvilket kan **reducere computational cost**