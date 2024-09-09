---
title: Experiment - Infrared Spectroscopy in the Analysis of Microplastics 
date: 2024-09-09 09:25:42
tags: [Spectroscopy, Experimental Physics, Microplastic, Computational physics]
---

# Objective

The aim of this experiment is to classify the microplastics collected. In order to do this, it will be necessary to collect sand from Jurujuba beach in Rio de Janeiro. To prepare the collected sample through procedures to remove residues that make it difficult to analyze the object studied and finally, to generate the spectrogram of the sample and then identify which polymer this sample belongs to. The Python language will be used to help identify the samples collected.


## Material

* The material used will be:

* MIRS system (Figure 01)

* Oven for drying the samples (Figure 02)

* Sieve with electronic vibration system (Figure 03)

{% asset_img "1.webp" "Figure 01" %}
<p style="text-align: center;">
  Figure 1: MIRS system  <br>
  Source: Teacher material  </p>
{% asset_img "2.webp" "Figure 02" %}
<p style="text-align: center;">
  Figure 2: Oven for drying the samples <br>
  Souruce: Teacher material </p>
{% asset_img "3.webp" "Figure 03" %}
<p style="text-align: center;">
  Figure 3: Sieve with electronic vibration system   <br>
  Source: Teacher material </p>

## Study area

 All the samples were taken at Jurujuba beach [Figure 4]. The site was chosen because of the characteristics of the beach. As it is a fishing colony, it is easy to find fishing gear in the sand, untreated sewage and the shape of the beach as it has a “horseshoe” shape which serves as a filter for the sea current, meaning that right after the sea rebound we can find a lot of garbage from the ocean and other places on the beach.

 {% asset_img "4.webp" "Figure 04" %}
<p style="text-align: center;">
  Figure 4: Jurujuba beach   <br>
  Source: Google imagen </p>

# Sample collection

Sediment samples were collected in 50x50 $cm^2$ quadrants, 1 cm deep. Samples were taken from 5 different locations 20 meters apart.

 {% asset_img "5.webp" "Figure 05" %}
<p style="text-align: center;">
  Figure: Sediment samples   <br>
  Source: Teacher material </p>

# Sample preparation

The samples were dried and sieved [Figure 05] through 1 mm and 5 mm sieves to separate grains and possible microplastics in this fraction. Visible plastics were separated manually [Figure 06].

{% asset_img "6.webp" "Figure 06" %}
<p style="text-align: center;">
  Figure 5: Samples being dried and sieved   <br>
  Source: Teacher material </p>

After separation, the samples will undergo various processes to remove impurities in order to obtain a purer sample for computer analysis and spectrograms. After separation, the samples will undergo various processes to remove impurities in order to obtain a purer sample for computer analysis and spectrograms.

{% asset_img "7.webp" "Figure 07" %}
<p style="text-align: center;">
  Figure 6: Samples being dried and sieved   <br>
  Source: Teacher material </p>

# Sample analysis

The analysis was carried out on two samples, obtained by the students of the Physics course (UFF). The MIRS system was used to obtain the spectrogram. In [Figure 07] we can see the spectrum of each sample.

# Result

Remember that the code used to identify the sample can be found at: https://github.com/Wendelvsouza/analise_de_microplasticos

To find out what type of material the samples are made of, the samples were compared with the polymer table [Table 1] using python (code can be seen here).

 

1 - Collect all possible peaks from each sample;
2 - Compare each value collected with the values in the table for each polymer;
3 - Apply the absolute difference between the value collected and the values in the table, defining conditions for the absolute difference to reduce the error;
4 - Identify which polymer the sample belongs to.

 

The samples and the corresponding polymer are:

 

Sample 1 -> High-density polyethylene (HDPE)
Sample 2 -> High-density polyethylene (HDPE)
Sample 3 -> High-density polyethylene (HDPE)
Sample 4 -> High-density polyethylene (HDPE)
Sample 5 -> Polypropylene (PP)

# Discussion and analysis of errors

Even if we manage to characterize the samples, we must consider some errors, which are:


1 - An error in the algorithm, which was unable to collect/analyze enough data to correctly classify the polymer;

2 - Another error we can consider is that the equipment is out of calibration or even that the sample has not been fully purified;

3 - We also have to consider external factors, for example any slightest disturbance during the reading may suffer a small variation causing these fluctuations;

4- We must also consider the uncertainty of the apparatus.


Looking at the spectra, we noticed some prominent peaks that were not identified in the polymer choices, one of the reasons being that they are contaminants, i.e. some substance contaminated the sample (polymer has the ability to adsorb chemical elements) and it was not possible to remove it during the cleaning process, so when we analyzed it we were able to visualize its presence using the MIR method.

# Conclusion

The main objective of the report was met, we were able to identify which polymer the samples were made of, that is, the polymers are HDPE and PP. Plastics have been widely used by industries due to their ability to be molded into various objects of interest and their low manufacturing cost. In fact, plastic has come to make life easier for human beings. The problem occurs after its use, i.e. its improper disposal and the formation of microplastics (plastic degradation, fragments of car tires, confetti, cosmetics, etc.). When these plastic particles enter the ocean, they cause immeasurable damage, as they can harm the aquatic eco-system. As already mentioned, when microplastics are ingested, they feed until they reach humans. Some countries (Sweden, the United States and Canada, for example) have adopted a ban on microplastics in the composition of materials. Some countries are abandoning plastic bags and straws (Brazil, Indonesia, among others). [12]

 
Even though some countries are taking steps to stop this degradation of nature by polymers, the fight is difficult. It is estimated that by 2050 there will be more plastic than fish in the oceans [3][4].


In order to reduce the damage caused by microplastics, certain measures should be taken, such as banning the use of this type of material, as this will reduce the amount of plastic and prevent pollution of the marine environment. Environmental education actions should also be considered, as they promote awareness and critical thinking about the problem, causing debates where everyone wins, not only humans but also animals and nature as a whole.

# Appendices

{% asset_img "8.webp" "Figure 08" %}
<p style="text-align: center;">
  Figure 8: Sample graphs </p>

{% asset_img "9.webp" "Figure 09" %}
<p style="text-align: center;">
  Figure 9: Polymer table<br>
  Source: Teacher material </p>

# References

[1] Teacher material unavailable

[2] Braun, S - Onde o plástico é proibido no mundo - 30/06/2019. Disponível em:

https://www.dw.com/pt-br/onde-o-pl%C3%A1stico-%C3%A9-proibido-no-mundo/a- 49398718
 
[3] The New Plastics Economy Rethinking the future of plastics, World Economic Forum, 2016. Disponível em: http://www3.weforum.org/docs/WEF_The_New_Plastics_Economy.pdf


[4] Presse, F - Oceanos terão mais plástico do que peixes em 2050 diz estudo. G1, 20/01/2016 Disponível em: http://g1.globo.com/natureza/noticia/2016/01/oceanos-terao-mais-plasticos-doque-peixes-em-2050-diz-estudo.html