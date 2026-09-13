#Cognition #Logic #Bayesian
### Intro/Disko

**Pure reasoning** vs **Statistical learning**
- Babier er konstant eksponeret for aldrig før sete situationer - hvis de skal kunne finde hoved og hale i det, må de kunne inferere nogle forventninger
- **Pure reasoning** er her defineret som even til at integrere abstrakt viden og perceptuelle inputs til at forudsige nye situationer

Teglas et al. forventer at babier har en fysisk simulation - intern generativ model, som kan integrerer forskellige abstrakte heuristikker og perceptuelle inputs, til at generere sofistikerede forudsigelser
- De laver en "Ideel Bayesiansk Observatør"-model, som integerer nogle fysiske regler (priors) med den "perceptuelle scene" (likelihoods) ved hjælp af brownian movement principper (begrænset af fysiske regler)
### Metode
**Violation of Expectation paradigme** - Bruger looking time til at undersøge viden/forventning pre-verbalt

**Figur 2A** 
- 20 deltagere - 12 måneder
- 12 forskellige film - 2 x 2 x 3
- **Observation** 3 + 1 objekter i en cirkel (Bevægende, bouncing)
	- Faktor af hvilket objekt, var i overtal/undertal - **Ratiofaktor**
	- Faktor af om overtal eller undertals objektet var tættest udgangen - **Distancefaktor**
- **Occlusion** cirklen tildækkes med varieret varighed
	- Opdelt i tre eksperimenter efter occlusion duration (2s, 1s, 0.04s)
- **Udfald** - et objekt kommer ud af udgangen
	- Looking-time målt - (**VoE)**
### Resultater

**Figur 2
- **B**. 0.04s looking-time: Signifikans for distancefaktor men ikke ratiofaktor
- **C.** 1s looking-time: Signifikans for både ratiofaktor og distancefaktor, men ingen interaktion
	- Tyder på en additiv effekt
- **D.** 2s looking-time: Signifikans for ratiofaktor, ikke for distancefaktor
- Tyder på en rationel forventning - distance kortsigtet men frekvens langsigtet
	- En form for dynamisk rationalitet, i stedet for en fast heuristik

**Ideal bayesian observer**
- Modellen arbejder ud fra pre-occlusion position og bevægelser
- Antager babiers intuitive fysik ved en form for **brownian motion**
	- Random pertubations - begrænset af barriere
- Monte Carlo samling prediction
	- Computationelle resourcer svarer til sampling antal - den ideale bayesianske observatør ved infinite limit

**Figur 3** - Model samenlignet med eksperiment
- **B.** Joint Probability for hver af de to typer på et givet tidspunkt, t, (y-aksen) over occlusion duration (x-aksen)
	- To forskellige starting conditions
- **C.** Betinget sandsynlighed (Den vi er interesseret i) - Givet et objekt kommer ud ved tid t, hvad er sandsynligheden for at det er hver af de to typer?
	- De to sandsynligheder konvergerer mod frekvensen
- **D.** De diskrete punkter tilsvarende eksperimentet på **C**
- **E.** Tilsvarende figur 2, hvis vi antager looking-time kan estimeres som *1-P(Object|t)*
- **F**. Korrelation for de 12 eksperimentelle konditioner 
	- Looking-time fra eksperimenterne på y-aksen
	- Den inverse betingede sandsynlighed på x-aksen
	- Stærk korrelation (r=0.94) og (p<0.0001)
	- Forklarer 88% varians (den bedste lineære combination af faktorer forklarer 61% varians)
	- Babier udfører altså kognitive beregning meget tæt på den optimale probabilistiske analyse (Givet de simple fysiske regler)
- Selv hvis modellen er begrænset og kun sampler 1-2 trajectories er den næsten identisk
	- Lidt snyd, fordi den tager gennemsnit af trials og deltagere, så det er i virkeligheden en del flere en 1-2 samples

**Model test i 4 og 5**

**Figur 4** - Test for tilsvarende random begivenheder fra andre eksperimenter
- **A, D og G** - Tre setups med forskellige betingelser, der tester lignende fysisk intution
- **B, E og H** - Looking-time for babier - resultater fra andre eksperimenter
- **C, F og I** - Den ideelle bayesianske observatørs forudsigelser
	- Den inverse betingede sandsynlighed - Fanger hovedtendenserne, omend ikke så kvantitativt præcist som første eksperiment
	- E og F er interessant - Modellen afviser blankt at objekter kan passere den fysiske barriere, mens babier er mere "open-minded"

**Figur 5** - Test for **objekt-kognition** 
- **A, B og C** - Undersøger objekt-kohærens-opfattelse - 3 måneder
	- **Habituering**: En lang stang bevæger sig frem og tilbage **eller** er stationær, bag et dække
	- Bagefter bliver det afsløret om det faktisk var 2 eller 1 stang
	- Modellen forudsiger, med reglerne for brownian moment, at stangen er én ved ens bevægelse, men er hip som hap hvis den er stationær - akkurat ligsom babier
- **D, E og F** - 2.5 måneder
	- **Habituering**: enten et eller to objekter
	- Gemt bag enten en hel eller splittet skærm
	- Skiftevis bliver et objekt ført frem i begge sider
	- Modellen forudsiger overraskelse ved ét objekt bag splittet skærm, men ellers ikke - overens med de reelle resultater
### Disko/Persp

**Pure reason vs statistical learning**
- Babierne behøver ikke at have været eksponeret for en situation mange gange, for at kunne give forudsigelse
- I stedet er der en **"one-shot" generativ proces**, der gør dem i stand til at bruge intuition / "mental game engine" - intuitiv fysik
- Dog kunne man forestille sig at de fysiske regler er statistisk funderet (spatiotemporel kohærens og soliditet)

**Rationel integration af variable**
- Babier bruger ikke blot simple heuristikker/regler, men formår at sætte dem i kontekst og integrere dem med hinanden - måske ved hjælp af en intern simulation / generativ model
- Fysiske principper som priors i en bayesiansk inferens

**Ideel Bayesiansk Observatør**
- Stærk korrelation med looking-time evidens, tyder på at babier bruge en form for monte carlo process, til at beregne mulige forløb
- Dog fanger modellen ikke babiers "open-mindedness" (figur 4 EF)
	- Fanget, hvis reglerne agerede som priors i bayesiansk inferens og ikke absolutte regler
- Formentlig er der ikke en **lineær** sammenhæng mellem expectation og looking-time

Looking-time paradigme **Violation of Expectation** vs **Need x Gain** model (Karni)
	- I forsøget antages at looking-time reflektere overraskelse, men måske det er mere komplekst
	- I Karnis model kunne høj looking-time ved VoE beskrives som en høj Gain ved brud på det familiære fysiske heuritikke