#Algorithms #TimeComplexity #DataStructures #Coding 
Læs opgaver grundigt inkl. små detaljer.
Husk geometriske serier er bagerst i CLRS.

Logaritme-regneregler:
$\log(a^r)=r\log(a)$.

2-tals logaritme:
$\lg_2(2^n)=n \lg_2(2)= n \cdot 1=n$.
$2^{\lg_2(n)} =n$.

## Korrekthed (invarianter) og Køretid
Korrekthed (invariant): Hvad gælder efter en iteration $i$?
Hvis loop fra $i=1$ til $n$ gælder følgende invarianter:
- $i\ge 0$ og $i\le n$.

**Køretid:**
Antal iterationer i et loop fra $i=a$ til $b$ er $k=b-a+1$.
Hvis en funktion eller en anden løkke kaldes inde i en løkke (fx fra $i=1$ til $n$), så skal man summere over denne funktion fra 1 til $n$.
- geometriske serier fx eksponentiel (domineres af sidste led)

**Asymptotisk notation:**
Store-O: øvre grænse (vokser højst som).
- $O(g(n))=\{f(n): c, n_0 > 0\}$ s.t.  $$0 \le f(n) \le c \cdot g(n)$$for alle $n \ge n_0$.
- Strammere grænser vokser langsommere. Altså $O(1)$ er strammere end $O(n)$. Fx hvis $O(1)$, så automatisk $O(n)$. 
- $O(1) \in O(\lg n) \in O(n) \in O(n \lg n) \in O(n^2)$
- (Hvis funktionen vokser hurtigere, så er algoritmen langsommere)

Store-Omega: nedre grænse (vokser mindst som).
- $\Omega(g(n))= \{f(n): c, n_0 > 0\}$ s.t.  $$0 \le c \cdot g(n) \le f(n)$$for alle $n \ge n_0$.
- Strammere grænser vokser hurtigere. Altså $\Omega(n)$ er strammere end $\Omega(1)$. Fx hvis $\Omega(n)$, så automatisk $\Omega(1)$.
- $\Omega(n^2) \in \Omega(n \lg n) \in \Omega(n) \in \Omega(\lg n) \in \Omega(1)$
- (Hvis funktionen vokser langsommere, så er algoritmen hurtigere)

Theta: tight bound (både O og Omega).
- $\Theta(g(n))= \{f(n): c, n_0 > 0\}$ s.t.  $$0 \le c_1g(n) \le f(n) \le c_2g(n)$$for alle $n \ge n_0$.

Lille-o: vokser strengt langsommere.
Lille-omega: vokser strengt hurtigere.

Relativ vækst huskeregel: $$\log^k n << n^{\epsilon} << n^k << c^n$$
**Stirling facts:**
$n!=o(n^n)$
$n! = w(2^n)$
$\lg n(n!) = \Theta(n \lg n)$

## Rekursionsligninger
Master Theorem: $$T(n)=aT(n/b)+ \Theta(f(n))$$Hvor $a$ er antallet af delproblemer, $b$ er faktoren vi dividerer størrelsen af delproblemerne med, og $f(n)$ er omkostningen af operationerne uden for det rekursive kald (fx splitte og kombinere).
- ved ligninger på substitutionsform kan $a$ være antallet af rekursive kald til samme størrelse fx $n-1$.

Case 1: $f(n)$ vokser langsommere end $n^{log_b a}$ (Store O).
- Løsning: $T(n)=\Theta(n^{log_b a})$
Case 2: $f(n)$ vokser lige så hurtigt som $n^{log_b a}$ (Theta).
- $f(n)$ vokser langsommere end $n^{log_b a} log^k n$ (eller lig med).
- Løsning: $T(n)=\Theta(n^{log_b a} log^{k+1}n)$
- $k\ge 0$ (og $c>0$.)
Case 3: $f(n)$ vokser hurtigere end $n^{log_b a}$ (Omega).
- Løsning: $T(n)=\Theta(f(n))$


