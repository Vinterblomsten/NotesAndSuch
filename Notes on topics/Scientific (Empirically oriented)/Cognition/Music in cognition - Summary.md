#MusicalCognition #Cognition #AI #Neuroscience 

![[Screenshot 2025-12-20 at 10.55.58.png]]

**Music in cognition**
- **Amusia**: congenital, developmental, or acquired disorder affecting the processing of pitch information.Colloquially, amusia is referred to as ‘tone-deafness’.
- **Auditory scene analysis**: grouping of individual elements of auditory environments into discrete perceptual units (i.e., objects and streams), namely, sound segregation. Auditory scene analysis is considered the fundamental psychological process of audition across species.
- **Automaticity**: property of cognition wherein a process is undertaken via implicit knowledge, without requiring intervention or explicit understanding
- **Beat**: the pulse, a periodic, repetitive stimulus that forms the basic rhythmic foundation of music; it is usually **isochronous** (i.e., with an immutable period length).
- **Cocktail party problem**: the problem of auditory scene analysis in natural auditory environments where many sounds co-occur but the listener must focus on only one of them, as at a cocktail party; the phenomenon includes both sound segregation and the direction of attention to the sound source of interest.
- **Encapsulation**: property of cognition wherein a process has some degree of impenetrability, in that it is unalterable by beliefs, desires, or knowledge, and does not rely on information from other processes.
- **Groove**: property of some forms of music that prompts dance and other rhythmic movement from listeners and/or performers.
- **Melodic contour**: directional pattern of a melody relative to its tonal content, as opposed to an absolute pitch level. For example, in English, a melodic contour might be described as going ‘up’ and then ‘down’.
- **Metrical hierarchy**: high-level organization of rhythmic information in music, involving multiple levels of beat strength, such that some beats are consistently heard as stronger than others (e.g., the first event in a repeating rhythmic group).
- **Musical surface:** lowest level of event information in music (e.g., a sequence of notes).
- **Syncopation**: a variety of musical rhythms simultaneous, that makes part of the tones **off-beat**
- **Pitch chrom**a: group of pitch levels that are separated by an octave (i.e., a doubling of frequency), also known as a pitch class. Colloquially, members of the same pitch chroma share a note name; all the Fs on a piano have the same chroma.
- **Probe tone**: tone in perceptual experiments that is compared to a context; on a given trial of 
- **Tonal hierarchy**: high-level organization of pitch information in music, involving multiple levels of stability, such that some tones are heard as more stable than others (e.g., the tonal center, which is the most stable tone in a melody or other musical example).
- **Universality**: property of a species, wherein a given phenomenon (here, a cognitive process) is expected to appear in some form across all typically developing individuals.
- **Harmonic Series**
- **Fourier analysis**
- **Tonic (tonal center)**
- **Dominant**
- **Timbre**
- **Overtones**

**Tonal perception**
- **Pure frequency** - "Tone"
- **Complex frequency**
- **Harmonic series**: Integer multiplication of a base frequency, generating harmonic sound patterns
- **Consonance and dissonance** - Interference of tonal frequencies. A spectrum from 100% harmonic - pitch chroma, dissonance 
- **Octave** is defined as the double frequency difference
- **Western turning - 12-TET system** uses equal ratios between successive notes. Each step is a **semitone**, and the frequency ratio between adjacent notes is the 12th root of 2 (≈ 1.05946)
- Three approaches to **tonal hierarchies**
	- **Acoustics** - Mathematically harmonic frequencies
	- **Statistical** - The use of tones in music (in relation to base tones)
	- **Expectation / preference** - Experimental testing with **probe tones** in different contexts
- **Tonic** (The home pitch / tone center) -> **Dominant** (Fifth) -> **Subdominant** (Fourth)
- The tonal hierarchy shapes listeners expectation, and surprises
 
