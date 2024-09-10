---
title: EXPERIMENT - Measuring the speed of propagation of electromagnetic radiation
date: 2024-09-09 13:46:41
categories: [Physics]
tags: [Physics, Nuclear physics, Experimental Physics, Radiation]
mathjax: true
---

In the previous post [click here](https://scientistsnotes.github.io/2024/08/20/post-7/) I talked about the theory of how fast electromagnetic radiation propagates. Now, the focus will be on the experimental part.

The measurements were carried out in 2018/2019 in the Multiuser Laboratory of Experimental Physics (LAFEX) of the Brazilian Center for Physics Research (CBPF), during an internship, under the guidance of Prof. André Massafferri Rodrigues and co-supervision of Prof. Henrique Saitovitch. This laboratory had all the necessary infrastructure for developing the experimental setup, consisting of radiation detectors, modules and associated acquisition electronics and a 22Na radioactive source. An illustration of the layout of the experimental setup used in this monograph is shown in Figure 01. The positrons generated from a 22Na source are annihilated with electrons present in an aluminum film covering the source. The photons generated in the annihilation process were directed to the scintillator detector, which in turn produced an analog signal for the electronic device, which transformed it into a digital signal so that it could be directed to the data acquisition system. This chapter will present the main characteristics of this arrangement.
 

 {% asset_img "1.webp" "Figure 01" %}
<p style="text-align: center;">
  Figure 1: Illustration of the experimental setup</p>

# RADIATION SOURCE

The radiation source used in this experiment was made commercially from an inert solution containing 22Na in an aluminum casing, 2.5 cm in diameter, with an intensity of 30µCi, manufactured by Eckert & Ziegler Isotope Products.  One advantage of using 22Na is that the positron from the b+ decay of 22Na to 22Ne (T1/2 3.6 ps) is created almost simultaneously with the emission of the 1274 keV gamma [01]. Thus, the positron can be used as a start for the electronic device associated with the experimental setup.

# RADIATION DETECTION

Determining the speed of propagation of electromagnetic radiation begins with the detection of photons from the 22Na source. As seen in section 2.4, after the positron is emitted, it is annihilated when it meets an electron from the outer layer of the source, emitting two photons, each with an energy of 511 keV, at exactly the same moment and in diametrically opposite directions.  The energy of 511 keV is equivalent to the energy corresponding to the masses of the electrons and positrons involved in the process.

The emission of these two photons originates from the same annihilation process, which is fundamental in determining the speed of light propagation, as it depends on a precise measurement of the relative time of emission of these photons.  In fact, there are countless annihilation processes occurring simultaneously and emitting γ (photons) in all directions, but for the purpose of this experiment and to maintain the coherence we are looking for, we need to detect the two γ coming from the same annihilation process.

 {% asset_img "2.webp" "Figure 02" %}
<p style="text-align: center;">
  Figure 2: Radiation detection system</p>

The γ radiation is detected by two detectors, made up of two photomultipliers (PMTs) with scintillator crystals attached, positioned on a 2.0 m precision rail, with the source in between them, as shown in Figure 02.  One detector remains fixed and the other mobile, i.e. its distance from the source can vary.

# DETECTORS

A radiation detector is a device that, when placed in a medium where there is a radiation field, is capable of indicating its presence.  A radiation detector usually consists of an element or material that is sensitive to radiation and a system that transforms these effects into a value related to a measurement quantity of this radiation [02].

# PHOTOMULTIPLIER TUBES OR PMTs

Photomultiplier tubes (PMTs) are devices that convert light into a measurable electric current.  A PMT, as shown in Figure 03, is essentially an electronic valve with a strong internal vacuum, which converts photons into electrons via the photoelectric effect.  In other words, it absorbs light and emits electrons, which are accelerated towards an anode. On the way, these electrons collide with dynodes that are at higher potentials, and in each of these an electron displaces 3 to 4 new electrons, which are accelerated to the next dynode. In this way, the incident light produces a current that can be measured electronically [03]. The working principle of a photomultiplier valve can be seen in Figure 04.

 {% asset_img "3.jpg" "Figure 03" %}
<p style="text-align: center;">
  Figure 3: What a photomultiplier valve looks like (modified [03])</p>
 {% asset_img "4.jpg" "Figure 04" %}
<p style="text-align: center;">
  Figure 4: Working principle of a photomultiplier valve (modified [03]) </p>

Thus the number of electrons pulled out grows and forms an electronic pulse. This pulse increases until it reaches the last dynode, called the anode, as shown in Figure 04.

A voltage of 2200V was applied to the PMTs used in this experiment.

# SCINTILLATORS

Scintillators are materials that are sensitive to radiation [04].  The scintillator consists of a transparent crystal, as shown in Figure 05, which becomes fluorescent when hit by ionizing radiation, i.e. this detector operates due to the fact that certain materials, when hit by ionizing radiation, emit a photon, i.e. a scintillation.

 {% asset_img "5.jpg" "Figure 05" %}
<p style="text-align: center;">
  Figure 5: Example of scintillating crystals </p>

Still looking at Figure 04, it can be seen that scintillators cannot be used on their own; they must be coupled to a photomultiplier, which will transform the light signal emitted by the scintillator into an electrical signal.

There are basically two types of scintillators in common use in nuclear and particle physics: organic or plastic scintillators and inorganic or crystalline scintillators [06]. 

The mechanism of scintillation in organic materials is quite different from that in inorganic crystals. Inorganic scintillators are better at detecting gamma rays and X-rays than organic scintillators. This is due to their high density and atomic number, which provides a high electron density[06].

# SCINTILLATORS INVOLVED

The scintillator crystals used in this experiment were BaF2 (Barium Fluoride) and CsF (Cesium Fluoride), which are inorganic and have better energy resolutions.

 {% asset_img "6.webp" "Figure 06" %}
<p style="text-align: center;">
  Figure 6: Radiation detection system - photomultipliers (PMTs) and scintillator crystals </p>

# SIGNAL PROCESSING

When the 511 keV photon hits the scintillator, it excites the atoms of the material causing the emission of several low energy photons, which are collected by the PMTs and which in turn convert photons into electrons.

Radiation detectors provide a variety of information about the detected particles in the form of electrical signals, for example through the polarity, amplitude or shape of the observed electrical pulse [06]. 

Signals generally carry information in two ways: analog or digital. An analog signal continuously encodes information, varying one or more of its characteristics depending on the value of the information. Some detectors generate pulses whose amplitude is proportional to the energy deposited there [07].   The digital pulse or logic pulse has a fixed shape and only two possible states: yes or no.  In order to extract information, the signals must be processed by an electronic system [07].   

It is necessary to distinguish between fast and slow signals in an electronic system. Fast signals are those with rise times in the order of a few ns or less, while slow signals have rise times in the order of hundreds of ns or more. Fast signals are important for time measurements (coincidence). On the other hand, slow signals are generally less susceptible to noise and offer better information on pulse height [07].

# NUCLEAR ELECTRONICS

In nuclear electronics, the two states of a logic signal are standardized by the NIM convention (Nuclear Instrument Module). Read more about NIM here.

One logic signal is usually taken as 0V, i.e. no pulse present, and the other at a fixed voltage level. Due to the obvious difficulty of generating a pulse with a certain exact voltage level, a voltage band is defined as the presence of a signal.

The system widely used in particle physics experiments is the NIM, which is an electronic system for measurements and a coincidence system. Each of the electronic modules that make up the NIM, shown in Figure 07, receive and emit characteristic electronic pulses. The appropriate combination of these pulses will lead to the final result.

 {% asset_img "7.jpg" "Figure 7" %}
<p style="text-align: center;">
  Figure 7: Electronic modules that make up the Nuclear Instrumentation Module (NIM) standard </p>

# PNIM STANDARD

The first and simplest standard established for nuclear physics and high energies is the modular system called NIM, which was established in 1964. In this system, as shown in Figure 07, the basic electronic apparatus consisting of amplifiers, discriminators, are built in the form of modules according to standardized mechanical and electrical specifications. These modules, in turn, fit into standardized bins that supply the modules with standardized voltages. The NIM system offers a great advantage in the flexibility of changing and upgrading instruments, as any NIM module will fit into any bin.

A specific electronic system for a given application can be created easily, simply by installing the necessary modules in a NIM bin and connecting them correctly. After the experiment, the modules can be transferred to another NIM system, combined with other modules for another application, leading to reduced costs and more efficient use of the instruments. For this reason, the NIM system is adopted worldwide by research laboratories and commercial enterprises [20].   NIM modules include both analog and digital instruments. As mentioned above, analog signals carry information in their height or shape, so they have varying heights and shapes. Digital or logic signals, on the other hand, are fixed in shape and have only two possible states: yes or no, which can be used to indicate the presence or absence of a particle in a detector, for example [08].  

There are two standard types of logic: slow-positive logic and fast-negative logic. The first refers to signals with slow rise times, in the order of hundreds of nanoseconds (ns) or more. They have a positive polarity and are used with slow detection systems. A disadvantage of these signals is that they cannot be transmitted over very long cables, as the signal becomes very attenuated as the wire size increases.

Fast-negative logic, also called NIM logic, uses extremely fast signals with rise times of around 1 ns and comparable widths. This type of signal is often used in experiments using fast detectors. Fast signals can be transmitted over relatively long cables because they are not attenuated [08].   The output signals from the PMTs are routed to the NIM acquisition system. Read more about the modules that make up the NIM standard [click here](https://scientistsnotes.github.io/2024/08/20/post-7/).

# BASIC COINCIDENCE TECHNIQUE

A very important technique in nuclear physics is the determination of coincidences. Just like the selection of pulse heights, the coincidence in time between two or more events serves as a powerful criterion for distinguishing reactions. The technique consists of converting the analog signal from the detectors into logical signals and sending them to a coincidence module. If two signals are indeed coincident, then a logic signal is produced at the output. Coincidence is considered to be the overlapping of signals. So a coincidence output signal is produced if any part of the incident signals overlap. So all pulses arriving within a time equal to the sum of their widths are recorded as coincident [08].    

Figure 08 shows the assembly of the experimental setup, including its electronic device.  Figure 09 shows a schematic of the electronic modules that make up the NIM.

{% asset_img "8.jpg" "Figure 8" %}
<p style="text-align: center;">
Figure 8: NIM (Nuclear Instrumentation Module) standard assembly system used in the experiment </p>

{% asset_img "9.webp" "Figure 9" %}
<p style="text-align: center;">
Figure 9: Schematic of the assembly of the NIM (Nuclear Instrumentation Module) standard [09] </p>

The signals coming out of the photomultipliers are sent to the NIM acquisition system, which is made up of electronic circuits for measuring coincidence records. Three types of coincidence were performed: slow, fast and slow-fast.  The slow and fast coincidences end up in an ADC module with a computer interface.

# SLOW COINCIDENCE

Slow coincidence consists of signals that aim to generate a digital pulse whenever two signals coincide within an energy window of 511 keV.  Figure 10 shows the entire assembly diagram for slow coincidence.  In this coincidence, the signals of interest come from the intermediate dynodes of the PMTs, as these signals have good energy resolution.  The pulse previously obtained from the dynode has positive polarity, an amplitude of approximately 0.5V and a width of 20ns, and passes through the preamplifier. The preamplifier outputs pulses with a fast rise and a slow fall, which are fed to the amplifier, which is an electronic module that makes it possible to regulate the input and output pulse. In this case, the output is bipolar.

{% asset_img "10.jpg" "Figure 10" %}
<p style="text-align: center;">
Figure 10: Schematic of the assembly of the NIM pattern for slow coincidence [09]</p>

At the output, all the PMT output pulses appear at this amplitude.  However, we are specifically interested in the amplitude for the Rγ of 511 KeV, so we used the single-channel module, where it is possible to delimit the amplitudes, creating the energy window of interest.  In this configuration, the 511 keV window to be analyzed is delimited. The single-channel module emits a digital pulse whenever the energy condition is met. This pulse passes through a delay module which is used to synchronize the delays, since the detectors are at different distances from each other.

These pulses are sent to a coincidence module to establish the time coincidence, which limits its output depending on the delays of the pulses coming from mono-channel 1, which is the start, and mono-channel 2, which is the stop. The coincidence module emits a positive logic pulse which is sent to the ADC.

# QUICK COINCIDENCE

Figure 11 shows the entire assembly scheme for the fast coincidence. The fast coincidence process is carried out with the anodes of the PMTs, as they have the best temporal resolution. These pulses, with negative polarity, have a fast rise and slow fall time, also due to the Rγ of 511 keV. They pass through a fast discriminator circuit (CFD) where they are digitized and modulated, with an amplitude of 0.8V and a width of 10 ns. The CFD is the module that receives the analog signal and emits a temporal pulse regardless of the amplitude of the input signal.


{% asset_img "11.jpg" "Figure 11" %}
<p style="text-align: center;">
Figure 11: Schematic of the assembly of the NIM standard for rapid coincidence [09]</p>

These CFD output pulses are processed in the TAC, which generates an electrical voltage proportional to the delay between them.  The two CFD pulses go, one of them to the TAC's START input, and the other to the STOP input, where they undergo a coincidence process.

The TAC's output pulse has an amplitude proportional to the differences in arrival times at the START/STOP inputs. This coincidence provided by the TAC also aims to filter out the γ coming from the same electron-positron annihilation event. The electrical voltage generated by the TAC is recorded by the ADC whenever there is a Gate pulse. This ensures that the time difference is only recorded when the energy condition is met.  The ADC module sends the voltage, converted into a byte, to the computer.

# SLOW-FAST COINCIDENCE

In the third coincidence mode, called slow-fast, the pulses coming from the single-channel access the ADC Gate, which allows access to the fast coincidences coming from the TAC.  From this stage, the final filtering is carried out for the pulses coming from the electron-positron annihilation process, with the maximum guarantee that the recorded processes come from the same event.

# TIME CALIBRATION

It is necessary to calibrate the timing, via the TC module, according to the ADC channels. The TC produces two pulses emitted with a high-precision variable delay, with a positive START/STOP output polarity, which are sent to the TAC's START/STOP inputs, where they undergo a coincidence process.   For time calibration, pulses with a 10 ns delay were sent to the TAC. From the TAC output, the pulse is sent to the ADC, completing the time calibration. After the time calibration, data collection begins.

---
This post is part of the monograph written at the end of my undergraduate studies at the Universidade Federal Fluminense (UFF). Due to the size of the content, this post will be divided into three parts: theoretical [click here](https://scientistsnotes.github.io/2024/08/20/post-7/), experimental and analysis of results [click here](https://scientistsnotes.github.io/2024/09/09/post-10).
---

# References

[01]  HEATH, R. L. Scintillation Spectrometry – Gamma-Ray Spectrum Catalogue, 1964 - Rev. Electronic Update 1997.  Available in:

https://drive.google.com/file/d/1NrTuMk6pvcmwhBaH7hlTq0IvlFMTDl07/view 

[02]  Detectores de Radiação - International Atomic Energy Agency.  Available in:

https://inis.iaea.org/collection/NCLCollectionStore/_Public/45/073/45073471.pdf 

[03]  BRAGA, Newton C.  Como Funcionam os Sensores Fotoelétricos, 2012.  Available in:

 https://www.newtoncbraga.com.br/index.php/como-funciona/4883-art644.html 

[04]  Detectores e Sensores - Desenvolvimento de detectores e sensores de radiação. IPEN - Instituto de Pesquisas Energéticas e Nucleares.  de Pesquisas Energéticas e Nucleares. Available in:

https://www.ipen.br/portal_por/portal/interna.php?secao_id=736

[05]  MODI, Vilesh.   Global Cesium Iodide Market 2017: Industry Trends and Manufactures Analysis.  Available in:

https://www.egypt-business.com/ticker/details/1724-global-cesium-iodide-market-2017-industry-trends-and-manufactures-analysis/120171 

[06]  CONNOR, Nick.   O que é Cintilador Inorgânico – Cristais de Cintilação – Definição, Radiation-dosimetry.org, 2020.  Available in:

https://www.radiation-dosimetry.org/pt-br/o-que-e-cintilador-inorganico-cristais-de-cintilacao-definicao/ 

[07]  SANTOS, Antônio Carlos Fontes.  Processamento de sinais I - Laboratório de Colisões Atômicas e Moleculares - Departamento de Física Nuclear, UFRJ, 2008.  Available in:

https://www.if.ufrj.br/~toni/capitulo_02.pdf 

[08]  SANTOS, Antônio Carlos Fontes.  O Padrão NIM - Laboratório de Colisões Atômicas e Moleculares - Departamento de Física Nuclear, UFRJ, 2008.  Available in:

https://www.if.ufrj.br/~toni/capitulo_5.pdf 

[09]  MASSAFFERRI, André Rodrigues. Instrumentação em Física de Altas Energias – Práticas Experimentais – Escola Avançada de Física Experimental, CBPF, 2016.  Available in:

https://drive.google.com/file/d/0B4whBKBOBYUYY0FVTm9NM285Z2s/view?resourcekey=0-NswahCN6Irh0IeCHVVKuyA