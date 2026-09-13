Tags: #AlgorithmicBias, #Fairness, #AI

Artiklen er helt generelt et forslag itl hvordan vi omgår de sociale feddback-loops som forårsages af statisk implementerede statistiske modeller. 

Forfatterne viser gennem eksempler, hvordan **interventioner, der ser “fair” ud i et datasæt**, kan få **modsatte effekter** i praksis. Et lån, der gives for at øge adgang til kredit blandt minoritetsgrupper, kan på længere sigt forværre deres økonomiske situation, hvis den sociale kontekst ikke er stabil. Ligeledes kan fairness-krav i ansættelsesalgoritmer skabe **utilsigtede incitamenter** eller forskydninger på arbejdsmarkedet, som underminerer retfærdighed på længere sigt.

Kort sagt: fairness-metrikker ignorerer de **dynamiske effekter** af implementering i virkelige sociale systemer.

Artiklens hovedbidrag er forfatternes forslag om at forstå og vurdere retfærdighed som et **dynamic trajectory** (Kan fortolkes som en række diskrete delpunkter) frem for som et enkelt slutmål eller et engangsevalueret resultat. De peger på tre dimensioner, hvori sådanne trajectory bør vurderes:

**Temporal dynamik**
Vi må forstå, hvordan retfærdighed udvikler sig over tid. Det handler ikke kun om, hvorvidt et system i sidste ende bliver fair, men også hvordan og hvor hurtigt forandringen sker, og hvilke midlertidige uretfærdigheder der opstår undervejs. Etisk set må vi tage stilling til, hvor store midlertidige uligheder vi kan acceptere for at nå et mere retfærdigt mål - Det er reelt et **tradeoff problem.**

Derudover skal vi tage højde for epistemiske hensyn – **nogle gange må vi acceptere midlertidige fejl eller skævheder for at lære, hvordan systemet fungerer**, og forbedre det på længere sigt. (Prioriterer en nutidig unfairness for at sikre en fremtidig fairness)

Desuden er det fejlagtigt overhovedet at tale om et "endemål". Sociale dynamikker og etiske problemstillinger stopper aldrig med at forandre sig (I manges optik inklusiv min egen i hvert fald) - **"The language of 'reaching the ideal target state' presupposes a false finality"**

Basically: Vi skal ikke spørge os selv blot om en given algoritme leder til en fair dom, men i stedet spørge os selv om hvorledes vi kan udvide vores viden om sociale systemer på en måde der kan lede til mere fairness i fremtiden, og hvad vi er villige til at ofre for det.

**Robusthed**
Et andet vurderingskriterium er robusthed – altså hvor modstandsdygtig en fairness-intervention er over for ændringer i omgivelserne, andre agenters ageren. En retfærdighedsstrategi, der kun fungerer under ideelle betingelser, er skrøbelig. Derimod kan en mindre perfekt, men robust politik være mere etisk forsvarlig, fordi den fortsat fremmer retfærdighed under realistiske, ustabile forhold.

Dette rejser også dilemmaer: Skal man tage højde for forventeligt uretfærdige handlinger fra andre aktører? Hvis man justerer sin politik efter andres uretfærdighed, risikerer man selv at blive medskyldig – men hvis man ignorerer den, kan indsatsen mislykkes.

**Eksempel**: Jobansøger A er bedre i flere kriterier end Jobansøger B, men jobbet vil eksponere den ansatte for et racistisk miljø, og A er af anden etnisk baggrund - Formentlig vil A forlade jobbet, hvilket i sidste ende vil være en dårligt forretning for virksomheden og en dårligt oplevelse for A, men hvis de i stedet hyrer B vil de være medskyldige i den selv samme racisme ("Jeg gjorde det af gode årsager" - stfu racisme undskyldes aldrig)

**Repræsentation og perspektivmangfoldighed**
Endelig påpeger forfatterne, at vores vurderinger af fairness-trajectories afhænger af hvordan vi modellerer verden, hvilke faktorer og relationer vi medtager, og hvilke vi udelader. Disse valg er i sig selv værdiladede. Derfor må moralfilosofi og teknisk design integreres, og forskellige samfundsgrupper bør inddrages i modelleringen for at sikre, at de normative og epistemiske perspektiver er mangfoldige.

Derved bliver fairness ikke et teknisk spørgsmål om statistik, men et kollektivt og demokratisk projekt om, hvordan vi forstår og styrer udviklingen af sociale systemer. (Lidt flødeskum-og-kirsebær-på-toppen konklusion, der ikke reelt konkretiserer den nødvendige proces)

