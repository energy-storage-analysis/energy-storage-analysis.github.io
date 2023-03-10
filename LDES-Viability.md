---
layout: default
title: A Technoeconomic Survey of Long-Duration Energy Storage Viability 
use_math: true
---

# {{ page.title }}

This page hosts some preliminary interactive visualizations of the data collected of the material cost floor for the energy capital cost ($USD/kWh$) for different energy types suitable for long duration energy storage. 

# Materials energy capital cost ($C_{kWh,mat}$) dataset

The cost of the material that the storage medium is built out of sets a lower bound on the achievable $C_{kWh}$. Therefore we meed to find a storage medium with a **material energy capital cost $(C_{kWh, mat})$** than approximately $10\ USD/kWh$.  $C_{kWh, mat}$ is calculated from the energy density, $\rho_E$ [kWh/kg], of the storage media (storing a given form of energy) and the material price, $C_{mat}$  [USD/kg], of the materials used in the storage media through the equation 


$$
C_{kWh, mat} = \frac{C_{mat} [USD/kg]}{\rho_E [kWh/kg]}
$$


Below is a plot that shows calculated $C_{kWh, mat}$ for a wide range of storage media.  Mouse over to see the name of the material. 

<div>
<center>
  <embed type="text/html" src="LDES-Viability/Ckwh_bokeh.html" style="width:100%" height=800> 
</center>
</div>

The plot below breaks out each storage medium into the material cost and energy density used to calculate $C_{kWh, mat}$ above. Click on a storage medium type in the legend to hide that class of storage medium. The line indicates  $C_{kWh, mat} = 10\ USD/kWh$

<div>
<center>
  <embed type="text/html" src="LDES-Viability/Ckwh_line_bokeh.html" style="width:100%" height=800> 
</center>
</div>
