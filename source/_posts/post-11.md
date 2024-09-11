---
title: Nuclear Electronics - NIM Standard
date: 2024-09-11 06:40:37
categories: [Physics]
tags: [Physics, Nuclear physics, Experimental Physics, Radiation]
mathjax: true
---

When we talk about Experimental Nuclear Physics, as we did in the post on “speed of propagation of electromagnetic radiation” [click here](https://scientistsnotes.github.io/2024/09/09/post-9/), we often use specific Nuclear Instrumentation modules, because in nuclear electronics, the two states of a logic signal are standardized by the NIM (Nuclear Instrument Module) convention.

One logic signal is usually 0V, i.e. no pulse present, and the other at a fixed voltage level. Due to the obvious difficulty of generating a pulse with a certain exact voltage level, a voltage band is defined as the presence of a signal.

The system widely used in particle physics experiments is the NIM, which is an electronic system for measurements and a coincidence system. 

Each of the electronic modules that make up the NIM, shown in figure 01, receive and emit characteristic electronic pulses. The appropriate combination of these pulses will lead to the final result.

{% asset_img "1.jpg" "Figure 01" %}
<p style="text-align: center;">
  Figure 1: Electronic Modules that make up the NIM Standard.</p>

# NIM STANDARD: 

The first and simplest standard established for nuclear physics and high energies is the modular system called NIM, which was established in 1964. In this system, as shown in figure 01, the basic electronic apparatus consisting of amplifiers, discriminators, etc. are built in the form of modules according to standardized mechanical and electrical specifications. These modules, in turn, fit into standardized bins that supply the modules with standardized voltages. The NIM system offers a great advantage in the flexibility of changing and upgrading instruments, as any NIM module will fit into any bin.

A specific electronic system for a given application can be created easily, simply by installing the necessary modules in a NIM bin and connecting them correctly. After the experiment, the modules can be transferred to another NIM system, combined with other modules for another application, leading to reduced costs and more efficient use of the instruments. For this reason, the NIM system is adopted worldwide by research laboratories and commercial enterprises [01].

# NIM LOGIC SIGNALS:

NIM modules include both analog and digital instruments. As mentioned above, analog signals carry information in their height or shape, so they have varying heights and shapes. Digital or logical signals, on the other hand, are fixed in shape and have only two possible states: yes or no, which can be used to indicate the presence or absence of a particle in a detector, for example[01].  

# STANDARD LOGIC SIGNALS:

There are two standard types of logic: slow-positive logic and fast-negative logic. The first refers to signals with slow rise times, in the order of hundreds of nanoseconds or more. They have a positive polarity and are used with slow detection systems. One disadvantage of these signals is that they cannot be transmitted over very long cables, as the signal becomes very attenuated as the wire length increases.

Fast-negative logic, also known as NIM logic, uses extremely fast signals with rise times of around 1 ns and comparable widths. This type of signal is often used in experiments using fast detectors. Fast signals can be transmitted over relatively long cables because they are not attenuated [01].

# ELECTRONIC MODULES:

The output signals from the PMTs are sent to the NIM acquisition system, consisting of:

# PREAMPLIFIER:

{% asset_img "2.jpg" "Figure 02" %}
<p style="text-align: center;">
Figure 2: Electronic Module - Preamplifier.</p>

Virtually all particle detectors provide a charge pulse Q at their output, which is produced by the incident radiation. For most detectors, however, the charge is so small that it is difficult to process the pulse.  Therefore, the first element in the signal processing chain is the preamplifier, shown in figure 02, whose basic function is to amplify weak signals coming from a detector. The preamplifier can be seen as a high-gain inverting amplifier [02]. 

# AMPLIFIER:

The functions of the amplifier are: to amplify the signal from the preamplifier and to give it a convenient shape, i.e. to format the pulse for subsequent processing [02].  Figure 03 shows the amplifier module used in this experiment. 

# DISCRIMINATOR

The discriminator is a device that only responds to input signals with a pulse height greater than a certain threshold. If this criterion is met, the discriminator responds by sending a standard logic signal, otherwise no response is sent. The most common use of the discriminator is to block low amplitude noise. Real pulses that have sufficient amplitude to trigger the discriminator are transformed into logical pulses for further processing.

An important feature of the discriminator is the triggering method. Because it is used for time measurements, it is important that the relationship between the time the pulse arrives and the time the logic pulse at the output is sent is constant.  In most discriminators, the trigger occurs when the pulse crosses the threshold [02].   

Figure 03 shows the discriminator module used in this experiment.

# SINGLE-CHANNEL ANALYZER (SCA):

The SCA (Single-Channel Analyser) is a device that classifies analog signals at its input according to their height. Similar to the discriminator, it has a threshold below which pulses are blocked and an upper level above which pulses are also blocked. Thus, only signals that are between these two levels, called a window, cause a response at the output of the SCA, i.e. a standard logic signal.  This makes it possible to choose the voltage of interest [02].   Figure 03 shows the SCA module used in this experiment.

{% asset_img "3.jpg" "Figure 03" %}
<p style="text-align: center;">
Figure 3: Electronic Modules - Amplifier, Discriminator, SCA, Universal Coincidence and Delay.</p>

# ANALOG-DIGITAL CONVERTERS (ADCs):

The ADC is a device that converts any information contained in an analog signal into an equivalent digital form. This instrument is the fundamental link between analog and digital electronics [02].  

The ADC used in this experiment is shown in figure 04.

# MULTI-CHANNEL ANALYZER (MCA):

MCA analyzers are devices that sort pulses according to their height and count them (N) for each height in a multichannel memory. The contents of each channel can then be displayed on a screen or printed out to give the spectrum of pulse heights. The MCA works by digitizing the amplitude of the incident pulse with an ADC [02].  

# TIME-AMPLITUDE CONVERTER (TAC) - THE START-STOP:

The TAC is a module that converts a time difference between two logic pulses into an output pulse, the height of which is proportional to the time difference. The pulse can then be analyzed by an MCA, to give a spectrum as a function of the time interval, followed by the ADC, which will digitize the output signal. Units such as TAC + ADC are called TDC (Time-to-Digital Converter).

The time measurement in a TAC is triggered by a START pulse and terminated by a STOP pulse.  The START signal turns on a counter that counts pulses and this counter is turned off when a STOP signal arrives, resulting in a number proportional to the time interval between pulses [03].  

Figure 04 shows the TAC module used in this experiment.

# TEMPORAL CALIBRATOR (TC):

The TC (Time Calibrator) electronic module emits pulses in multiple amplitude sequences, according to the internal calibration that is set by the control switches. The pulses with positive polarity from the TC START/STOP output are routed to the TAC START/STOP inputs, where they undergo a coincidence process [03].   

Figure 04 shows the TC module used in this experiment.

{% asset_img "4.jpg" "Figure 04" %}
<p style="text-align: center;">
Figure 4: Electronic Modules - Amplifier, Discriminator, SCA, Universal Coincidence and Delay.</p>

# DELAY MODULE:

This module is a delay generator, which adjusts the pulses in relation to time according to the distance of the PMTs from the source.

Figure 03 shows the Delay module used in this experiment.

---

This post is part of the monograph written at the end of my undergraduate studies at the Fluminense Federal University (UFF). To see: Theory: Speed of propagation of electromagnetic radiation [click here](https://scientistsnotes.github.io/2024/08/20/post-7/), experiment [click here](https://scientistsnotes.github.io/2024/09/09/post-9/) and analysis of results [click here](https://scientistsnotes.github.io/2024/09/09/post-10/).

---

References:

[01]  SANTOS, Antônio Carlos Fontes.  O Padrão NIM - Laboratório de Colisões Atômicas e Moleculares - Departamento de Física Nuclear, UFRJ, 2008.  Available at:

[capitulo_5.pdf (ufrj.br)](https://www.if.ufrj.br/~toni/capitulo_5.pdf)

[02]  SANTOS, Antônio Carlos Fontes.  Processamento de sinais II - Laboratório de Colisões Atômicas e Moleculares - Departamento de Física Nuclear, UFRJ, 2008.  Available at:

[Processamento de Sinais II (ufrj.br)](https://www.if.ufrj.br/~toni/capitulo_5.pdf)

[03]  SANTOS, Antônio Carlos Fontes.  Sistemas de Medida de Tempo - Laboratório de Colisões Atômicas e Moleculares - Departamento de Física Nuclear, UFRJ, 2008.  Available at:

[capitulo_06.pdf (ufrj.br)](https://www.if.ufrj.br/~toni/capitulo_06.pdf)