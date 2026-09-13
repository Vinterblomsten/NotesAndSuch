
Tags: #Ethics, #Fairness, #Egalitarianism, #Discrimination

### Introduction
Machine learning, and especially its use in societal issues, introduce problems of fairness and discrimination - especially in a world, where these issues are already apparent and underlying. This arises questions of how we formalises these things - what does it mean for an ML-model to be fair and non discriminatory?

Not always an easy task: Men and women treated similarly in prison parole sentencing, would result in women being locked up longer, even with a much lower rate og re-offending. (Even though this seems to me, to be a socialogical problem in it self, and maybe even a self-supporting problem)

Many measures exists for example:
- Accuracy equity - overall accuracy of prediction for each group
- Conditional accuracy equity - accuracy equity conditional  on their predicted class
- Equality of opportunity - Is the desirable outcome equally likely predicted given the base rate of each group
- Disparate treatment - Difference in false positives between groups

The problem is that (apparently) these measures are mathematically impossible to simultaneously satisfy - and choices between fairness measures must be made

- Which measures of fairness are most appropriate given the contexts?
- Which variables are legitimate grounds for differential treatments? (Models blind to all variables, would assign predictions at random and thus be useless)
- Should we maximase opportunity for all or minimize harm for the most exposed?
- Should we enforce differential treatment in the present to beat existing systematic patterns of discrimination, in order to secure fairness in the future, or should we enforce fairness now without resolving the future issues?

As I can see, these questions goes far beyond machine learning and wanders several paces in the world of moral and political philosophy.

**Fairness**: A placeholder term for a variety of normative egalitarian considerations.

### What is Discrimination and what makes it wrong? - skifter lige til dansk 

Diskrimination kan opfattes som forskelsbehandling baseret på medlemskab af ellers grupper, såsom køn, etnicitet eller religion, i en beslutningstagnings proces. 

**Mental state accounts** (Scanlon blandt andet) siger at diskrimination, og det der gør det forkert, er eksistensen af beslutningstagerens systematiske animositet eller preference mellem disse grupper. Altså er det i direkte forbindelse til beslutningstagerens moralske karakter. Systematisk diskrimination vil altså ikke altid falde ind under denne paraply af diskriminationdefinitioner, også selvom det, at man overser denne forskelsbehandling (ignorant ondskab), tælles med som en underbevist forskelsbehandling. 

Under disse accounts er diskrimination ikke naturligt overført til prædiktive modeller - men proponenter, vil sige at
1. Designeren af ML udviser en diskriminativ faveur ved ikke at inkorporere disse anti-diskriminatoriske elementer i modellen
2. Den data der bruges til at træne modellen, er et produkt af en stor population af holdninger, der kan indeholde diskrimination, der så inkorporeres i modellen - Systematisk **bias**

**Når individer ikke behandles sådan** er en anden definition - se statistisk evidens artiklen. 
Diskrimination eksisterer og er forkert, når der infereres viden om et individ på baggrund af generalisering om hvilke grupper individet er medlem ad. Dette er specielt relevant ift. statistisk diskrimination - ofte i forlængelse af systematisk diskrimination. 

Det kan være enormt svært at formaliserer hvorfor kravet om at individer behandles sådan er en nødvendighed, men det føles intuitivt for enormt mange af os - se Epistimologien om statistisk evidens. Hvis dette er et helt generelt krav - ikke blot til for eksempel retsager - så trækker det hele eksistensgrundlaget væk under prædiktive modeller, de de helt generelt opererer på basis af statistisk evidens.

En kritisk af dette kriterier for diskrimination er bredden - det rammer ikke kun forskelsbehandling mellem mere "beskyttede" grupper, etnicitet, køn, religion, men også mange andre faktorer, som man i nogen grad kan have kontrol over som individ. 
(Eksempel: selv en optagelsesprøve er en form for generaliserbarhed mellem individer, så hvor går grænsen?)

