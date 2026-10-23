---
layout: default
title: "DNA Mutations and Repair"
---

Tags: #CellBiology #Genetics 

DNA is constantly damaged with 10,000 to 100,000 damages to the DNA per cell per day. Given $3\times10^{13}$ cells in a human this is quite a lot. We have a DNA repair system fixing most of these damages, but some make it through - **mutations**. Whether the mutations happens to **somatic cells** or **gametese (Kønsceller)** makes a lot of difference, as mutations in a somatic cell *can* lead to individual disease, but mutations in gametese (or precursor cells) can lead to disease (maybe precancer mutations) for every child. 

**DNA Repair Mechanisms**
These have kept most of the genes safe for millions of years

The important mechanisms:
- Proofreading
- Mismatch repair
- Excision repair
- Homolog recombination
- Non-homolog endjoining

If DNA is damaged to prospects could be
- Celle death (e.g. apoptosis)
- Cancer by the mutations
- Genetic diseases
- Evolutionary (fordele?)

Mutations in somatic cells are only dangerous to our selves.

### Damage to the DNA
The possible sources of damages can be divided into two categories

**Endogen**
- Errors in DNA replication
- Spontanious in the cell because of metabolism

**Exogen**
- UV and radioactivity
- Chemical

Some of the resulting damages include 
- Lack of a base
- Modification of a base
- Wrong base pair
- Base-dimers (Covalent binding of bases)
- Breakage of one or both strands
##### Errors during the DNA replication
DNA polymerase makes 1 mistake for every 100,000 nucleotides. This is quite a lot, but the **polymerase proofreading** and **mismatch repair** we get to 1 in $10^9$ nucleotides

The first correction mechanism is done by the **DNA polymerase** when synthesizing the strand. This is called **proofreading**. This is done by **another domain** on the polymerase, than the one performing **polymerization**. Just before placing a new nucleotide, the polymerase "checks" whether the bases are a match, and if not, it clips off the mispaired nucleotide and tries again.
- This is only possible because of the direction of the synthesis. If it were to be synthesizes in the 5' direction, then the removal of the wrong nucleotide would result in the strand being blocked by a phosphate.

If the error **gets past proofreading** we can get a **mismatch** (Wrong nucleotide pairing). If such a mismatch is left for further replication, we get different DNA helices with correct parings, but mutated sequences:
![Screenshot 2026-09-26 at 16.07.22](../z-Figures/Screenshot%202026-09-26%20at%2016.07.22.png)

For fixing these wrong nucleotide pairings we have the **mismatch repair system**
The problem is to identify which strand is the **correct strand**, that is the original strand. This is possible because there is a difference between the strands **just after synthesis**. There is **gaps** between the DNA fragments, that have not yet been mended by **DNA ligase**. 
- **Mismatch repair proteins** identifies a hole and scan the newly synthesized strand til it finds an error (A **mismatch**)
- It then removes the entire segment from the error to the hole, which can then be recreated correctly by the DNA polymerase. 
<img src="../z-Figures/Screenshot%202026-09-27%20at%2010.54.49.png" alt="Screenshot 2026-09-27 at 10.54.49" width="558">
##### Spontaneous damage to the DNA
Damages not only happen during replication, but also spontaneously.  

One spontaneous error is **depurination (Depurinering)** where the **$\beta$-glycoside binding is hydrolyzed**, and the **base is released from the nucleotide**

Another is **deamination (Deaminering)** where an **amine group** is removed from the base - swapped with a **ketone** - changing it into another base - **Adenine is deaminated to Guanine**, or **Cytosine is deaminated to Uracil**

![Screenshot 2026-09-27 at 10.58.11](../z-Figures/Screenshot%202026-09-27%20at%2010.58.11.png)

A particularly tough deamination to fix is when **5-methyl-cytosine** is deaminated to **thymine**. Which is almost never fixed.

##### Mutations as a result of environment and actions
This is damages, that aren't spontaneous, but happens as a result of UV, radiation, and chemicals such as in cigarettes, nitrate and nitrite preservative, and barbecuing. 

