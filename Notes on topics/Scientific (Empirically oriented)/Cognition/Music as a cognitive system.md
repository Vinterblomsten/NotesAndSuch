#MusicalCognition #Cognition #Perception #Modelling 

#### Basic theory of music
![[Screenshot 2025-09-10 at 10.29.57.png]]

**Pure sounds**: Single frequency wave
**Complex sounds**: A mix of different frequency waves - all "real" sounds are complex sounds
**Harmonic series**: Integer multiplication of a base frequency, generating harmonic sound patterns

**Fourier transform**
The Fourier transform is used to decompose a complex sound into the different frequency waves

![[Pasted image 20250910103210.png|500]]


**Consonance and dissonance**
- The way the waves interact with each other through constructive and destructive interference
- The further two frequencies are to each other the less interference (En general)
 ![[Screenshot 2025-09-10 at 10.47.01.png|500]]
 ![[Screenshot 2025-09-10 at 10.53.23.png]]
 The modern 12-note musical system, also called **12-tone equal temperament (12-TET)**, organizes pitches by dividing each octave into 12 equal steps on a logarithmic scale of frequency.

- **Octaves and Doubling**: An octave is defined as the interval between one pitch and another with exactly double its frequency. For example, if middle A (A4) is set at 440 Hz, then A5 is 880 Hz, and A3 is 220 Hz.
- **Equal Steps**: Instead of dividing the octave into simple integer ratios (as in earlier tuning systems), the 12-TET system uses equal ratios between successive notes. Each step is a **semitone**, and the frequency ratio between adjacent notes is the 12th root of 2 (≈ 1.05946).
- **General Formula**: If f0f_0f0​ is a reference frequency (usually A4 = 440 Hz), then the frequency of the note nnn semitones away is:
$$f(n) = f_0 \times 2^{\tfrac{n}{12}}$$
- **Result**: This system ensures that music can be played in any key with the same relative consonance, making it highly versatile for modulation and harmony across instruments. However, the trade-off is that pure harmonic ratios (like 3:2 for a perfect fifth) are only approximated, not exact.

![[Screenshot 2025-09-10 at 11.01.53.png]]

#### Measuring pitch expectations
![[Screenshot 2025-09-10 at 11.21.28.png|300]]

The note connections can be representat as a torus (**The doughnut of musicality**):
![[Tonnetz.gif]]

![[Screenshot 2025-09-10 at 11.26.53.png]]
**Acoustics**: The mathematical harmony of the waves
**Statistical**: The duration and amount of the different notes across a large collection of music (In g-major)
**Rating**: People rating the sound in expectations (**Probe-tone rating**)

#### Musical rhythm

Rythm is a human property (or is it?[Snowball](https://www.youtube.com/watch?v=cJOZp2ZftCw))

**Meter**: The regular pattern of strong and weak beats in music, typically grouped into measures (e.g., 3/4 or 4/4 time)
**Rhythm**: The arrangement of sounds and silences in time, created by varying note durations and accents within the meter.

Rhythmic expectations can be measured and ranked just as tonal expectations:
![[Screenshot 2025-09-10 at 11.51.35.png]]
- **Maybe a problem i think**: The temporal aspect of music is in contrast to the tonal aspect (if we accept the 12 note-system) a continuous scale (somewhat) wheras the tonal is discrete

**Interesting hypothesis**: Rhythmic syncrony raises empati and the likelihood of helping in the group
![[Screenshot 2025-09-10 at 11.57.33.png]]
#### Cochlear transduction

![[Screenshot 2025-09-10 at 10.37.06.png|500]]
The cochlear - organ of corti and the basilar membrane
- The basilar membrane is effectet by the vibrations in the fluid of the cohclear
- The membrane has different thicknesses, and the different parts of the membrane is vibrating at different frequencies - essentially a mechanical fourier transform - decomposing the sound to the different frequencies
- The signal are transducted by the cochlear nerve trough the medula - pons - midbrain - mgn to the primary audiatory cortex in the temporal lobe
![[Screenshot 2025-09-10 at 10.42.00.png|400]]

![[Screenshot 2025-09-10 at 10.42.30.png]]
##### Tonal hierarchy
Tonal hierarchy refers to the organization of pitches in tonal music according to their relative stability and importance. In Western tonal music, some notes are perceived as more central or stable than others. The **tonic** (the “home” pitch) is the most stable, followed by the **dominant** (fifth degree) and **subdominant** (fourth degree), which play key structural roles. Other scale degrees have varying degrees of tension and tend to resolve toward more stable tones.

This hierarchy shapes listeners’ expectations, creates a sense of direction, and provides coherence in tonal music. It’s a foundational concept in music theory, particularly in the analysis of harmony, melody, and cadences.


**Sequential data**
Simple sequence is when each measurement have no influence towards future measurements

**Markov chains** is a representation of the influence towards future data points - Used in modelling of data
- First order chains - each observaiton influence the next
- Second order chains - each observation influence the two next in the line
- N-order markov chain - each observation influence the n next in line
- Hidden markov model - Each observation is influenced by a hidden markov chain, but doesn't directly influence each other - they can even me multilayered (several markov chains - hidden markov models inside hidden markov moddels, etc.)
![[Pasted image 20250917103447.png|300]]
**Prediction by partial matching (PPM)**
**n-grams** are sequences of elements (letters, numbers, etc) can be high order and low order depending of the n

n-gram models are models based on n elements, where low order n-gram models are quick to learn, and high order n-gram models can capture more complex patterns
- 'ABC' -> 'D' (Low order)
- 'ABCABC' -> 'A' (High order ish)

Psychologically the further an element is in memory (time) the less weight it has in terms of prediction (memory decay)
![[Screenshot 2025-09-17 at 10.45.06.png|500]]

**Duration and information content**
Experimenting with duration of notes and amount of notes, it seems that the decay of importance of each note is much less controlled by the duration since the note, but the number of new notes since the last


