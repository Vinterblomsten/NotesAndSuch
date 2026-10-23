---
layout: default
title: "DNA Replication"
---

Tags: #CellBiology #Genetics 

The cells of the body is constantly multiplying and being replaced with a total of **$10^{16}$ cell divisions in an average human life**. Before each cell division, the DNA must be copied.

The synthesis must only happen in the **S phase of the cell cycle**, but the processes leading to the replication can happen in earlier phases.

More in the cell cyclus lecture

##### Strands of replication
The **DNA polymerase** does 5'$\rightarrow$ 3' synthesis of the DNA strands, that is it **reads from 3' end to the 5' end** ([Defined by the "free" carbon in the dexoyribose"](DNA_and_Chromosomes.md)), and thus is **synthesized the other way round**: 5'$\rightarrow$ 3'. 
<img src="../z-Figures/Screenshot%202026-09-26%20at%2013.49.59.png" alt="Screenshot 2026-09-26 at 13.49.59" width="436">

The synthesis are said to be **semiconservative**, as each new DNA helix is a result of one original strand and one new one. (Altough in the next generation of DNA, half of the helices are without any of the "grandmother" strands)

##### Replication origins
The replication starts in the **origins of replication** (about 10,000 of them in eucaryote cells, greatly increasing the speed of replication). These replication origins are formed by specific nucleotide codes, with a **majority of A-T pairs**. as they form weaker (fewer) bonds than the C-G pairs, and thus **require less energy to pry apart**. From each of these the replication begins outwards towards both ends.

At each replication origin there forms **two replication forks**, one at each end. As replication moves in both directions it is called **bidirectional** (Nor all organisms use bidirectional replication).
<img src="../z-Figures/Screenshot%202026-09-26%20at%2014.01.26.png" alt="Screenshot 2026-09-26 at 14.01.26" width="331">

The replication forks are **asymetrical** as a resulting of the **antiparallel strands** of the DNA. This means that the one new strand (**the leading strand**) are being synthesized in the same direction (appending the 3' end) as the replication fork movement, whereas the other new strand (**the lagging strand**) are being synthesized away from the replication fork. However, as a result of the movement of the replication fork, this must be done **discontinously** (discretely) in a lot of smaller **okazagi fragements**, that are fused later on. 
<img src="../z-Figures/Screenshot%202026-09-26%20at%2014.27.38.png" alt="Screenshot 2026-09-26 at 14.27.38" width="530">
##### DNA Polymerase
The enzymes responsible for the actual synthesis of new strands are called DNA polymerases. These **catalyze the addition of nucleotides to the 3' end** of a growing DNA strand, using an original strand as a template. 

The to-be-bound nucleotides are present as deoxyribosenucleoside **triphosphates**, which means that **the hydrolysis of the high-energy bond**, cleaving pyrophosphate (Diphosphate), **fuels the forming of the phosphodiester bond** it self, binding the nucleotide to the 3' end of the strand. The pyrophosphate is hydrolyzed again, making the reverse reaction very unlikely.
<img src="../z-Figures/Screenshot%202026-09-26%20at%2014.08.26.png" alt="Screenshot 2026-09-26 at 14.08.26" width="445">
The DNA polymerase can't itself begin a new DNA strand, but merely add nucleotides to the growing 3' end of a strand. DNA synthesis thus requires a **primer** with 3'-OH (That is an exposed 3' end). This primer is **RNA** synthesized by **DNA-primase**. The DNA polymerase can then begin the DNA synthesis at the 3' end of the RNA primer
- On the **leading strand** there is only needed one primer in the beginning, from witch the DNA polymerase can synthesize the new strand continually. 
- On the **lagging strand** the DNA-primase must regularly synthesize new primer, from which the DNA polymerase can backtrack, each resulting in an **okazaki fragment**

<img src="../z-Figures/Screenshot%202026-09-26%20at%2014.50.06.png" alt="Screenshot 2026-09-26 at 14.50.06" width="274">
When the DNA polyemerase reaches the next primer in line (the next okazaki fragment) it stops
- **Nucleases** will then remove the RNA primer
- **Repair polymerase** fills out the exposed segment, until only one phosphodiester bond is missing, between each of the fragments.
- This bond is mended by **DNA ligase** fueled by ATP
##### The Replication Machine 
Firstly (in the $G_1$ phase) two initiator proteins Origine replication complex (**ORC**) and **Cdc6** recognizes and binds to the **origins of replication** sequences
- Two of the proteins **Helicase** binds using ATP, while Cdc6 dissociates. 
- This forms the **prereplicative complex (Pre-RC)** (Maybe also called the initiation complex?)

When the replication is signaled the Pre-RC is **activated by S-Cdk**, and the replication begins. 

The **helicase** slides along the DNA **disassociating the strands** using ATP for energy 
- Behind the helicase the protein monomers **single-strand DNA-binding proteins (SSB)** binds to the lagging string keeping it straight, and thus **keeping the helix from reforming**

A **sliding clamp** is locked around each strand, by the ATP-fueled **clamp loader**. The polymerase is then bound to the sliding clamp, letting it slide along the strand. 

As the helicase dissociates the strands continuously, the **leading strand-polymerase** simply follows while synthesizing new DNA. On the **lacking strand**, a primase regularly synthesizes RNA primers, which is used by polymerase moving in the opposite direction in segments, before returning and repeating (in reality is it the strand that is moving, as the polymerase associates with the helicase complex).

<img src="../z-Figures/Screenshot%202026-09-26%20at%2015.05.13.png" alt="Screenshot 2026-09-26 at 15.05.13" width="439">

#### Complications during replication
During the replication there occurs **supercoiling**, where the DNA wraps around it self (like a cable when wrapping it around) in front of the replication, as the helicase unwraps the helix. This is solved by **topoisomorase I and II**. These enzymes creates a transient cleavage of the helix (one strand for topoisomerase I and the other for II), which allows the DNA to "uncoil" by rotating freely, before putting them back together
<img src="../z-Figures/Screenshot%202026-09-26%20at%2015.07.36.png" alt="Screenshot 2026-09-26 at 15.07.36" width="547">
#### Replication and nucleosomes
The **nucleosomes** dissociates, that is the histones are displaced. After the replication, the **CAF1** and **NAP1** recreates the now duplicated nucleosomes
<img src="../z-Figures/Screenshot%202026-09-26%20at%2015.11.06.png" alt="Screenshot 2026-09-26 at 15.11.06" width="646">
#### Replication of Telomeres
When reaching the end of the DNA in a **chromosome**, the lead strand will finish as it should (The 3' end), but the **lagging strand** will finish with a RNA primer at the end (The 5' end), as there is not previous segment to reach it, and the polymerase can't synthesize DNA instead. 

Without a fix to this, the chromosomes wlil quicly shorten.

The **telomerase** fixes this. At the end of the chromosome, we find a **telomere repeat sequence**. The telomerase extends the repeating sequence on the **lead strand**, such that an RNA primer can be added on complementary to this (**The primer is carried and removed again by the telomerase**), and the DNA polymerase can finish the **lagging strand**
<img src="../z-Figures/Screenshot%202026-09-26%20at%2015.21.25.png" alt="Screenshot 2026-09-26 at 15.21.25" width="565">

In general the **telomeres does becomes shorter** with age
- 15000 bp  from birth
- 7000 bp at adulthood
At som point, there is no more telomerase, and the cells can no longer divide. 
- In cancer cells, the mutations allows the telomeres to keep their length, and thus the cells becomes "immortal"

**Chemo therapy targets topoisomerasem** which means that they can cleave the DNA, but the drugs inhibits the rebinding of the DNA, which means that the DNA is degraded and the cell dies.
- This is smart, because it targets cells with rapid cell division and thus DNA replication - cancer cells

### DNA Cloning (Opformering)
There are $3.2\times10^9$ nucleotides in the human genome, which mean that a primer of length 16 can bind to one single place in the genome ($4^{16}=4.3\times10^9$). This is the principle we use in PCR.

**Polymerase Chain Reaction (PCR)**
A type of polymerase that can tolerate boiling, is the essence of PCR. It is a repeating three step proces:
1. **Denaturing of the DNA** by heat (90 degrees)
2. **Annealing of two primers** One for each end of the segment of interest (60 degrees)
3. **DNA synthesis** (70 degrees)

![Screenshot 2026-09-26 at 15.28.05](../z-Figures/Screenshot%202026-09-26%20at%2015.28.05.png)