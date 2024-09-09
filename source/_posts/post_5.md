---
title: EXPERIMENT - The interaction of radiation with matter
date: 2024-07-14 00:00:00
categories: [Computational Physics]
tags: [Experimental Physics, Microplastics]
---

# EXPERIMENT
 
In this post we aim to create the image of the chest simulation, since the previous post only covered the theoretical part of the experiment. This experiment aims to describe more clearly the process of transforming radiation into an image and the interaction of radiation with different materials, improving our understanding of how radiation interacts.

# MATERIAL
 
The equipment used in this experiment was:
 
- Radioactive source: Cesium-137.
- Collector: Geiger-Muller counter.
- Acrylic plates.
- Millimeter paper. 
    * 2.0 mm thick
    * 36 cm high
    * 3.0 cm wide

- A simulation of a thorax cut in half:
 
    * Soft tissue: Styrofoam plate
    * Rib bone: Bovine tibia
    * Lung tissue: Silicone rubber
    * Heart: Aircrete
    * Pacemaker: Lead


{% asset_img "a.png" "Figure 1a"%}
<p style="text-align: center;">
  Figure 1a: Simulation of the thorax used in the experiment.   <br>
  Source: Lecture material by Professor Dr. Meigikos. </p>

{% asset_img "b.png" "Figure 1b"%}
<p style="text-align: center;">
  Figure 1b: Actual assembly used in the experiment.  <br>
  Source: Lecture material by Professor Dr. Meigikos.  </p>


# EXPERIMENT
 
To set up the experiment, we placed the thorax between the collector and the radioactive source [Figure 1b], and the GM counter was placed 1.5 cm away. In order to produce a good quality image, we had to collect as many measurements as possible. So, using a piece of graph paper that has 1.0 cm² in each square, we were able to take measurements pixel by pixel. Data was collected from 1656 different positions on the graph paper. Each square was exposed to radiation for 60 seconds, which means that by relating each pixel to the number of counts, we can then assemble the image by relating each number of events (pixel) to a color.

## OBSERVATIONS
  
The distance between the source and the detector must be minimal and fixed throughout the experiment so that the transmitted photons only pass through each square of paper and are fully captured by the counter.
To find the exact distance we must use the concept of shock section and solid angle[2], from which we obtained a value of 4.5 cm measured from the source.

# ERROR ANALYSIS
 
Some possible errors that should be considered[3]:
 
Instrumental errors:
 
Alignment of the source with the GM counter (obeying the solid angle rule) o equipment that is not in perfect condition or calibrated.
 
Observational errors:
 
Wrong reading of measurements, wrong units, etc.
 
Environmental errors:
 
As the laboratory was not isolated, we may have collected radiation from various elements present there, which could then significantly alter the result.
 
Random errors:
 
Fluctuations in measurements.



# DISCUSSION OF THE RESULTS
 
The [Table 1] helps us to understand the effects that occur during the photon's interaction with matter, i.e. as we increase the photon's energy, the probability of the photoelectric effect occurring decreases and the probability of the Compton effect occurring increases, in accordance with the theory ([Figure 4] from the post on the theoretical part ,click here). In other words, by increasing the energy above 1022 keV we start to have a probability of pair production occurring. As you can see in [Figure 2], we have the image produced with the data collected from the experiment. The Python programming language was used to interpret the data, and by defining a color palette, it was possible to associate a color with each count number. Comparing [Figure 1a] and [Figure 2] we can easily identify each object in the digitized image. We can use the image as a heat map and associate each region with the amount of radiation collected by the counter.
 
It is known that the density of the material and the atomic number influence the attenuation and consequently the quality of the image. By looking at [Table 2] we can understand why each object has its characteristic color and understand the effect of attenuation on the respective objects. For example, comparing [Figure 1a] and [Figure 2], the pacemaker (lead) has a very inharmonious coloration, because it has a high density, the greater its attenuation, so that the counter will only count (on average) 100 emerging photons. Looking at the muscle (Styrofoam), we can see that it is a natural object because it is distributed harmoniously in the image (the opposite of lead), we see that its density is much lower than lead, so its attenuation power is much lower and consequently the counter will count more emerging photons (on average 550).
 
<p style="text-align: center;">
  Table 1: Effects of photon interaction with material.  <br>
   Source: Lecture material by Professor Dr. Meigikos.  </p>
{% asset_img "c.png" "Table 1:" %}


{% asset_img "d.png" "Figure 2" %}
<p style="text-align: center;">
  Figure 2: Image generated from the data collected.   <br>
  Source: Lecture material by Professor Dr. Meigikos  </p>
 
<p style="text-align: center;">
  Table 2: Materials used and their respective densities.   <br>
  Source: Lecture material by Professor Dr. Meigikos. </p>
{% asset_img "e.png" "Table 2" %}

# CODE
 
The code used to generate the image can be seen in Figure [3]. The .csv file containing the collected data and the code in ipynb can be found on GitHub 


<p style="text-align: center;">
  Code: Python code used to generate the image.  </p>
```python

from pathlib import Path
import pandas as pd

from range_key_dict import RangeKeyDict

#Place the directory where the counts.xlsx file is contained.
v = Path(r"directory_here")

data = pd.read_excel(v,index_col=None, header=None)

colors = RangeKeyDict({
#azul    
    (0, 101): "#0200a0",
    (101, 131): "#0200d7",
    (131, 176): "#0001fc",
    (176,191 ): "#0661f9",
    (191, 231): "#0486ff",
    (231, 241): "#00c0f8",
    (241, 261): "#01f7fe",
    (261, 291): "#31fdd0",
    (291, 301): "#48ffb0",
# green
    (301, 326): "#6eff8f",
    (326, 361): "#adff4d",
# yellow    
    (361, 376): "#eefe0f",
    (375, 386): "#fffc03",
    (386, 396): "#ffdf00",
    (396, 411): "#ffcf02",
    (411, 426): "#ffae03",
# orange
    (426, 440): "#fc9100",
    (440, 447): "#ff7f00",
# red
    (447, 461): "#fe5900",
    (461, 471): "#fe3e03",
    (471, 501): "#fd1f00",
    (501, 511): "#e40000",
    (511, 526): "#cd0200",
    (526, 536): "#c20000",
    (536, 551): "#900000",
    (551, 600): "#7b0106",    
});
 
pulmao = data.style.applymap(lambda x: "background-color: {}".format(colors[x]))
pulmao.to_excel("Torax.xlsx")

```
# CONCLUSION
 
As expected, the experiment was able to produce a digital image using electromagnetic radiation, using the Python programming language to transform data into colors, simulating radiography equipment that is widely used in industries, the medical field, security systems, etc. As low-cost material was used, this experiment can easily be reproduced in schools, technical courses, science fairs, etc.
 
The physics behind the experiment is extremely rich and involves various concepts that contribute to the construction of scientific knowledge in a meaningful way. One suggestion for a future experiment is to try to reproduce a higher quality digital image, for example by reducing the area of the graph paper from 1.0 cm² to 0.5 cm² (or less) and consequently increasing the number of measurements.

# REFERENCE:

[1] Material by Professor Dr. Meigikos.
 
[2] Solid Angle - Center for teaching and applied research - 2003. Available at:
 
http://www.cepa.if.usp.br/e-fisica/eletricidade/basico/cap00_intr/cap00intr_03.htm
 
[3] Preston, W and Dietz, E - "The Art of Experimental Physics" - Ed: John Wiley & Sons - New York, 1991. Available at:
 
https://wwwp.fc.unesp.br/~jhdsilva/Tipos_de_Erros_Experimentais.pdf