**Hvad vokser hurtigst?**
En polynomiel faktor vokser altid hurtigere end $\lg n$, selv hvis faktoren er meget lille fx 0.043 (fra $log_9  10$).
- $log n = o(n^{\epsilon})$
Man kan finde ud af, hvilken af to funktioner, der vokser hurtigst ved at dividere dem med hinanden og betragte grænse, når $n$ går mod uendelig. For $lim_{n \rightarrow \infty} \frac{f(n)}{g(n)}$ har vi:
- Grænse 0: $f(n)$ langsommere end $g(n)$.
- Grænse konstant $c>0$: de vokser lige hurtigt.
- Grænse $\infty$: $f(n)$ hurtigere end $g(n)$.

**Substitutionsmetoden**:
$$T(n)=a⋅T(n−c)+f(n)$$
Hvor $a$ svarer til antallet af rekursive kald og $c$ til hvor meget vi reducerer problemstørrelsen per kald. $f(n)$ er stadig omkostning per rekursivt kald.

**Generelt for $a=1$:** løsningen er $O(n⋅f(n))$. Vi udfører $f(n)$ arbejde $n$ gange.
For $a\ge 2$: træet $a$-dobles hvert niveau, $n$ niveauer.
- (cirka) generel løsning $O(a^n)$ eller hvis $f(n)$ dominerer (men det gør den ofte ikke).
- Mere præcis: $O((a^{1/c})^n)$.

Hvis rekursiv omkostning er konstant:
$T(n)=2T(n-1)+\Theta(1)$  Løsning: $\Theta(2^n)$.
$T(n)=3T(n-1)+\Theta(1)$  Løsning: $\Theta(3^{n})$.
$T(n)=2T(n-2)+\Theta(1)$  Løsning: $\Theta(2^{n/2})$.
$T(n)=T(n-1)+\Theta(1)$  Løsning: $\Theta(n)$.
$T(n)=T(n-2)+\Theta(1)$  Løsning: $\Theta(n)$.

## Del og Hersk 
Rekursive Algoritmer.
- rekursion håndterer nedbrydning til mindre delproblemer.
- loops kan udføre lokalt arbejde i et rekursivt kald.
- brug rekursionsligninger til at bestemme køretid.

**Merge-sort** (sorteringsalgoritme):
- Merge-sort danner et fuldt binært træ
- Antal indre knuder i et fuldt binært træ er $n-1$
- Antal af rekursive kald til merge-sort er givet ved $2n-1$ (indre knuder + $n$ blade)
	- kan vises ved induktion i $n$
- Antal sammenligninger kan findes ved at håndkøre algoritmen
	- Sammenligningerne kommer først i Merge-delen.
	- Først splittes op indtil blade. Herefter sammenlignes elementer i hhv. venstre og højre del. Hver del sorteres og næste Merge sættes i gang. Man bliver ved med at sammenligne det samme element indtil det skal indsættes i den sorterede del.
- Antal samtidige kald til Merge-sort er antal levels i rekursionstræet / rekursionsdybden (inkl. rod og blade). Fx 3 samtidige kald for 4 elementer og 4 kald for 5 elementer.

**Max-subarray:** Største sum i sammenhængende interval.
Naiv algoritme: $O(n^3)$.
- Beregner 𝑧𝑖𝑗 for alle 1 ≤ 𝑖 ≤ 𝑗 ≤ 𝑛.
Bedre algoritme: $O(n^2)$.
- Bruger prefix sums (for hvert indeks gemmer summen af alle elementer før det indeks). sum(i,j)=P[j]−P[i−1].
- prefix kan fungere ved produkt (hvis ingen elementer er 0): product(i,j)=P[j]/P[i-1].
- prefix XOR: P[j] XOR P[i-1]
- prefix counts: antal 1'er i [i,j] = P[j] - P[i-1].

Optimal algoritme:
Man kan skelne imellem tre typer af optimale løsninger:
1. 𝑖≤𝑛/2<𝑗 (i og j er på hver side af midten)
2. 𝑖≤𝑗≤𝑛/2 (både i og j er på venstre side af midten)
3. 𝑛/2<𝑖≤𝑗 (både i og j er på højre side af midten)

Køretid: $O(n\lg n)$.
- $O(n)$ tid plus 2 rekursive delproblemer hver med størrelse $n/2$.
- $T(n)=2T(n/2)+O(n)$

**Multiplikation af store tal**:

