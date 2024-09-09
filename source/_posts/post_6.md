---
title: THEORY - Infrared Spectroscopy in the Analysis of Microplastics
date: 2024-08-13 18:02:25
mathjax: true
categories: [Programming]
tags: [Spectroscopy, Experimental Physics, Microplastic]

---

This article was one of the evaluations we had during the pandemic in the Modern Physics Laboratory II course, taught by Professor Dr. Roberto Meigikos during his undergraduate studies at the Fluminense Federal University (UFF). As it was distance learning, it wasn't possible to carry out the experiments physically, so we used data collected by students from previous semesters. In this post we aim to present the theoretical physics behind the interaction of radiation with material, and experimentally, simulating a tomography of a lung, built with low-cost material.

# Introduction

Plastic is a word derived from the Greek plastikos, which means “flexible and easily moldable”. The first synthetic plastic appeared with the aim of replacing other materials, such as elephant ivory (by John Wesley Hyatt [1]), which was used to make billiard balls.

Plastic is used in large quantities [2] by humans in their daily lives in
packaging industries, toy production, clothing, cosmetics, automotive lines, among others. Due to this deliberate consumption of polymers, large quantities of waste are generated which are poorly recycled and reused, and consequently end up in the environment. Depending on the type of plastic, it takes years to decompose and thus has a major impact on nature.

One of the biggest problems with plastic pollution is that it is found in aquatic environments.
environments, which undergo reactions due to ultraviolet radiation, mechanical action and hydrolysis. These are physical phenomena responsible for degrading these plastics into small particles, i.e. meso-plastics, micro-plastics and nano-plastics.

Polymers have the capacity to adsorb chemical elements (including heavy metals),
making them highly toxic. Polymers that undergo solar radiation have their molecular structure altered [3][4]. Ingesting polymers is extremely harmful to aquatic animals and even their predators, including humans [5]. predators, including humans [5], as they can cause some effects such as: internal damage, failure to reproduce, developing reproductive abnormalities and cancer.

This post aims to analyze the plastic objects found on Jurujuba beach in Rio de Janeiro and identify the elements that make them up. The sample is identified using
equipment (Mid Infra-Red Spectroscopy - MIRS system), which will irradiate the collected sample and generate a sample and generate a frequency spectrum. This spectrum is then compared with a sample identification table, thus recognizing the polymer analyzed.

# Theoretical reference
## Electromagnetic waves

Electromagnetic waves [6] [Figure 1] are oscillations formed by electric and magnetic fields magnetic fields in which they move at the speed of light (the speed varies if moving in a vacuum or in a material medium) and carry energy.

{% asset_img "1.webp" "Figure 1" %}
<p style="text-align: center;">
  figure 1: Electromagnetic waves <br>
  Source: https://www.pngitem.com/middle/hRTTRbw_qual-efeito-do-nacl-nas-particulas-poder-de/ </p>

This energy depends on the wave number:

$$ E = hc\lambda^{-1} $$

where:

$ h $ is Planck's constant
$ c $ speed of light
$ \lambda^{-1} $ wave number

For example, we can see in [Figure 2] that blue visible light has a shorter wavelength than red, so the electromagnetic wave in the blue range is more energetic than the wave in the red range.

{% asset_img "2.webp" "Figure 2" %}
<p style="text-align: center;">
  figure 2: Wavelength table. <br>
  Source: https://dan-scientia.blogspot.com/2010/03/relacao-da-frequencia-com-o-comprimento.html </p>


## Photon absorption and emission

In order to understand the absorption and emission of photons, we have to consider that electromagnetic waves have an intrinsic duality, i.e. wave-particle duality [7] and that the photon's energy is quantized (an idea proposed by Einstein in 1095), i.e. each photon has only one particular energy which cannot be subdivided and which is absorbed or emitted [8] [Figure 3] completely.

**Absorption**: Occurs when an electron in a fundamental state, with fundamental energy,
receives a photon whose quantum of energy is exactly the difference between the energy levels of the electron's initial initial state of the electron and the next excited state.

