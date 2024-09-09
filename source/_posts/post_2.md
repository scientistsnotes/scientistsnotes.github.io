---
title: THEORY - The interaction of radiation with matter
date: 2024-07-13 00:00:00
mathjax: true
categories: [Physics]
tags: [Radiation, Nuclear physics,Experimental Physics]
---

This article was one of the evaluations we had during the pandemic in the Modern Physics Laboratory II course, taught by Professor Dr. Roberto Meigikos during his undergraduate studies at the Fluminense Federal University (UFF). As it was distance learning, it wasn't possible to carry out the experiments physically, so we used data collected by students from previous semesters. In this post we aim to present the theoretical physics behind the interaction of radiation with material, and experimentally, simulating a tomography of a lung, built with low-cost material.


# Introduction

Ionizing radiation is of great interest to humanity, specifically to the health community (nuclear medicine, radiotherapy, radiodiagnosis, radiopharmaceuticals, etc.) because it can be used for diagnosing and treating tumours, cancers and other diseases, providing patients with a better quality of life [1]. We can characterize ionizing radiation as particles without mass (x-rays and gamma rays) or with mass (electrons, neutrons, protons, etc.)
 
X-rays were discovered by Roentgen in 1895 [2] and radioactivity by Becquerel (Becquerel discovered the phenomenon and Marie Curie "baptized" it radioactivity) A brief discussion can be seen here [3] in 1896 [4]
 
In order to understand how tomography works, i.e. how the image is created from the interaction of electromagnetic radiation with matter, we must study various phenomena such as the Compton effect, the photoelectric effect and others.

# Basic principles of radiation interaction with matter
 
When ionizing radiation (an electromagnetic wave with energy greater than 16 eV) interacts with matter, some or all of its energy is transferred to the atoms, causing atomic excitation and ionization [Figure 1]. Electromagnetic radiation is called indirectly ionizing radiation due to its transfer of energy to the electron, which will cause further ionization. However, for this process to occur, the electromagnetic wave, which has no charge and no rest mass, must travel through a large thickness when it hits a material before it undergoes its first interaction. In this interaction, the waves can be partially or totally absorbed, as well as scattering after the interaction or simply not interacting and the wave passing straight through. So, given these conditions, we have to consider that the probability of radiation interacting with matter depends directly on the value of its energy.
 
The main interactions, excluding nuclear reactions, are: photoelectric effect, Compton effect and pair production. All these interactions are called "catastrophic" because in all cases the incident photon disappears after a single interaction with a single atom of matter.

{% asset_img "a.webp" "Figure 1" %}
<p style="text-align: center;">
  Figure 1: Interaction of ionizing radiation with matter.  <br>
  Source: http://appasp.cnen.gov.br/seguranca/documentos/FundamentosCORv10.pdf   </p>

## Photoelectric effect

$$E_{c} = h \cdot v - B_{e}$$
 
 Where: h is Planck's constant, $𝑣$ is the frequency of the radiation and $𝐵_{𝑒}$ is the binding energy of the orbital electron.

 {% asset_img "b.webp" "Figure 2" %}
<p style="text-align: center;">
  Figure 2: Representation of the photoelectric effect.  <br>
  Source: http://appasp.cnen.gov.br/seguranca/documentos/FundamentosCORv10.pdf   </p>


## Compton effect

In the Compton effect [7] the incident photon gives up part of its energy to a single orbital electron of any level of the electronic cloud of the atom with which it interacts [Figure 3], ionizing an atom. A scattered radiation known as a Compton ray appears, with lower energy than the incident photon. The energy of the scattered photon $E'_\gamma$ will be:
 