Karatsuba: Reducer fra 4 multiplikationer til 3.
- Skriv tallene som polynomier $x=aB+b$, hvor $B=10^m$ og $m=n/2$.
- $T(n)=3T(n/2)+O(n)$= $O(n^{\log_2 3})$
- hurtigere end $O(n^2)$.
Del: split tallene i halvdele.
Hersk: multiplicer mindre tal rekursivt.
Kombinér: saml resultatet med potenser af 10.

Trin (base 10):
- x=aB+b og y=cB+d.
- z2 = ac
- z0 = bd
- z1 = (a+b)(c+d)
- ad + bc = z1 − z2 − z0
- xy = z2·10^{2m} + (z1−z2−z0)·10^m + z0
## Sortering
Insertionsort er god på næsten sorterede arrays: $O(n)$. Værst ved omvendt sorteret: $O(n^2$).
Heapsort sorterer in-place: $O(1)$ ekstra plads.
- køretid: delarray på størrelse $k=j-i+1$: $O(k\lg k)$.
Mergesort bruger $O(n)$ ekstra plads.
- køretid: $O(n\lg n)$.
- Merge har køretid $\Theta(n)$.
Quicksort: $O(n^2)$, men avg. $n\lg n$.

Theorem 8.1: Enhver sammenligningsbaseret sorteringsalgoritme kræver $\Omega(n \lg n)$ sammenligninger i værste fald (worst case).
- fx mergesort og quicksort.
## Amortiseret Analyse
Potentialfunktioner er aldrig negative.

Amortiseret omkostning per operation: 
- faktisk omkostning + ændring i potentialfunktion (D er datastruktur).
- kan også bestemmes ved: Total omkostning delt med antallet af operationer.

Amortiseret omkostning for $n$ operationer:

Den totale amortiserede omkostning giver en øvre grænse for den totale faktiske omkostning.

**Dynamiske tabeller:**
Table-Insert:
- Potentialefunktion: $\Phi(T)=2(T.num - T.size/2).$ Hvor $T.num$ er antallet af elementer i tabellen efter $i$ og $T.size$ er kapaciteten lige nu.
- Kapaciteten af tabellen fordobles netop når den er fuld, og dermed er tabellen halvt fuld efter udvidelsen. Vi har $T.size=2T.num$ (maks. kapacitet). Dermed er potentialet 0 efter en udvidelse.
- Potentialet er størst lige inden udvidelse. Vi har $T.num=T.size$ (maks. antal elementer i tabellen). Ydermere har vi $T.num = O(i)$.
- Potentialefunktion efter $i$ Table-Insert operationer: $\Omega(1)$ og $O(i)$.
	- under selve Insert-operationen når potentialefunktionen 0, men efter har den 2 for det nye indsatte element.
- Amortiseret omkostning: $O(1)$.

Invarianter for dynamiske tabeller og Table-Insert:
- $T.size ≤ 2 · T.num$
- $T.num ≤ T.size$

**Med Table-Delete:**
Potentialfunktionen:


Vi har $\Phi(T)\le T.size$ og $\Phi(T)=0$ når $\alpha=1/2$.
Når $\alpha\ge 1/2$ har vi Insert +2 og Delete -2.
Når $\alpha<1/2$ har vi Insert -1 og Delete +1.


Amortiseret omkostning stadig $O(1)$?

**Binær-tæller:**
Potentialefunktionen er defineret ved antallet af 1’taller i binær-repræsentationen af $i.$
Efter $i$ Increment operationer:
- Den øvre grænse for potentialefunktionen er $O(\lg(i))$.
	- Antallet af 1’taller i binær repræsentation af $i$ kan højst være $k$ (antallet af bits) og mindst være 0 (hvis i = 0 og vi startede ved 0). Derfor $0 ≤ Φ(D_i) ≤ k.$
	- En k-bit counter kan max repræsentere tal op til $2^k − 1$ (hvis $i = 2^k$ kræves en ekstra bit). Altså må $i ≤ 2^k − 1$ og $i ≤ 2^k − 1 ⇔ \lg(i + 1) ≤ k.$
	- Derfor skal $k$ mindst være $k = ⌈\lg(i + 1)⌉$. Vi får dermed en tilstrækkelig øvre grænse: $0 ≤ Φ(D_i) ≤ ⌈\lg(i + 1)⌉.$