**Emission**: Occurs when the electron is in an excited state (after receiving a photon) and
returns to its ground state, emitting a photon with energy equal to the energy of the difference between the states. It can be called an energy state transition.

{% asset_img "3.webp" "Figure 3" %}
{% asset_img "4.webp" "Figure 3" %}
<p style="text-align: center;">
  Figure 3: Photon absorption and emission. <br>
  Source: http://www.if.ufrgs.br/cref/camiladebom/Aulas/Pages/3.html
http://www.astronoo.com/pt/artigos/principio-absorcao-emissao-atomica.html </p>

## Spectral lines

When radiation hits an atom, it excites the electrons and when they are excited, they radiate photons. Each photon will have its own characteristic frequency. We can see in [Figure 4], for example, that when a prism is hit by white light, it will form an absorption spectrum containing all the colors of a rainbow, i.e. electromagnetic waves whose frequencies are located between infrared and ultraviolet.

{% asset_img "5.webp" "Figure 4" %}
<p style="text-align: center;">
  Figure 4: Spectres. <br>
  Source: http://www.if.ufrgs.br/cref/camiladebom/Aulas/Pages/3.html</p>

We can consider that each atom will have its own fingerprint, for example, the absorption and emission spectrum of the hydrogen atom [Figure 5]. As no other atom will have the same spectral composition, we can analyze various substances using the periodic table of spectra. For example, the table of emission spectra [Figure 6].

{% asset_img "6.webp" "Figure 5" %}
<p style="text-align: center;">
  Figure 5: Emission and absorption lines for the hydrogen atom. <br>
  Source: http://www.if.ufrgs.br/cref/camiladebom/Aulas/Pages/3.html</p>

{% asset_img "6.webp" "Figure 7" %}
<p style="text-align: center;">
  Figure 6:  Periodic table with emission spectra of the elements. <br>
  Source:  https://www.tabelaperiodica.org/</p>

## Infrared spectroscopy

Infrared spectroscopy is a technique based on molecular absorption, in which we consider that the molecule may contain 2 or more atoms that behave like a simple harmonic oscillator [9] and that the energy absorbed by a given molecule stimulates rotational and vibrational transitions [Figure 7].

{% asset_img "8.webp" "Figure 7" %}
<p style="text-align: center;">
  Figure 7:  Vibrational models. <br>
  Source:  https://queslemartins.unir.br/pagina/exibir/19174 </p>

Molecular vibrations can be classified into axial deformations or stretches and angular deformations. Stretches are changes in the internuclear distance of the atoms involved, i.e. alternately increasing and decreasing this distance. Angular deformations, on the other hand, can consist of a change in the bond angle with a group of atoms or the movement of a group of atoms in relation to the rest of the molecule. [10]

Each atom will have its own vibrational mode with its own characteristic frequency. The frequency range of The frequency range of interest is 4000 to 400 cm -1, which is the average MIR range and is also the frequency capable of exciting an organic molecule. In section 2.3, photon absorption and emission were explained and here the idea remains the same, but with some modifications as it is a harmonic oscillator model, whose energy variation for the state transition to occur is given by:

$$ \Delta E = hf $$

where

$ \Delta E $ is the energy difference between the excited and fundamental states of the molecule;

$ h $ Planck's constant.

$ f $ is the vibrational frequency.

Remember that the molecular energy is the sum of the rotational, vibrational and electron excitation energies:

$$ E = E_{vib} + E_{rot} + E_{el} $$

the frequency of an oscillator made up of 2 atoms will be:

$$ f = \frac{1}{2\pi}\sqrt{\frac{F}{\mu}} $$

where:

F is the bond strength constant Inter atomic.
$ \mu $ is the reduced mass given by:

$ \mu = \frac{m_2m_1}{m_1 + m_2} $