Man kan snakke om et form for trade-off mellem præcision og forskelsbehandling - maksimer det første og minimer det andet

### Egalitarisme - Elsker at den politiske filosofi tager over forresten
Alle mennesker skal behandles **ligeligt** - Hvordan dette skal fortolkes har sådan cirka ti millioner forskellige stemmer (Lige fordeling af goder, lige fordeling af muligheder, lige fordeling af rettigheder?)

Generelt mapper ML-modeller et individ til et kategorisk output: Godkendelse/afslag, bail/jail, høj/lav rente - Ofte har disse modeller altså en indflydelse på fordelingen af forskellige "valutaer": Økonomiske resourcer, individuelle muligheder. Hvilke valutaer der skal fordeles efter egalitaristiske principper er et diskuteret emne - se ovenover. 

Der er også stor forskel på lige udfald af fordeling og lige muligheder for fordeling - Hvilken lighed man er interesseret i afhænger af såkaldte **spheres of justice**, altså hvilken kontekst fordelingen finder sted (Democratic justice, ecnomic justice, social justice, etc.) - fordelingen af den demokratiske stemme bør være lige for udfald, mens fordelingen af sociale relationer bør være lige for muligheder, da de befinder sig i to forskellige *spheres*.

**Luck egalitarianism** - som jeg tror de fleste af os er enig i i nogen grad - Beskriver at der bør påtvinges lighed på basis af de ting der er et resultat af *held*, som vi ikke selv er i kontrol over - vores medfødte helbred, vores etnicitet, indfødte sociale klasse, etc. - mens de ting der er et resultat af vore frie valg godt må blive mødt med belønning eller straf. 
Problemet er at det kan være en umulig opgave at identificerer og sorterer kvaliteter som er et resultat af held fra de andre.

Et eksempel er COMPAS - ikke grundet dets statistiske forskelsbehandling mellem etniciteter, men det generelle måde at give score på baggrund af variabler, der er et resultat af held (Uheld måske): sociale cirkler, familie, nabolag - som ikke nok med at de eksisterer som en proxy for etnicitetsparametre, så bryder de også med luck egalitarismens principper.

**Deontic justice** fokuserer på, hvordan en ulighedstilstand blev produceret, snarere end uligheden i sig selv . Denne tilgang kræver, at man inddrager **historisk og sociologisk kontekst** for meningsfuldt at kunne vurdere, om en given ulighed er unfair. I ML er dette vigtigt, da det betyder, at man ikke blot kan tage statistiske fakta for givet; man skal spørge, om det kan retfærdiggøres - igen tilbage til om hvorvidt den statiske diskrimination bygger på et systematisk biased datasæt. 
En deontisk tilgang antyder for eksempel, at hvis ulige base rates i COMPAS-scoringer forhindrer, at forskellige fairness-målinger kan opfyldes samtidigt, skal opmærksomheden rettes mod de **historiske årsager** til disse ulige base rates

**Distributivt vs repræsentativt fairness** er distinktionen mellem lighed mellem individer og lighed med repræsentationer for grupper af individer, for eksempel etniciteter, sprogbrugere, aldersgrupper, religioner. Det kan helt simplificeret ses eksempelvis i det amerikanske parlament, hvor der er en distributiv fairness på tværs af befolkning i repræsentanternes hus (I princip, ikke i realitet), mens senatet udgør en repræsentativ fairness i form af at alle de forskellige befolkningsgrupper, der udgøres af staterne, bliver politisk ligeligt fordelt. (Dette er ikke en holdning pro det amerikanske politiske system - thank fuck, men et fint eksempel på forskellen)

Summa summarum data-scientists prøver at fixe et problem, som de slet ikke forstår det fulde omfang af (hvis nogen gør overhovedet), men vi er nødt til at inkorporer disse moralske og politiske principper og tankegange i implementeringen af prædiktive modeller, hvis det er noget vi skal bruge overhovedet (jeg er ikke overbevist)