$$E^{'}{\gamma} = \frac{E{\gamma}}{ 1 + \alpha(1 - \cos{\theta})}$$
 
Where: $E_\gamma$ is the energy of the incident photon.
 
$$\alpha = \frac{E_\gamma}{m_o c^2}$$
 
The energy of the scattered photon is maximum for $\theta = 0^{\circ}$ and minimum for $\theta = 180^{\circ} $. The kinetic energy of the ejected electron is maximum for this case and equal to:
 
$$T_{max} = E_\gamma \frac{2\alpha}{1 + 2\alpha}$$
 
In general, the direction of the Compton ray is unpredictable because it depends on the geometry of the interaction between the incident photon and the electron.

{% asset_img "c.webp" "Figure 3" %}
 <p style="text-align: center;">
  Figure 3: Representation of the Compton effect.   <br>
  Source: http://appasp.cnen.gov.br/seguranca/documentos/FundamentosCORv10.pdf  </p>


## Pair production effect

The pair production effect[8] can only occur when the incident photon has relatively high energy ( 𝐸𝛾 > 1.022 𝑀𝑒𝑉 ) and the energy materializes [Figure 4] When passing close to the nucleus, the photon interacts with the nuclear electric field, dissipating energy and transforming into a pair of electrons (one negative, one positive)
 
$$\gamma \rightarrow e^+ + e^- + \textbf{kinetic energy}$$
 
If $E_\gamma$ is greater than 1.022 𝑀𝑒𝑉 the pair of electrons will receive kinetic energy

{% asset_img "d.webp" "Figure 4" %}
<p style="text-align: center;">
  Figure 4: Representation of the pair production effect.   <br>
  Source: http://appasp.cnen.gov.br/seguranca/documentos/FundamentosCORv10.pdf  </p>


# Analysis of the probability of occurrence of the photoelectric, pair production and Compton effects

We can see in [Figure 5] that the photon's interaction with matter has a probability of predominance for the photoelectric effect, which has photons with low energies and atoms with high atomic numbers, but as the photon's energy increases, the dominance of the photoelectric effect decreases and the Compton effect begins to dominate. The probability of the Compton effect occurring decreases for atoms with a high atomic number and has a higher probability for low atomic numbers. As the energy of the photon increases, the Compton effect also begins to fall and the probability of pair production begins to increase.

{% asset_img "e.webp" "Figure 5" %}
<p style="text-align: center;">
  Figure 5: Representation of the probability of photon interaction with matter.  <br>
  Source: Lecture material by Professor Dr. Meigikos. </p>


For an atomic number equal to 20 (calcium), which is the mineral present in the human body [10], mainly in bones, we have [Table 1] with the range of dominance according to the energy of the incident photon. We can see that the Compton effect has the largest range, considering energies above 10 MeV. This energy range is not normally found in natural radiation but only in particle accelerators, such as Sirius (Brazil) and LHC (Switzerland).

<p style="text-align: center;">
  Table 01: Predominance of effects according to photon energy.   <br>
  Source: Lecture material by Professor Dr. Meigikos.   </p>
{% asset_img "f.webp" "Table 01" %}


# Stopping power

The particle's interaction with the absorbing material determines its energy loss and therefore its range in the material. As the number of interactions over a macroscopic length is large compared to the energy fluctuations, an average value of this loss can be obtained. So, when passing through a distance x, the particle's energy loss will be given by dE/dx.
 
This interaction is a probabilistic process and has the direct consequence of energy loss through kinetic energy. The stopping power, or stopping power, is the negative of the average value of the energy loss
energy loss by distance:
 
$$\text{S(stopping power)} = - \left<\frac{dE}{dx}\right> $$
 
Calculating the average value of this derivative, we find that:
 
$$\left<\frac{dE}{dx}\right> = - \frac{4\pi e^4z^2}{m_0 c^2\beta^2}N\frac{Z}{A}\left[\frac{1}{2} ln\frac{2m_0c^2\beta^2}{I^2(1-\beta^2)}T_{max} - \beta^2 - \frac{\delta}{2}\right]$$
 
Where:
 
$\frac{4\pi e^4z^2}{m_0 c^2\beta^2}$ - Characteristics of the incident beam and $\beta$ is the velocity of the particle (the faster, the lower the loss)
 
$N\frac{Z}{A}$ - Characteristics of the medium and the electron density (the higher the atomic number and the higher the density of the medium, the greater the probability of braking occurring);
 
$I$: is the average excitation potential;
 
$T_{max}$: is the maximum energy that can be transferred in a collision;
 
$\frac{\delta}{2} $: is the correction due to the effects of density and polarization of the medium
 
The contrast present in the images becomes more intense at low energies. As the energy increases, the radiation passes through the medium more easily, causing the contrast to decrease. As can be seen in [figure 03], soft tissue (composed of H, C, N, O) has an energy < 1 keV and the contrast media I (Z=53) and Ba (Z=56) have energies of 34 and 37 keV [5], respectively. This forms the sharpness of the image.

{% asset_img "g.webp" "Figure 6" %}
<p style="text-align: center;">
  Figure 6: Effect of K-layer electron interaction with soft tissue and contrasts.  <br>
  Source: Lecture material by Professor Dr. Meigikos. </p>


However, when it reaches very high energy values, the probability of breakage is high, so the particle may suffer braking. On the other hand, the lower the energy level, the more difficult it is for the radiation to pass through the medium. The S (stopping power) graph of the Muon in Copper [11], shown in [figure 7], shows the variation of this particle at various energy levels.



{% asset_img "h.webp" "Figure 7" %}
<p style="text-align: center;">
  Figure 7: Stopping Power graph by moment of the Muon.   <br>
  Source: https://physics.stackexchange.com/questions/156755/stopping-power-diagramhttps://physics.stackexchange.com/questions/156755/stopping-power-diagram  </p>



It follows that the denser the material in question, the less radiation will pass through it and the worse the contrast will be in the constructed image.

## Shock section

The cross section represents the probability of a given reaction or interaction occurring It is defined as the ratio between the number of events observed by incident photon fluxes per unit time and the number of scattered ones [Figure 8]
 
The flux incident on the target is
 
$$ \phi_A = \frac{N_A}{A} $$
 
where


$N_A$ is the number of photons per unit time incident on a region whose area is A
 
The number of atoms in the material $n_B$ will be
 
$$ n_B = AdN_B $$
 
being
 
d is the thickness of the material S surface
 
$N_B $ is the number of scattering centers per unit volume in the alv
 
Then we can write the shock section as
 
$$\theta_{tot} = \frac{N_{tot}}{\phi_A n_B}$$
 
Ond
 
$N_{tot}$ are the total number of photons that interact with the material per unit time.
 
The intensity of the radiation obeys the inverse square law of its radial distance [12][Figure 9]
 
$$I = \frac{\phi_A}{4\pi r^2}$$

{% asset_img "i.png" "Figure 8" %}
<p style="text-align: center;">
  Figure 8: Incident flux on target.   <br>
  Source: Lecture material by Professor Dr. Meigikos.  </p>


{% asset_img "j.webp" "Figure 9" %}
<p style="text-align: center;">
  Figure 9: Radiation intensity.   <br>
  Source: Lecture material by Professor Dr. Meigikos.  </p>


## Image production[10]

Image production involves the attenuation and absorption of photons. The density and atomic number of the material influence how the image generated by a photographic plate is obtained. We can see in [Figure 10] an image produced through the interaction of photons with a real lung. We can see that there are differences in contrasts, so we can identify each region of the lung. However, there are undesirable effects, as seen in [Figure 11], which happen when the Compton effect occurs, which is basically the scattering of photons, polluting the image on the photographic plate.

{% asset_img "k.png" "Figure 10" %}
<p style="text-align: center;">
  Figure 10: Lungs without Compton effect.  <br>
  Source: Lecture material by Professor Dr. Meigikos.  </p>



{% asset_img "l.png" "Figure 11" %}
<p style="text-align: center;">
  Figure 11: Lung with Compton effect.   <br>
  Source: Lecture material by Professor Dr. Meigikos.</p>

As the post was so large, it was decided to split it into two, one being the theoretical part and the other being the experimental part. In the experimental part we will use the Python language to interpret and create the image of the lung using the data collected.
  
References
 
[1] Cecilia, A. - Radioprotection in Health Services - February 2023. Available at:
 
http://www.fiocruz.br/biossegurancahospitalar/dados/material10.pdf
 
[2] Brazilian Journal of Pathology and Laboratory Medicine - Volume 45 - Number 1 - 2009. Available at:
 
https://www.scielo.br/j/jbpml/a/nx9PgT734TySs5j9RhwzQTn/?format=pdf&lang=pt
 
[3] Martins, R. - How Becquerel didn't discover radioactivity - Caderno Catarinense de Ensino de Física - 2009 Available at:
 
https://www.researchgate.net/publication/275832998_Como_Becquerel_nao_descobriu_a_radioatividade
 
[4] Rios, E - Antoine Henri Becquerel (1852 - 1908) - Radiation Biophysics - UFRGS. Available at:
 
https://www.ufrgs.br/fismed/becquerel.htm
 
[5] Tauhata, L. Salati, I. P. A., Di Prinzio, R., Di Prinzio, A - RADIOPROTECTION AND DOSIMETRY: FUNDAMENTALS - April 2014. Available at:
 
http://appasp.cnen.gov.br/seguranca/documentos/FundamentosCORv10.pdf
 
[6] USP - EXPERIMENTAL BASES OF QUANTUM MECHANICS PHOTOELECTRIC EFFECT. Available at:
 
https://edisciplinas.usp.br/pluginfile.php/4356224/mod_resource/content/1/Teoria%20do%20efeito%20fotoel%C3%A9trico.pdf
 
[7] Silva, I., & Freire Jr, O. - The discovery of the Compton effect: From a semiclassical to a quantum approach - Revista Brasileira De Ensino De Física - 2014. Available at:
 
https://doi.org/10.1590/S1806-11172014000100026
 
[8] Hubbell, J - Electron-positron pair production by photons: A historical overview - 2006. Available at:
 
https://doi.org/10.1016/j.radphyschem.2005.10.008
 
[9] Lecture material by Professor Dr. Meigikos.
 
[10] Lewis, J - Hypercalcemia (high levels of calcium in the blood) - October 2021. Available at:
 
https://www.msdmanuals.com/pt-br/casa/dist%C3%BArbios-hormonais-e-metab%C3%B3licos/equil%C3%ADbrio-eletrol%C3%ADtico/considera%C3%A7%C3%B5es-gerais-sobre-a-fun%C3%A7%C3%A3o-do-c%C3%A1lcio-no-organismo
 
[11] Particle physics - Stopping power diagram - Physics Stack Exchange. Available at:
 
https://physics.stackexchange.com/questions/156755/stopping-power-diagramhttps://physics.stackexchange.com/questions/156755/stopping-power-diagram
 
[12] Vieira, P, Lara, V, Amaral, D - Demonstration of the inverse square law using a tablet/smartphone - Revista Brasileira De Ensino De Física, 36 - 2014. Available at:
 
https://doi.org/10.1590/S1806-11172014000300017
 
[13] Meigikos, R - Interaction of Radiation Physics with Everyday Life: a multidisciplinary practice for Physics Teaching - 2017. Available at:
 
https://doi.org/10.1590/1806-9126-RBEF-2016-0119