- Vi kan ikke begrænse potentialefunktionen nedefra, da vi har skiftevis store og små værdier, når $i$ bliver større.
- Amortiseret tid: $O(1)$ per Increment (gælder også Decrement).
Potentialefunktionen for Increment er høj ved $2^k -1$ og ved $2^k$ for Decrement.
- Hvis de bruges skiftevis får vi $O(k)$, altså kun de dyre operationer.
Kan generaliseres til andre base-$k$ tællere.

## Fibonacci Hobe
Min-Heap ordnede:
- Ethvert barns nøgle er mindre end (eller ens med) forælderens nøgle.
- IKKE venstre/højre sorteret.
Consolidate: Sørger for øvre grænse på antal børn $D(n)$. Ingen rodknuder må have samme antal børn.
- $D(n)=O(\lg n)$. Dermed er den amortiserede omkostning af at udtrække minimum knude $O(\lg n)$.
- Hvis ikke vi laver Consolidate kan den amortiserede omkostning blive $O(n)$.
	- Fx lav $n$ Insert operationer -> $n$ knuder i rodlisten. Kald Extract-Min $n/2$ gange. 
	- Altså hver Extract-Min skal gennemløbe hele rodlisten for at finde det nye minimum, hvilket koster $O(n)$ per kald. Dette resulterer i $\Omega(n^2)$. Del med antal operationer $n/2$ og vi får $O(n)$ amortiseret.

Køretider per operation:

Potentialefunktion:
- $\Phi(H)= t(H) + 2m(H)$, hvor $t(H)$ er antallet af træer i rodlisten og $m(H)$ er antallet af markerede knuder.
- $0\le \Phi(H) \le n$. Dermed $O(n)$. Hvis alle nøgler er sit eget træ og dermed er ingen knuder markeret.

Markerede knuder:
- En knude markeres, hvis den ikke er en rod og et af knudens børn er blevet fjernet ved en Decrease-key.
- Markeringen fjernes, hvis knuden bliver en rod (fx ved Cut) eller knude blive fjernet fra sin forælder (ved Cascading-cuts).
- Hvis en knude er markeret, så har den mistet præcis ét barn.

