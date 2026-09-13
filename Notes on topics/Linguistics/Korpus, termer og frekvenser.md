#Language 
- Hvor stort er ordforrådet i et korpus? - Heaps lov
- Hvor hyppige er de enkelte ord i korpus i forhold til hinanden? - Zipfs lov
- Hvilket ord er signifikante, dvs. siger noget vææsentligt om indholdet? - Termvægt tf\*idf
	- Om et ord et frekvent betyder ikke at det er signifikant
- Hvordan kan termvægt bruges til søgning i tekst? - Cosinus similarity
	- Hvordan kan man sammenligne vektorer for ord i et vektorspace

##### Heaps lov
Stigningen i ordforråd når korpus vokser, kan beregnes med følgende formel
$$v=k\times n^\beta$$
hvor $v$ er ordforrådsstørelse, $k$ og $\beta$ passer til forskellige sprog og: $10<k<100$ , $\beta\approx0.5$ og $n$ er antal ord i korpus.

Altså: Mængden af nye ord i ordforråd stiger hurtigt i starten, men væsentlig mindre når korpus bliver stort nok.

Øvelse: Hvor mange ord kan vi forvente i tekst klimaforandringer.txt: cst.dk/bolette/inform
![[Screenshot 2026-03-03 at 13.50.46.png| 300]]
Cirka 163 med 266 ord i alt

#### Zipfs lov
Hvad kan vi sige om ords **frekvens** i et korpus? - De er skævt fordeligt!
Frekvensen af et ord er næsten omvendt proportional med dets rang (i hyppighed)
$$freq\times rang \approx c$$
Hvor $c$ er en konstant, på tværs af ord i korpus. 20% mest frekvente termer dækker over ca. 70% af et dokument. 

#### Termvægt
Hvordan beregner vi ords semantiske vægt/signifikans i et givent dokument?
Vigtige faktorer
- Frekvens i dokumentet
- Hvor mange andre dokumenter optræder det?

Andre faktorer
- Former, synonymer, semmsnsætninger
- Funktionsord vs indholdsord

Formel for det
$$
idf_i=\log(N/n_i)
$$
Hvor N er det samede antal dokumenter og $n_i$ er antallet af dokumenter hvor termen optræder.
Kombineret med: $tf_i$ Som er den rå frekvensvægt / den absolutte frekvens får vi vægten:
$$
w_{i,j}=tf_{i,j}\times idf_i=tf_{i,j}\times \log(N/n_i)
$$

