---
title: DATA ANALYSIS - Measuring the speed of propagation of electromagnetic radiation.
date: 2024-09-09 15:46:45
categories: [Physics]
tags: [Physics, Nuclear physics, Experimental Physics, Radiation]
mathjax: true
---

In previous posts I talked about the theory of the speed of propagation of electromagnetic radiation [click here](https://scientistsnotes.github.io/2024/08/20/post-7/) and showed how the experimental setup was done [click here](https://scientistsnotes.github.io/2024/09/09/post-9/). Now, we will discuss the results obtained in this experiment and compare them with other results found previously.

After the acquisition, the data analysis began. To do this, we used a dedicated software package developed by CERN called ROOT, as shown in Figure 01. ROOT is an object-oriented program originally designed for analysis and [data acquisition](https://en.wikipedia.org/wiki/Data_acquisition) in particle and high-energy physics experiments and contains several features specific to this field, such as [histogram](https://en.wikipedia.org/wiki/Histogram) and [graph](https://en.wikipedia.org/wiki/Graph_of_a_function) creation to visualize and analyze [distributions](https://en.wikipedia.org/wiki/Distribution_(mathematics)) and [functions](https://en.wikipedia.org/wiki/Function_(mathematics)), [curve fitting](https://en.wikipedia.org/wiki/Curve_fitting), [statistical](hhttps://en.wikipedia.org/wiki/Statistics) tools used for [data analysis](https://en.wikipedia.org/wiki/Data_analysis), mathematical functions among many others. It maintains its libraries written in C++.

{% asset_img "1.jpg" "Figure 01" %}
<p style="text-align: center;">
  Figure 1: Dedicated software package for data analysis</p>

ROOT has been designed for high [computing efficiency](https://en.wikipedia.org/wiki/Computer_performance), as it is required to process data from the [Large Hadron Collider](https://en.wikipedia.org/wiki/Large_Hadron_Collider) (LHC) experiments estimated at several [petabytes](https://simple.wikipedia.org/wiki/Petabyte) per year. 

In order for ROOT to interpret and analyze the data, the C++ programming language was used.  It was therefore necessary to develop a script which, when run by ROOT, loaded all the data needed for analysis and, at the end, created histograms, curve fits and the calculation of the final result. This script was developed by Prof. Dr. André Massafferri Rodrigues and adjusted according to the data demand of each experiment.  

When ROOT was fed with the data obtained, as the first step in the analysis, the calibration spectrum was created by distributing the ADC channels referring to the temporal calibration pulses, shown in Figure 02-A, and adjusting it, creating a calibration line shown in Figure 02-B, where the delay time is related to the ADC channels. 

Then, the data distributed over the channels that appear on the ADC, as shown in Figure 02-A, is transformed into time. When ROOT makes this transformation, it generates a straight line, using the equation:

$$y = ax + b$$ 

where corresponds to time, corresponds to the calibration result in the final position, the ADC Channel and the calibration result in the initial position, as shown in Figure 02-B.

Therefore, using the calibration line, it was possible to relate the ADC peak channels to the corresponding time.

{% asset_img "2.jpg" "Figure 02" %}
<p style="text-align: center;">
Figure 2-A: Distribution of ADC channels referring to the temporal calibration pulses.<br>
Figure 2-B: Graph of temporal calibration as a function of ADC channels.
</p>

Table 2 shows the result of the calibration spectrum distributed over the ADC channels for the calibration pulses used to construct the graph in Figure 30-A and the time to which each channel peak corresponds.


<p style="text-align: center;">
Table 1: Temporal calibration results.
</p>
{% asset_img "3.jpg" "Table 1" %}

So each variation in the detector's position gives us a variation in time. This is essential for calculating the speed, as we'll see later.

As a second step in data analysis, ROOT also creates graphs of the counts distributed over the ADC channels, adjusting them using Gaussians. Figure 03 shows the distribution of ADC channels for the γ radiation captured from 22Na.

Looking at Figure 02, you can see that with each change in the position of the mobile detector, the peak count shifts to the right in relation to the ADC channel. This shift in position is what makes it possible to calculate the speed, since the time calibration tells us exactly how long the radiation has been flying.

Then, as a final step, ROOT calculates the speed of propagation of the electromagnetic radiation based on this information and creates a graph of the final result of the data collection, as shown in Figure 04.

{% asset_img "4.jpg" "Figure 03" %}
{% asset_img "5.jpg" "Figure 03" %}
<p style="text-align: center;">
  Figure 3: Distribution of ADC channels for γ radiation.</p>
{% asset_img "6.jpg" "Figure 04" %}
<p style="text-align: center;">
  Figure 4: Final result of data collection.</p>

Then, given the variation in time ($ {\Delta t} $ ) and position ($ {\Delta s} $ ), one of the main kinematic equations is used to calculate the average speed:

$$ v = \frac{\Delta s}{ \Delta t} $$

The result obtained in this experiment was:

$$ c = 2.92 x 10^8 m/s $$

When compared to the theoretical value of the speed of light, given by , this experimental result is in the same order of magnitude.  In other words, the electromagnetic radiation emitted by the 22Na source measured in this experimental practice propagates with a value very close to the reference value, achieving 98% of the expected value, which shows how satisfactory this measurement was.

Based on the theoretical reference here, the 22Na source used in this experiment decays, partly emitting a positron (β+ decay) and partly emitting a pair of γs, due to pair production interaction, with a peak energy of 511 keV.  It was commented that it was essential that the emission of the two photons originated from the same annihilation process, as a precise measurement of the emission time of these photons was required. So, using this decay, it was possible to calculate the speed of propagation of the radiation, which is theoretically the same as the speed of propagation of light in a vacuum, i.e. $ c = 2.99796 x 10^8 m/s $.

The experiment consisted of measuring the differences in the time of flight of the pair of γs from the shifts in the positions of the spectra, shown in Figure 03, resulting from the coincidences of the γs detected by the two detector systems, according to the varying distance of one of the detectors from the precision rail.

This experiment was reproduced several times and the value obtained remained within the reference range. Published articles and technical notes show very similar results to those calculated using this experiment, as shown below.

# VARIATIONS OF THIS EXPERIMENTAL PRACTICE

<p style="text-align: center;">
Table 2: Other results obtained for the speed of radiation propagation in different material media.
</p>
{% asset_img "7.jpg" "Table 2" %}

These results lead us to conclude that, although electromagnetic radiation can pass through different materials, its speed can suffer different delays.  This variation is due to the refractive index of each material used. 

Another proposed variation of this experiment was the use of glass tubes containing water.  Table 4 shows the results of another group of experiments using water with or without flux.

<p style="text-align: center;">
Table 3: Other results obtained for the speed of radiation propagation in different material media.
</p>
{% asset_img "8.jpg" "Table 3" %}

As expected, these results show that, regardless of the direction of the water flow, the propagation speed was lower in water than in air.

It's important to note that for each group of data to be compared, the time calibration and all the air propagation data is taken and then the measurements are taken with the different material media.  It is believed that in this way it will be possible to obtain more realistic results than when only comparing the speed with data collected at another time.

All the results presented in Tables 3 and 4 were obtained from experiments carried out at the then Angular Correlation Laboratory/CBPF within the context of the Hyperfine Interactions Measurement Group[02] [03] [04], with their respective conclusions.

Systematic errors can cause the difference in values between the various results presented here.  Unfortunately, as mentioned above, some of the data takes a long time to be collected and in the meantime unforeseen events can get in the way, such as the power grid being switched off, for example.

The main result presented here, although satisfactory, differs from other results presented for the propagation of the speed of electromagnetic radiation in air.

# CONCLUSION

The main objective of this experiment was to measure the speed of propagation of electromagnetic radiation, using a 22Na source, by measuring the variation in the arrival time of a pair of 511keV γs, which are detected by two detectors, one fixed and one mobile.  The coincidence method described here showed good suitability, as the result analyzed, when compared with the value of the speed of light propagation, even at small distances, could be obtained accurately. 

In addition to the result being within the reference range already described, it was also possible to manipulate the electronic equipment and modules that make up the NIM (Nuclear Instrumentation Module) standard, which are widely used in nuclear and particle physics.  In addition to data analysis and adjustments using computer programs, which are also extremely important in experimental physics.

---
This post is part of the monograph written at the end of my undergraduate studies at the Universidade Federal Fluminense (UFF). Due to the size of the content, this post will be divided into three parts: theoretical [click here](https://scientistsnotes.github.io/2024/08/20/post-7/), experimental [click here](https://scientistsnotes.github.io/2024/09/09/post-9/) and analysis of results .

---

# References

[24]  ROOT: Data Analysis Framework.  Available at:

https://root.cern 

[25]  CAVALCANTE, José T.P.D., SILVA, Paulo R.J., SAITOVITCH, Henrique.  Measurements of the Propagation Speed of 511 KeV Gamma-Rays in Air and Other Material Media - CBPF-NF-007/07.  Available at:

cbpfindex.cbpf.br/publication_pdfs/NF00707.2007_12_06_13_59_57.pdf

[26]  NETO, Osmar F. S, L., CAVALCANTE, José T.P.D., SILVA, Paulo R.J., SAITOVITCH, Henrique.  Propagation Speed of Rγ-511 keV in Plastics - CBPF-NF-010/12.  Available at:

https://inis.iaea.org/search/search.aspx?orig_q=RN:43080989

[27]  NETO, Osmar F. S, L., CAVALCANTE, José T.P.D., SILVA, Paulo R.J., SAITOVITCH, Henrique.  Propagation Speed of γ-Radiation (Rγ) in Water with/without Flux - CBPF-NF-017/11.  Available at:

carpedien.ien.gov.br/handle/ien/2759