Tidsforbrug af Extract-Min efter en operation der omdanner H til H':
- total amortiseret omkostning er øvre grænse på faktisk omkostning.
- $O(\lg n + Φ(H) − Φ(H')) \in O(n)$, da $Φ(H) − Φ(H') \in O(n)$.

## Induktionsbeviser
Base case + induktionsskridt.
Ved iterationer: antag for $i$ og se på evt. cases af, hvad der sker for én iteration.
Kubiksætning: $(n+1)^3=n^3+3n^2+3n+1$.
## Dynamisk Programmering
Optimal delstruktur.
Overlappende delproblemer:
- Samme udregning opstår flere steder i rekursionstræet.
- Løsning: Memoisering.
Ofte skal rekursionsligningerne fra de originale problemer benyttes igen med en (simpel) modifikation. Dermed kan man også evt. bruge samme analyse til fx køretid eller korrekthed som CLRS.

**Rod-cutting:**
Den første måde at skære stangen af længde $n$ ud i en stang af længde $i$ og en anden af længde $n-i$ er den optimale. Brug denne til at vælge udskæringer for resten $n-i$.
$r[n]$ indeholder bedste værdi og $s[n]$ indeholder lokationen / længden af det bedste første snit.

Top-down (start med $n$).

Rekursionsligning: $r_n =\max(p_i+r_{n-i} : 1 \le i \le n)$.
- maksimer fortjeneste: fortjeneste af først cut $p_i$ + den optimale fortjeneste af den resterende længde.
- hvert $i$ er længden af det første stykke, vi skærer af fra venstre.
- der er præcis ét snit i hvert rekursivt kald.

Dynamisk løsning (CLRS):

Bottom-up (start med korteste længder): køretid $\Theta(n^2)$.
evt. Top-down (start med $n$).

Alternative variationer:
- Farvet stangudskæring (hvis forrige stykke rødt, skal det næste være blåt).

**Longest common subsequences (LCS):**
Rekursionen går baglæns. Vi starter med det største problem og arbejder ned mod basistilfældene.
Rekursionsligning for længden af en LCS:

Midterste = Match.
- gå ét skridt ned i begge dimensioner.
Tredje = Ingen match - vi prøver at springe $x_i$ eller $y_i$ over og vælger den bedste. Vi leder efter næste match.
- gå først et skridt ned i X og så prøv med Y. Vælg det bedste.


Køretid: $O(mn)$, hvor $m$ er antal bogstaver i X og $n$ er antal bogstaver i Y.
- hver tabel indgang tager $\Theta(1)$ at beregne.

Alternative variationer:
- LIS: Longest Increasing Subsequence (og længste ikke-aftagende delsekvens)
- LCS uden gentagelser

**Matrix-Chain-Multiplication:**
Bedste måde at sætte parenteser for at minimere omkostning af multiplikationerne.
Rekursionsligningen:


Dynamisk løsning (CLRS):
Algoritmen returnerer optimal parentes struktur (s) og minimum antal multiplikationer (m).
- s[i,j]=k
- Vi splitter mellem $A_k$ og $A_{k+1}$.


Køretid: $\Theta(n^3)$ og plads $\Theta(n^2)$.

Alternative variationer:
- Find værste måde at sætte parenteser.

## Grådige Algoritmer
Optimal delstruktur og Greedy Property.

**Huffmann Koder:**
Sæt laveste to frekvenser sammen hver gang.
- Husk at se om summen af to mindre frekvenser stadig er mindre end de mindste ubrugte frekvenser.
Omkostning af træet (antal bits det kræver at indkode):


Grådig løsning:


Køretid: $O(n\log n)$.

Alternative variationer:
- Minimal omkostning af koden.
- Byg koden.

**Aktivitetsudvælgelse:**
Originalt problem: Så mange som muligt.
- vælg altid ikke-overlappende aktivitet med tidligst sluttid (Theorem 15.1).
- top-down: tag et valg, herefter løs delproblemer.
- rekursiv algoritme: $O(n\lg n)$ for sortering men $\Theta(n)$ hvis sorteret ift. sluttider.
- iterativ algoritme (antager også stigende sluttider): $f_k= \max\{f_i:a_i\in A\}$. Også $\Theta(n)$.
- så mange som muligt i en sum: altid fjern største element først.

Rekursionsligning:


Grådig løsning (iterativ):
Antager sorteret input ift. sluttider.


Køretid: $\Theta(n)$ (hvis sorteret, ellers $O(n\log n)$).

Aktivitetsudvælgelse med pause på 1 imellem: grådig.

Alternative variationer (dynamiske): 
- Weighted activity selection: maksimer summen af vægtene (dynamisk).
	- $OPT(j)=\max(p_j​+OPT(p(j)), OPT(j−1))$
	- Sortér aktiviteter efter sluttid.
	- For hver aktivitet j, find p(j) (kan gøres med binær søgning i O(nlog⁡n)).
	- Kør DP-formlen ovenfor.
	- OPT(n)= maksimal profit.
-  Maksimer samlet længde af aktiviteterne (vægten er længden her).

**Knapsack problem:**
Brøker: grådigt.
- vælg altid den dyreste ting.
0/1 maks. antal objekter: grådigt.
- vælg altid objekt med mindst vægt.

0/1 knapsack dynamiske versioner:
Maksimer værdi:
- $K(i,w)$ er den optimale værdi med de første $i$ ting og vægtkapacitet $w$.

- case 1: ingen værdi eller ingen kapacitet
- case 2: den i'te ting er for tung
- case 3: vælg bedste løsning af ikke tag med (forrige løsning) vs. tag med (værdien lægges til og vægten trækkes fra kapaciteten).
- køretid $O(nW)$.
Antal måder (øl-opgaven): 
- Hvis vi kigge på antallet af måder, hvorpå vi kan bruge kapaciteten kan vi summere $K(w,i-1) + K(w-w_i,i-1)$ og ændre basis tilfælde til $N(0,i)=1$.
Unbounded knapsack: 
- Minimalt antal mønter til at bruge et beløb $b$: $\min(1 + M[b - v[i]])$, hvis $b>0$, hvor $v_i$ er værdien af den sidst brugte mønt.
- Gentagen produktion.
Multipel Choice Knapsack:
- Objekterne er opdelt i grupper, og man må vælge præcis ét objekt fra hver gruppe.
Maksimer: Primært antal objekter, sekundært samlet værdi.
Bin-packing:
- Hver bin har $C$ kapacitet. Vi har $n$ objekter hver med en vægt $w_i$, der alle skal være i en bin. Minimer antallet af bins.
## Search Trees
Et træ har altid $n-1$ kanter, hvor $n$ er antal knuder.
Binary Search Trees: max to børn.
- kan bruges til at finde max og min i $O(h)$, hvis sorteret.
	- bedste tilfælde: $O(\lg n)$. Værste tilfælde: $O(n)$.
	- inorder traversal giver sorteret rækkefølge
- søg i et sorteret array $x$ efter et sammenligningselement $k$.
- floor = den største værdi, der ikke overstiger $k$.
- ceiling = den mindste værdi, der er lig med eller overstiger $k$.
- AVL træer er balancerede $O(\lg n)$.
Diverse funktioner ved søgetræer:
- Tree-Search.
- Tree-Successor funktion (den nærmeste mindre værdi er forgængeren).
- Tree-Minimum og Tree-Maximum (find hhv. mindste og største nøgle i et træ).
- Tree-Insert og Tree-Delete.

Algoritmer:
Køretid $O(h)$, hvis balanceret $O(\lg n)$.
## Red-Black Trees
Balanceret binært træ (AVL træ): Dybde af T er højst $2 \log (n +1)$, hvor $n$ er antallet af knuder i træet. Insert, Delete, Search: $O(\lg n)$ pga. max dybden.
Ved Insert farves knuden først rød og får 2 NIL blade.
Global invariant: venstre barn er mindre end forælder og højre barn er større.

**De fire egenskaber:**
- Roden er sort.
- Bladene er sorte.
- Røde knuder har altid to sorte børn.
- Black Height: $bh(v)$. For alle $v$, så indeholder alle stier fra $v$ til blad det samme antal sorte knuder. Den sorte højde af en knude $v$ er antallet af sorte knuder på vej ned igennem en vilkårlig sti fra $v$ ($v$ ikke medregnet).
	- derfor er højden af et blad lig med 0.

Claim: For alle $v$:
- Størrelsen $|T_v|\ge 2^{bh(v)}-1$.

Invarianter:
- Højden og den sorte højde er altid den samme for et blad (højden er 0, da blade ikke har nogen børn).
- Antal røde knuder er altid mindre end antal sorte knuder (inkl. blade). 

**Rotationer:**
- Left-Rotation: $x.right = y.left$ og $y.left = x$.
- Right-Rotation: $y.left=x.right$ og $x.right=y$
- Højden af træet kan ændre sig ved en rotation.

## Algoritmisk Geometri
Konveks hylster (CH):
- den mindste konvekse mængde (polygon: alle vinkler mindre end 180 grader), der indeholder M. Vi må ikke "gå ind" i polygonet igen. Eksempel: M er en cirkel, CH(M) er en disk. Mængden M er en del af CH(M).
- nedre grænse for beregning: $\Omega(n \lg n)$ pga. sortering.
- ønske: kun skarpe venstre sving (hvor vinkler mindre end 180 grader).
- $p_1$ er altid med.

**Grahams scan:**
Tager altid $O(n \lg n)$.

**Jarvis' March:**
Tager $O(nh)$, hvor $h$ er antallet af hjørne i det konvekse hylster.
Jarvis’ march tager tid $\Theta(n^2)$ på et værste input med $n$ knuder.
- når $h=\Theta(n)$.
- Jarvis er hurtigere end Grahams når $h=o(\lg n)$.
## Minimum Spanning Trees (MST)
Kruskal: Grådige algoritme.
- Vælg altid den lavest vægtede kant, der ikke laver en cycle.
- Køretid: $O(E \lg V)$
Prim: Udvid forbundet MST.
- Roden tages først ud af prioritetskøen.
- Herefter vælg lavest vægtede kant fra rod til naboer.
- Dernæst betragt lavest vægtede kant fra rod og fra den valgte nabo. Vælg den laveste der ikke laver en cycle.
- Køretid: $O(E \lg V)$. Hvis Fibonacci heap til implementering af min-priority queue: $O(E+V \lg V)$.

**Snit og kanter**
Snittet respekterer $A$, hvis ingen af kanterne i A krydser snittet. 
- fx hvis begge endpoints i alle kanter ligger i snittet.
- fx hvis ingen endpoints i alle kanterne ligger i snittet.
En kant $(u,v)$ er sikker for $A$ (hvor $A$ er en delmængde af et MST), hvis et snit $(S,V\setminus S)$ af $G$ respekterer $A$ og $(u,v)$ er en let kant, der krydser snittet (CLRS Theorem 21.1). 
- hvis kanten er i MST, så er den sikker for A.
## Shortest Paths
 $G^′$ er et normalt træ med $s$ som rod.
I et shortest path tree $G'$, så kan alle knuder i $V'$ nås fra $s$.
Knuden $s$ har kun udgående kanter.
$G'$ har $|V'|-1$ kanter.
$G'$ indeholder ikke nødvendigvis den kant i $G$ med den laveste vægt.
- der kan være en kant, der ikke kan nås fr $s$.
Enhver sti i $G^′$ er en korteste vej i G.
Der kan være flere korteste veje.

Dijkstra: kun ikke-negative vægte.
- Køretid: $O(V^2)$ med simpel implementering. $O(E+V \lg V)$ med Fibonacci heap.
Bellman Ford: kan håndtere negative vægte, hvis ingen negative cycles.
- Køretid: $O(V * E)$.
## Parallelle Algoritmer
Spawn og sync.
CLRS og slides: Sum-algoritme, Fibonacci algoritme, Merge-sort algoritme, Matrix-multiplication algoritme.
Hver opmærksom på om operationerne angives som de serielle eller parallelle.

Arbejde $T_1$ = køretiden af den parallelle algoritmes serielle projektion.
- fx $T_1$ af P-Naive-Merge-sort er $\Theta(n\lg n)$ da Merge-Sort er dens serielle projektion og worst case running time er $O(n\lg n)$.
Span $T_{\infty}$ = længste kritiske sti / længste sti af afhængige knuder. 
- Span kan bestemmes ved rekursionsligning. Ofte fx højde af et træ, men ikke altid.

*Span law* siger, at spandet $T_{\infty}$ angiver den absolutte nedre grænse for køretiden, uanset hvor mange processorer man tilføjer.
_Work Law_ siger, at køretiden på $p$ processorer aldrig kan være mindre end det totale arbejde divideret med antallet af processorer ($T_p \ge T_1/p$).

**Brent's Theorem** (kombineret med work og span law):
$$\max(\frac{T_1}{p}, T_{\infty}) \le T_p \le \frac{T_1}{p} + T_{\infty}$$
Brents theorem giver den øvre grænse for køretiden. En grådig scheduler er aldrig mere end end faktor 2 fra optimalitet.
Parallelisme: $c=\frac{T_1}{T_{\infty}}$ (maksimale antal $c$ processorer der giver meningsfuld speedup).

## Disjunkte mængder
CLRS 19.3 (trærepræsentationer) og 21.
Til at kombinere to undertræer via. Kruskals. Effektiv til at håndtere forbindelsesproblemer i grafer. Understøtter union og find operationer.
- kan bestemme om en kant lukker en cycle i en forest F.

Make-set: $O(1)$.

**Heuristikker for bedre køretid:**
Union by rank (minimer højden af træet): 
Rank er en øvre grænse for højden.
- Union(x,y): $O(\lg n)$.
- Union(x,x): laver to kald til Find-Set(x) og så returnerer.
- Uden *path comprehension*: Find-Set(x) tager $O(n)$.

Union by rank alene (træer): $O(m \lg n)$ for $m$ operationer, hvor $n$ er Make-Set.

Link(x,y):
Rank sættes til højeste af de to sæt, der kombineres.
Rank stiger med én, hvis x.rank=y.rank.

Path comprehension (fremtidige kald bliver hurtigere):
- Find-Set(x): $O(\lg n)$.
- Hvis Find-Set(x) allerede er blevet kaldt én gang, så tager de resterende kald konstant tid.
- Uden *union by rank*: Union(x,y) tager $O(n)$.