Therefore, if a sample is irradiated with infrared light, part of the radiation is absorbed. This
detailed information is obtained about the vibrations of molecules and vibrational frequencies, which allows chemical compounds to be characterized [Figure 8] [11].

{% asset_img "9.webp" "Figure 8" %}
<p style="text-align: center;">
  Figure 8: Molecular vibrational frequencies. <br>
  Source: Lecture by Professor Dr. Roberto Meigikos. </p>

## Fourier Transform Infrared Spectroscopy (FTIRIS)

FTIR is basically used to generate an interferogram using a Michelson interferometer [12]. The spectra are obtained by calculating the Fourier transform of the interferogram. The interferometer [13] consists of a system of reflecting mirrors and semi-transparent mirrors (beam splitters) whose function is to combine the separate light beams that initially come from the same source [Figure 9]. When they travel the same distance there is constructive interference, otherwise there is destructive interference, i.e. they are out of phase.

{% asset_img "10.webp" "Figure 9" %}
<p style="text-align: center;">
  Figure 9: Interferometer. <br>
  Source: http://hyperphysics.phy-astr.gsu.edu/hbasees/phyopt/michel.html. </p>

You can see in [Figure 10] the process for generating the spectrogram, and in [Figure 11] that the spectrum obtained is the Fourier transform of the interferogram.

{% asset_img "11.webp" "Figure 10" %}
<p style="text-align: center;">
  Figure 10: Diagram of the process to generate the spectrum. <br>
  Source: http://hyperphysics.phy-astr.gsu.edu/hbasees/phyopt/michel.html. </p>

{% asset_img "12.webp" "Figure 11" %}
<p style="text-align: center;">
  Figure 11: Fourier transform. <br>
  Source: Lecture by Professor Dr. Roberto Meigikos. </p>

The Fourier Transform [14] decomposes a time signal (non-periodic, i.e. non-cyclic functions) into sine and cosine components.

# Microplastics
## Plastic waste

In 1997, the first floating waste island was discovered by oceanographer Charles Moore. There are a total of 5 plastic islands [Figure 12]. The islands form when waste enters rotating ocean currents and ends up in the center of large oceans. 

{% asset_img "13.webp" "Figure 12" %}
<p style="text-align: center;">
  Figure 12:  Rubbish islands. <br>
  Source: https://www.iberdrola.com/meioambiente/as-5-ilhas-de-lixo-nos-oceanos </p>

25 million tons of waste are dumped into the ocean every year, 80% of which comes from cities and 50% of which is plastic [15]. The main sources of waste today are: wear particles from car tires, landfills, sewage, the agricultural industry, cosmetics industries and others. These materials slowly deteriorate and when they become small enough, they can be mistaken for food and end up being ingested by animals, causing various problems already mentioned in the introduction. Plastics can be classified into a few categories: size, polymer origin, color and shape.

## Size 

Classification by size:

Macro-plastics (> 25 mm)
Meso-plastics (5 - 25 mm)
Micro-plastics (< 5 mm)

## Origin

Micro-plastics can also be sub-classified as primary or secondary.

Primary: These are produced by man in the size that they fall under as micro-plastics. For example: resin pellets (raw materials for plastic products whose shapes include shapes), household utensils, personal care products (facial cleansers, toothpastes, exfoliating creams).

Secondary: these are products of the degradation of larger plastic items, due to the action of external
(UV radiation and physical abrasion, etc.) which are broken down into smaller and smaller fragments until they reach the size of micro-plastics.

## Polymer

The type of polymer used in the production of micro-plastics can be determined during the FTIR analysis phase. A complete list with their applications can be seen in [Figure 13].

{% asset_img "14.webp" "Figure 13" %}
<p style="text-align: center;">
  Figure 13: Polymers and applications. <br>
  Source: Lecture by Professor Dr. Roberto Meigikos </p>

## Color and Shapes

We can identify polymers by color and shape[Figure 14].

