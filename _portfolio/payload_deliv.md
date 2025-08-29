---
title: "Payload Delivery Plane (Col. Pollo J. Rosso) "
date: 2025-06-15
collection: portfolio
tags: [CAD, Python, MATLAB]
header:
  teaser: delivery_plane/DSC_0420.jpg
---
## Overview
This was my senior design project, where I worked with a team of 5 other aerospace engineering seniors. Our task was to design from the ground up a radio controlled plane, that could carry two separate payloads. One a weight based payload and the other volume based. Where the volume based payload would then be dropped while in flight. 

<div class="lead-photo">
  <figure>
    <img src="/images/delivery_plane/IMG_0004.JPG">
    <figcaption>UCSD MAE 155B team MJ<sup>5</sup>— Spring 2025</figcaption>
  </figure>
</div>



## Design Constraints and Competition Rules
- Design, build, and successfully fly an aircraft that results in the highest possible flight score utilizing the given flight score
- Aircraft must be electrically powered
- Package 1 must be lead weights, minimum weight of 0.5 lb
- Package 2 must be an empty cardboard box, minimum volume of 500 cm<sup>3</sup>
- Package 2 must be deployed while in air
- Must have a successful empty weight flight 
- Before first flight aircraft needs to be approved and safe for flight



## Component Restrictions 
- Motor: Cobra C-2217 Brushless Kv=1180
- Speed Controller: Flite Test 40 Amp ESC
- Battery: Tattu 11.1V 1800mAh 3S 45C LiPo
- Receiver: FrSky Taranis Receiver X8R 8 Channel 2.4 GHz

## Objective (Flight Score)

<div class="eq-box">
  <div class="eq">
\[
J(x) =
\frac{ r_{W_p}\, W_p(x) + r_{V_p}\, V_p(x) - c_e\, E_f(x) - c_c }{ T_f(x) }
\;-\;
\frac{ c_{W_g}\, W_g(x) }{ t_l }
\;-\; c_f
\]
  </div>

  <div>
<h4 class="subtle">Symbols &amp; Definitions</h4>
<table class="params">
  <thead>
    <tr>
      <th>Symbol</th>
      <th>Definition</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>\(x\)</td><td>aircraft design (decision variables)</td></tr>
    <tr><td>\(W_p(x)\)</td><td>package-1 weight</td></tr>
    <tr><td>\(V_p(x)\)</td><td>package-2 volume</td></tr>
    <tr><td>\(E_f(x)\)</td><td>energy consumption</td></tr>
    <tr><td>\(W_g(x)\)</td><td>gross weight</td></tr>
    <tr><td>\(T_f(x)\)</td><td>flight time</td></tr>
    <tr><td>\(r_{W_p},\, r_{V_p}\)</td><td>revenue per unit weight / volume</td></tr>
    <tr><td>\(c_e\)</td><td>cost per unit energy</td></tr>
    <tr><td>\(c_c\)</td><td>cost per flight</td></tr>
    <tr><td>\(c_{W_g}\)</td><td>cost per unit gross weight</td></tr>
    <tr><td>\(c_f\)</td><td>fixed operating cost</td></tr>
    <tr><td>\(t_l\)</td><td>total aircraft-life flight time</td></tr>
  </tbody>
</table>

  <h4 class="subtle">Nominal values & units</h4>
  <table class="params">
    <thead>
      <tr>
        <th>Quantity</th><th>Symbol</th><th>Value</th><th>Units</th>
        <th>SI value</th><th>SI units</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Revenue per unit payload weight</td><td>\(r_{W_p}\)</td><td>1</td><td>\([\$/\mathrm{lb}]\)</td><td>\(2.25\times10^{-1}\)</td><td>\([\$/\mathrm{N}]\)</td></tr>
      <tr><td>Revenue per unit payload volume</td><td>\(r_{V_p}\)</td><td>300</td><td>\([\$/\mathrm{m}^3]\)</td><td>\(3.00\times10^{2}\)</td><td>\([\$/\mathrm{m}^3]\)</td></tr>
      <tr><td>Cost per unit energy</td><td>\(c_e\)</td><td>0.3</td><td>\([\$/\mathrm{kWh}]\)</td><td>\(8.33\times10^{-8}\)</td><td>\([\$/\mathrm{J}]\)</td></tr>
      <tr><td>Cost per flight (COC)</td><td>\(c_c\)</td><td>0.5</td><td>\([\$]\)</td><td>0.5</td><td>\([\$]\)</td></tr>
      <tr><td>Cost per unit gross weight</td><td>\(c_{W_g}\)</td><td>300</td><td>\([\$/\mathrm{lb}]\)</td><td>\(6.74\times10^{1}\)</td><td>\([\$/\mathrm{N}]\)</td></tr>
      <tr><td>Cost per unit flight-time (FOC)</td><td>\(c_f\)</td><td>0.2</td><td>\([\$/\mathrm{h}]\)</td><td>\(5.56\times10^{-5}\)</td><td>\([\$/\mathrm{s}]\)</td></tr>
      <tr><td>Total flight time in aircraft life</td><td>\(t_l\)</td><td>1000</td><td>\([\mathrm{h}]\)</td><td>\(3.60\times10^{6}\)</td><td>\([\mathrm{s}]\)</td></tr>
    </tbody>
  </table>
  </div>
</div>


## Development

### Conceptual Design

### Preliminary Design

### Detail Design & Fabrication

## Gallery

### Flight Videos
#### Light Payload and Successful Package Drop
<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/oGGQHPh8Jqk?autoplay=1&mute=1&loop=1&playlist=oGGQHPh8Jqk"
    title="Light payload and successful package drop"
    frameborder="0"
    allow="autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
### Images