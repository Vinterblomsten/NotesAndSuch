Tags: #AlgorithmicBias #Fairness #Discrimination 

**Algorithmic Bias** opstår, når ML-programmer "lærer" af statistiske regelmæssigheder i menneskeskabte datasæt. Programmet opsnapper sociale mønstre, der afspejles i dataene. Biaset er typisk ikke eksplicit indkodet af programmører, men opstår implicit ud af algoritmens drift på dataene.

**Proxy-parametre** er parametre som ofte har en vis korrelation med socialt-sensitive attributter, såsom race, religion eller køn, og som ofte lægger brosten for at et algoritmisk bias finder vej ind i algoritmen gennem et, på overfladen, anonymiseret datasæt (altså fri fra de socialt sensitive attributter)

**Evidence for algorithmic bias**
Diverse eksempler på algoritmisk bias implementeres systemer i virkeligheden: NLP-modeller trænet på internettet, COMPAS, ansigtsgenkendelse, etc.

**Cognitive bias**
Ligesom algoritmer kan menneskelig kognitivt bias også være virkelig **implicit**, hvilket betyder, at den påvirker en persons overbevisninger og handlinger, selvom det ikke er eksplicit repræsenteret i deres kognitive repertoire som en bevidst stereotyp. For eksempel kan en person have et implicit bias om, at ældre mennesker er dårlige til computere, selvom de bevidst afviser denne stereotype. Denne fleksibilitet i biasets struktur og indflydelse på beslutningstagen gælder generelt, uanset om biaset er socialt, moralsk forkasteligt eller ej, og viser, at forhindringer i at afhjælpe skadeligt bias ikke er unikke for det algoritmiske domæne.

**Proxy problemet** består i at der ikke er noget perfekt, algoritmisk løsning på at fjerne alle rester social diskrimination i ML-systemer (Se Fairness in Machine Learning artiklen), uden samtidig at skære kraftigt ned på præcisionen af systemet. Samtidig er en selvforstærkende effekt, hvis socialt-diskriminerende systemer implementeres (positiv feedback mekanisme - ikke positivt i en valensmæssigforstand, men rent teknisk positiv feedback):

Et godt eksempel er ansættelse af kvindligere filosoffer: Hvis man anonymiserer ansøgingen, så køn er skjult, men antallet af publikationer er tilgængeligt, så vil dette antal, der gennemsnitteligt er væsentligt lavere for kvinder, agerer som en proxy for køn. Det virker dog som en meget fair parameter at kigge på antal publikationer, men hvis man tager den allerede eksisterende mandsdominerende struktur i ansættelserne og dermed publikationerne for øje, så bliver det tydeligt, at ansættelse baseret på denne model kun forstærker effekten og dermed problemet, uden at det har rod i nogen form for forskel i akademisk kunden. 