{% asset_img "15.webp" "Figure 14" %}
{% asset_img "16.webp" "Figure 15" %}
<p style="text-align: center;">
  Figure 15: Identifying and sorting by color and shape.. <br>
  Source: Lecture by Professor Dr. Roberto Meigikos </p>

# Experiment

This post introduced physical concepts such as: Electromagnetic waves, photon absorption/emission and spectral lines. With these concepts we are able to identify some materials collected on the beach and characterize whether they are polymers or not using techniques such as FTIR also mentioned in this post. Micro-plastics and their harmful effects were also discussed.

The next post will deal with the experimental part in which we will collect a small amount of sand from Jurujuba beach containing plastic waste, analyzing it with the FTIR method and obtaining its spectrum range and consequently classifying the polymer using the Python programming language.

# References

[1] Britannica, The Editors of Encyclopaedi - "John Wesley Hyatt" - Encyclopedia Britannica, 24 Nov. 2022. Disponível em:

https://www.britannica.com/biography/John-Wesley-Hyatt

[2] Carrança, T- Consumo de plásticos explode na pandemia e Brasil recicla menos de 2% do material - BBC News Brasil - 30 novembro 2020. Disponível em:

https://www.bbc.com/portuguese/brasil-55131470

[3] Stieven, L; Marlene, R - Influência da radiação solar na degradação do polipropileno. 3º Congresso Internacional de Tecnologias para o Meio Ambiente – RS, BRASIL - 13/09/2021. Disponível em: 

https://siambiental.ucs.br/congresso/getArtigo.php?id=71&ano=_terceiro Acessado: 

[4] Ipen - Polímero - 13/09/2021. Disponível em:

 https://www.ipen.br/portal_por/portal/interna.php?secao_id=737 

[5] Veiga, E - Cada pessoa come até 121 mil partículas de plástico por ano, diz estudo - BBC News Brasil - 5 junho 2019. Disponível em:

 https://www.bbc.com/portuguese/geral-48518601

[6] Radiação eletromagnética - 9 abril 2023. Disponível em:

https://pt.wikipedia.org/wiki/Radia%C3%A7%C3%A3o_eletromagn%C3%A9tica

[7] Leia mais sobre dualidade onda – partícula:

http://www.cbpf.br/~eduhq/html/aprenda_mais/jurema/ficha_dualidadeonda.htm#1
https://en.wikipedia.org/wiki/Wave%E2%80%93particle_duality

[8] Veja aula do prof: Jorge de Sá UFF no youtube:

https://www.youtube.com/watch?v=X5_3YYcb0s4

[9] Da Costa, G - MOVIMENTO HARMÔNICO SIMPLES (MHS) - 9 abril 2023. Disponível em: 

https://midia.atp.usp.br/plc/plc0002/impressos/plc0002_11.pdf

[10] FORATO, L; BERNADES, R - A Espectroscopia na região do Infravermelho e algumas aplicações. Embrapa Instrumentação 2010 tiragem 300

[11] MEIGIKOS, R. Prática 4/MIRS Microplásticos Slide. Disponível em: 

https://docs.google.com/presentation/d/1JemU9E2e_1zHjXZvxo4QAw- _V05XI3Ne/edit#slide=id.p34 

[12] Albert A. Michelson - Biographical - 9 abril 2023. Disponível em: 

https://www.nobelprize.org/prizes/physics/1907/michelson/biographical/

[13] CATELLI, F. VICENZI, S. 2004 INTERFERÔMETRO DE MICHELSON. Disponível em: 

https://periodicos.ufsc.br/index.php/fisica/article/view/10025/14562

[14] A Transformada de Fourier - Para aprofundar mais no conceito acesse:

https://www.feis.unesp.br/Home/departamentos/e
ngenhariaeletrica/mcap05.pdf

[15] SOLDERA, B - Lixo no oceano: tem solução?. Aguasustentavel,2021. Disponivel em: 

https://www.aguasustentavel.org.br/blog/109-lixo-no-oceano-tem-solucao
