---
title: Electrical Properties (NeuroFys)
layout: default
---

# Electrical Properties (NeuroFys)

Tags: #Physics #Physiology  #Electricity

Electrical descriptions are a great abstraction for talking about the electrical properties of the cell.
#### Basic principles & terms

**Electrical charge (Q)** of particles is given by the electrons and protrons. 
- It is meassured in **Coulombs (C)** where $1C=6.24\times 10^{18}$ electrons
- One columb is the charge delved by a current of 1 ampere in 1 second: $1C=1A\times 1s$
- In the cells this is **ions** ($Na^+, Cl^-, Ca^{2+}$)

**Electrical current (I)** is a stream of charged particles
- It is defined as the change of charge over time: $I=\frac{dQ}{dt}$
- Measured in **ampere (A)** where **$1A=1C/1s$** or $1C=6.24\times 10^{18}$ electrons per second

(Difference) **Electrical potential (V)** between two points i what we call **voltage**
- A battery has a certain voltage, which represents the difference in charge between the two poles
- It can be described as an **electric pressure** where electrons wants to flow towards a more stable postition (lower difference in charge)
- Measured in **volts (V)**
- Analogy with water pressure is a good illustration of voltage

**Electrical resistance (R)** is a resistance of the movement of electrical charges
- Measured in **ohm ($\Omega$)** where $[\Omega]=[V]/[A]$ 
- In the water analogy, it is like reducing the diameter of a pipe

**Electrical conductance (G)** is the inverse of resistance $G=1/R$
- Measured in **siemens (S)** where $[S]=[\Omega^{-1}]$ 
- This is often better in the membrane analysis, as the conductance is **relatable to permeability**
	- Here **ion channels** provide single channel conducatance ($\gamma$)
	- The total conductance is given by $G=\Sigma \gamma$ 

**Capacitance (C)** is the ability to store charges when connected to a voltage in a **capacitor**
- Whenever two surfaces of electrical conducting material are sperated by an insolator (lipid bilayer in the cell)
- Given by the charge and voltage: $C=Q/V$
- The capacitance is **proportional to the area** of the plates, and **inversely proportional to the distance** between the plates
![217](z-Figures/Screenshot%202026-09-02%20at%2010.45.31.png)
- It is measured in **farad (F)** where $[F]=[C]/[V]$
#### Relation of parameters

**Ohms law**: $V=R\times I$ - describes the relation between voltage and current across a resistor
- The current through a resistor is directly proportional to the voltage across it
- The larger the voltage - the more the current
- etc.

**Capacitive current** is the current moving into the capacitor at any point
- It is present whenever current is flowing: $I_c=\frac{dQ}{dt}=C\frac{dV}{dt}$
- When V is constant then $\frac{dV}{dt}=0$ and $I_c=0$
##### Membrane time constant
When we have a **resistance and a capacitor in parallel**. In the cell this is always present as the membrane and the inverse permeability.

It is usable when we create a **constant influx of current** in the neuron - $I_m$

Kirchoffs law says that all current sent into the circuit must exit the circuit through any path.
- In this circuit: $I_m=I_r+I_c$	

Given Ohms law and capacitive current
- $I_r=V_m/R_m$
- $I_c=C_m\frac{dV_m}{dt}$
where $V_m$ is the membrane potential, $R_m$ is the membrane resistance, $C_m$ is the membrane capacitance.

Together we get the equation:$$I_m=\frac{V_m}{R_m}+C_m\frac{dV_m}{dt}$$This differential equation can be solved as a function of $V_m$ in relation to time:
$$\Delta V_m(t)=\Delta V_{m,\infty}[1-e^{-t/\tau}]$$
where $\Delta V_{m,\infty}$: The final steady-state ($t\rightarrow \infty$), the height of the curve as long as the current influx remains.

$\tau$ (tau) called the **time constant** is defined as:
$$\tau=R_m\times C_m$$
with the unit si calculated $\Omega\times C/V=V/A\times C/V=C/A=C/(C/s)=s$ to seconds

At $t=\tau$ we have $\Delta V_m(t)=\Delta V_{m,\infty}[1-e^{-1}]\approx 0.63\Delta V_{m,\infty}$, that is we can **find the point of 63% of the steady-state, to find the time constant.** 
![Screenshot 2026-09-02 at 15.03.30](z-Figures/Screenshot%202026-09-02%20at%2015.03.30.png)
**Functionally** :
- Neurons with **large** $\tau$ (High resistance and high capacitance) integrate synaptic inputs over a longer period. This means that it is good for summing many small, temporarily spread out inputs. 
- Neurons with **small** $\tau$ responds and resets quickly. 


##### Membrane length Constant
What will happen to a depolarization over distance?
![Screenshot 2026-09-02 at 11.00.17](z-Figures/Screenshot%202026-09-02%20at%2011.00.17.png)
In this model we have
- $r_o$: extracellular resistance ($\Omega/cm$)
- $r_i$: intracellular resistance ($\Omega/cm$)
- $r_m$: membrane resistance ($\Omega\times cm$)

We can then find the change in membrane potential as a function of distance
$$\Delta V_m(x)=\Delta V_0-e^{-t/\lambda}$$
where: $$\lambda=\sqrt{\frac{r_m}{r_i+r_o}}\approx\sqrt{\frac{r_m}{r_i}}$$
We see that when $x=\lambda$, then $\Delta V_m(x)=\Delta V_0-e^{-1}$, meaning that we see an $\approx 37\%$ decline in membrane potential at distance of the length constant.

**Functionally**
- You can pass signals very long, if the membrane resistance is high and the inside (and outside) resistance is low and vice versa

![353](z-Figures/Screenshot%202026-09-02%20at%2015.36.17.png)
(Also the lobster nerve is myelinated and thus higher membrane resistance than the pyramidal neuron)

Space constant - **Complex version** (Luo.)
- $R_i$: intracellular resistance per length (volume somehow?) ($\Omega\times cm$)
- $R_m$: membrane resistance per area ($\Omega\times cm^2$)
- $d$: diameter of the fiber ($cm$)
$$\lambda=\sqrt{\frac{dR_m}{4R_i}}$$