Particularly UV results in **thymine dimers**. This is a result of two neighboring thymines forming a **covalent bond**, which for example will stall the replication process at the affected side. 
- This can in fact happen for all **prydimidines** (Cytosine, Thymine and Uracil)
![Screenshot 2026-09-27 at 11.05.51](../z-Figures/Screenshot%202026-09-27%20at%2011.05.51.png)
#### Excision Repair
When damage happen to only one of the strands, we use excision repair. This includes multiple processes given the particular damage, but the general process is in three steps

1. The error is cleaved (**excised**)  from the DNA (**Nuclease** activity)
2. The repair **DNA polymerase** fills in the missing part using the other strand as template
3. A **DNA ligase** fills in the nick/gap

The two specific processes used (Excluding Mismatch repair): 

**Base excision repair** happens when there occurs a **mismatch** between the bases in the base pair - for example after **depurination**
- Specific **glycalases** removes the base
- **AP endonuclease** removes the backbone
- **DNA polymerase** synthesizes a new correct fragment
- **DNA ligase** closes the nick

**Nucleotide excision repair** is when there occurs **thymine dimers**
- **Endonuclease** cleaves the DNA backbone around the affected area
- **Helicase** removes the affect DNA
- **DNA polymerase** synthesizes a new correct fragment
- **DNA ligase** closes the nick
#### Double strand cleavage
If both strands are damaged / cleaved, we have **no intact template strand** to repair the DNA. There are two mechanisms for fixing this.

**Nonhomologous end joining** can happen always after an accidental double strand break. It is simply to quickly join the exposed ends together before they drift apart.
- **Nuclease** processes the DNA end, often **removing nucleotides** in order to align the ends. 
- **Specialized DNA ligase** joins the end together
- This results in a repaired DNA string, with some loss of bp and thus **mutations**

**Homologous recombination** can only be used when there is an undamaged DNA clone nearby (Shortly after replication)
- The undamaged DNA can be used as a template 
- We don't need to understand the details!
- **Recombination-specific nucleases** processes 5' ends of the two exposed DNA ends. 
- **Rad52** guides to 3' end to the aligning part of the non-damged DNA strand, where it can be extended by **DNA polymerase**
- The same thing occurs for the other fragment
- **DNA Ligase** merges the nick
- Results in a fully repaired DNA with **no loss of bp**

![Screenshot 2026-09-27 at 11.31.38](../z-Figures/Screenshot%202026-09-27%20at%2011.31.38.png)
##### Mutations accumulates
Many mutations are usually needed to have any real effect, but sometimes single mutations can have en effect on its own
- **A single mutation in a valine** in the $\beta$-globulin gene results in **mutated hemoglobin** and strokes

#### Mutation classification
Looking at the single nucleotide level we have
- **Insertions** - A new nucleotide inserted
- **Deletion** - A nucleotide is removed
- **Base-change** 

When wee look at how these mutations **affect the codons** we have in importance ranking
- **Nonsense** - Encoding a stop codon
- **Missense** - Resulting in a different amino acid
- **Synonymous**  - Resulting in the same amino acid by chance

When looking at the reading frame we have
- **Frameshift** mutations where a number of nucleotides thats not a product of 3 is added/removed - Thus changing every codon
- **Inframe** mutations, where the number **is a multiple of 3**, thus affecting the amino acids in the affected codons, but not shifting the reading frame.

In protein coding genome, **some point mutations doesn't change the protein** at all
- E.g. AAG (Coding for lysine) -> AAA (Also coding for lysine)

##### Mutations in the DNA repair genes
Some of the worst mutations are genes coding for the proteins involved in the DNA repair it self:
- Xeroderma pigmentosum (XP)
- Werner syndrome
- Breast- and ovary cancer (BRCA1/2)
- Prostata cancer (BRCA2)

When the DNA repair proteins fail, the mutations can accumulate far quicker - especially two types of mutations leads to cancerous cells
- **Oncogenes** are genes that if mutates leads to **uninhibited cell division**
- **Tumor supressor genes** are genes that supresses **uninhibited cell division**, but if mutated can't inhibit the tumor.