**Rythmic perception**
- **Meter**: The regular pattern of strong and weak beats in music, typically grouped into measures (e.g., 3/4 or 4/4 time)
- **Rhythm**: The arrangement of sounds and silences in time, created by varying note durations and accents within the meter.
- Rhythmic expectations can be measured and ranked just as tonal expectations:
	- Simple interger ratios (1:2) > complex integer ratios (7:8)

**Fysiologisk** (dansk forresten)
- Trommehinde
- Hammer, armboldt og stigbøjle
- Cochlea
- Basilar membrane - Vibrerer på lokation bestemt af lydfrekvensen, mekanisk "fourier analyse"
- Auditory cortex - Temporallappen

**Markov chains** is a representation of the influence towards future data points - Used in modelling of data
- Simple data - No influence between datapoints, independent samples
- **First order chains** - each observation influence the next
- **Second order chains** - each observation influence the two next in the line
- **N-order markov chain** - each observation influence the n next in line
- **Hidden markov model** - Each observation is influenced by a hidden markov chain, but doesn't directly influence each other - they can even me multilayered (several markov chains - hidden markov models inside hidden markov models, etc.)

An **_n_-gram** is a sequence of _n_ adjacent symbols in a particular order - for example letter (or tones)
- An **n-gram model** predicts the next symbol in a sequence, on basis of the n-gram
	- For example a model trained on "**a b c b c a**" would guess that a **c** follows a **b**, and a **b** following an **a**, but it would be 50/50 about whether a **c** is followed by an **a** or a **b**
	- It has a **markov order** of n-1

**Prediction by partial matching (PPM)**
- Used a mixture of n-gram models (high and low order)
- **PPM-Decay** employs a customisable **decay kernel** that downweights historic observations over time, allowing the model to adapt effectively when the statistical structure of an environment changes. 
- Includes a **finite-capacity memory buffer** (simulating short-term or echoic memory limitations) 
- and **stochastic retrieval noise** (simulating memory imperfection), which causes the fidelity of stored information to degrade as it moves from the active buffer into **long-term storage**

- **Experiment 1:** The model predicted artificial sequences where statistical rules changed over time, demonstrating that **memory decay improves accuracy in dynamic environments**
- **Experiment 2:** The model predicted chord sequences in Pop, Jazz, and Bach corpora, showing that **weighting recent events improves the learning of musical harmony**
- **Experiment 3:** The model simulated human reaction times in an auditory pattern detection task, confirming that performance is **constrained by a memory buffer with a limited item capacity rather than just time duration**

**Uncertainty and surprise** (Cheung et.al.)
- **IDyOM**-model built upon the standard PPM algorithm - combining a **long-term model** (trained on a large corpus of music) with a **short-term model** (utilizing only the current piece), trained on 745 songs from US Billboard top 100
- **Entropy** reflects how **uncertain** a listener is when anticipating an upcoming chord (given the portion heard so far) 
- **Information content** reflects how **surprised** the listener is once actually hearing the chord 
- **Pleasure** was modulated by surprise that was modulated by uncertainty (High pleasure at both high surprise and low uncertainty and vice verca)
	- Uncetainty and surprise was calculated with NN over a bunch of pop chord progression - pleasure was reported.
![[Screenshot 2025-12-20 at 14.25.09.png|300]]

**Music neuroscience**
- **Amygdala, Hippocampus and Audidatory cortex** activity was modulated by Interaction with uncertainty and surprise
- **Nucleus Accumbens (NAcc - Dopamine system)** does _not_ track the interaction (pleasure) but rather shows a main effect of uncertainty - When the music is uncertain, the brain is motivated to resolve that uncertainty, engaging the NAcc to direct attention toward the stimulus
- **Free-energy-principle** - when precision is low, the brain expects to be exposed to prediction error, so it prepares to minimize it by focusing or something


- **Parkinson** are less sensitive to complexity of music, and doesn't "feel" the need to move. Further backing of **dopamine involvement**
- Music helps parkinson patient with steady walking

![[Screenshot 2025-12-20 at 14.06.03.png]]

