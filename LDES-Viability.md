---
layout: default
title: A Technoeconomic Survey of Long-Duration Energy Storage Viability 
use_math: true
---

# {{ page.title }}

This page hosts a brief outline of our recent article "A Technoeconomic Survey of Long-Duration Energy Storage Viability" (link added upon publication) along with interactive visualizations related to the work. 

# Motivating the Energy Capital Cost ($C_{kWh}$) as a Long Duration Energy Storage Figure of Merit

A key metric for energy storage systems is levelized cost of storage (**LCOS**) which can be defined as the extra price that must be charged when selling electricity, in addition to the price of charging paid by the system operator, to make the energy storage system economically viable over its lifetime. With some simplifying assumptions we can derive an expression of the LCOS:

$$
LCOS = \frac{1}{CF*LT_{eff,h}}\left\lbrack \frac{C_{kWh}}{\eta_{d\ }}*DD\  + C_{kW} \right\rbrack + P_{chg}\left( \frac{1}{\eta_{RT}} - 1 \right)
$$

<div markdown = "0">
<button type="button" class="collapsible">Open for term definitions and  derivation of LCOS equation </button>
  <div class="extended" style="display:none">

    {% include_relative LDES-Viability/lcos.md %}

  </div>
</div>


The critical feature of the LCOS is that for sufficiently long duration the last term will begin to dominate the expression and the LCOS can be approximated 

$$
LCOS \approx \frac{C_{kWh}}{CF*LT_{eff,h}*\eta_{d}} * DD
$$

The scaling factor with duration represents the key figure of merit for long duration energy storage systems. In this expression the component that will be able to vary over many orders of magnitude is $C_{kWh}$ and is what we chose to focus on in this study. The effect of  $C_{kWh}$, as well as the other parameters on the LCOS can be explored in the plot below.


<div>
<center>
  <embed type="text/html" src="LDES-Viability/lcos_duration.html" width=1200 height=410> 
</center>
</div>

# Materials energy capital cost ($C_{kWh,mat}$) dataset

The cost of the material that the storage medium (SM) is built out of sets a lower bound on the achievable $C_{kWh}$. This **material energy capital cost $(C_{kWh, mat})$** is calculated from the energy density, $\rho_E$ [kWh/kg], of the SM (storing a given form of energy) and the material price, $C_{mat}$  [USD/kg], of the materials used in the SM through the equation 


$$
C_{kWh, mat} = \frac{C_{mat} [USD/kg]}{\rho_E [kWh/kg]}
$$


We have acquired material cost and energy density data to calculate $(C_{kWh, mat})$ for a wide range of SM. The plot below shows this data grouped by type of storage media technology and colored by the form of energy. Mouse over to see the name of the material. 

<div>
<center>
  <embed type="text/html" src="LDES-Viability/Ckwh_bokeh.html" style="width:100%" height=800> 
</center>
</div>

The plot below breaks out each SM into the material cost and energy density used to calculate $C_{kWh, mat}$ above. Click on a SM type in the legend to hide that class of SM. The line indicates  $C_{kWh, mat} = 10\ USD/kWh$ which we have determined in our paper as a rough cutoff of viability for economically providing 100 hours of discharge duration. 

<div>
<center>
  <embed type="text/html" src="LDES-Viability/Ckwh_line_bokeh.html" style="width:100%" height=800> 
</center>
</div>

<div markdown = "0">
{% include collapsible.html %}
</div>