---
title: "Payload Delivery Plane (Col. Pollo J. Rosso) "
date: 2025-06-15
collection: portfolio
tags: [CAD, Python, MATLAB]
header:
  teaser: delivery_plane/DSC_0420.jpg

attachments:
 - title: "Preliminary Design Review (FDR)"
   pdf: /files/docs/payload_delivery/PDR_MJ5.pdf
   pptx: /files/docs/payload_delivery/PDR_Presentation.pptx
 - title: "Final Design Review (FDR)" 
   pdf: /files/docs/payload_delivery/FDR_MJ5.pdf
   pptx: /files/docs/payload_delivery/FDR_Presentation.pptx
 - title: "Senior Day Poster"
   pdf: /files/docs/payload_delivery/Team_3_MJ5_Poster_colored_fixedlogo.pdf   

 
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

<div class="concept">

  <!-- Design objective -->
  <div class="concept__sub">
    <p class="subhead">Design objective &amp; score</p>
    <p>Maximize flight score based on payload revenue, energy &amp; operating costs, and time:</p>

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
    </div>

    - Fixed parameters used: $r_{W_p}=1,\ r_{V_p}=300,\ c_e=0.3,\ c_c=0.5,\ c_{W_g}=300,\ c_f=0.2,\ t_l=1000$.
  </div>

  <!-- Key assumptions -->
  <div class="concept__sub">
    <p class="subhead">Key assumptions &amp; early sizing.</p>

    <ul class="assumptions">
      <li>Glide ratio:
        <div class="assumption-value">$L/D \approx 8{-}13$</div>
      </li>

      <li>Electric battery specific energy:
        <div class="assumption-value">$4.53\times10^{5}\ \mathrm{J/kg}$</div>
        <div class="assumption-note">(from $11.1\,\mathrm{V},\ 1.8\,\mathrm{Ah},\ 0.1588\,\mathrm{kg}$)</div>
      </li>

      <li>Initial gross weight target:
        <div class="assumption-value">$\approx 2\ \mathrm{kg}$</div>
        <div class="assumption-note">Wing loading: $\approx 2.05\ \mathrm{lb/ft}^2$</div>
      </li>

      <li>Competition constraints:
        <div class="assumption-value">$W_p \ge 0.5\ \mathrm{lb},\quad V_p \ge 500\ \mathrm{cm}^3$</div>
      </li>

      <li>Working goals:
        <div class="assumption-value">$W_p = 1.5\ \mathrm{lb},\quad V_p = 0.5\ \mathrm{L}$ (min)</div>
      </li>
    </ul>
  </div>

  <!-- Architecture -->
  <div class="concept__sub">
    <p class="subhead">Architecture &amp; materials.</p>
    <ul>
      <li>High-wing with dihedral for stability; simple planform for manufacturability.</li>
      <li>Structure: balsa wing, plywood fuselage; control surfaces from dense foam.</li>
      <li>5-servo layout: 2× aileron, 1× elevator, 1× rudder/nose-wheel, 1× drop mechanism.</li>
      <li>Weight payload near CG; volume payload released via single 9 g servo.</li>
    </ul>
  </div>

  <!-- Scoring insights -->
  <div class="concept__sub">
    <p class="subhead">Scoring strategy insights.</p>
    <ul>
      <li>Energy cost per mission is small (≈ $0.12$), so <strong>reducing flight time</strong> (higher cruise speed) boosts score materially.</li>
      <li>Adequate wing loading for low takeoff/landing speeds; empty-weight fraction target $0.5\text{–}0.7$.</li>
    </ul>
  </div>

  <!-- Electronics -->
  <div class="concept__sub">
    <p class="subhead">Fixed electronics &amp; selected components.</p>
    <ul>
      <li>Cobra C-2217/16 (Kv 1180) motor, 40 A ESC, 3S 1800 mAh LiPo, FrSky X8R, SG90 servos, standard linkages &amp; hardware.</li>
    </ul>
  </div>

</div>

### Preliminary Design

<div class="concept">

  <!-- Propulsion -->
  <div class="concept__sub">
    <p class="subhead">Propulsion &amp; propeller choice.</p>
    <ul>
      <li>Motor constraint: Cobra C2217/16, 11.1 V, Kv = 1180 → no-load speed ≈ <strong>13,098 RPM</strong>; usable band <strong>6,500–10,500 RPM</strong>.</li>
      <li>APC <strong>8×6-E</strong> vs <strong>9×6-E</strong>: the 8×6-E is slightly more efficient, but cruise thrust needed ≈ <strong>3 N</strong>.
        At <strong>9,000 RPM</strong> the <strong>9×6-E</strong> makes ≈ <strong>3.75 N</strong> while the 8×6-E makes ≈ <strong>2.66 N</strong>.</li>
      <li><strong>Selected propeller: APC 9×6-E</strong> (meets cruise-thrust with margin at realistic RPM).</li>
    </ul>
  </div>

  <!-- Airfoil -->
  <div class="concept__sub">
    <p class="subhead">Airfoil &amp; aerodynamic model.</p>
    <ul>
      <li>Analysis at $Re \approx 5\times10^{5}$; constraints: $t/c \le 12\%$ (servo fit), camber $\le 6\%$ (manufacturability/stability).</li>
      <li>Candidates: Clark-Y, NACA 4415/0012/4412/2412 → <strong>NACA 4412</strong> chosen for higher L/D in the operating range.</li>
      <li>2-D refs: $C_{L,\max}\approx1.52$, $C_{d,\min}\approx0.007$, $C_m\approx-0.10$ at low $\alpha$.</li>
      <li>3-D correction gives $C_{L,\max}\approx1.36$ at $\alpha\approx13.25^\circ$ (spanwise correction from assignment method).</li>
    </ul>
  </div>

  <!-- Performance -->
  <div class="concept__sub">
    <p class="subhead">Performance estimates (Initial).</p>
    <ul>
      <li>Takeoff model ($\mu_\text{roll}=0.03$): ground run $S_G \approx \,18\ \text{m}$; stall speed $V_\text{stall}\approx11\ \text{m/s}$.</li>
      <li>Thrust-required vs. cruise speed: thrust at nominal cruise ≈ <strong>3 N</strong>; available thrust ~<strong>10 N</strong> → $V_{\max}\approx45\ \text{m/s}$.</li>
      <li>Wing-loading carpet: optimum around <strong>100 N/m²</strong> for the sizing assumptions used.</li>
    </ul>
  </div>

  <!-- Geometry -->
  <div class="concept__sub">
    <p class="subhead">Baseline geometry (working values).</p>
    <ul>
      <li>Wing area $S\approx0.23\ \text{m}^2$, span $b\approx1.15\ \text{m}$, chord $c\approx0.20\ \text{m}$ (basis for Re &amp; perf calcs).</li>
    </ul>
  </div>

  <!-- Rationale -->
  <div class="concept__sub">
    <p class="subhead">Rationale.</p>
    <p class="mb-0">
      The prop choice prioritizes meeting cruise-thrust with margin in the 50–80 % RPM band,
      while NACA 4412 offers strong L/D and gentle stall at your Reynolds number—both consistent
      with minimizing flight time while keeping takeoff distance short.
    </p>
  </div>


</div>

### Detail Design & Fabrication

<div class="concept">

  <div class="concept__sub">
    <p class="subhead">Payload architecture</p>
    <ul>
      <li><strong>Payload 1 (weights):</strong> plywood mount with removable slides; velcro retention; calibrated up to competition max</li>
      <li><strong>Payload 2 (volume):</strong> 3D-printed bomb-bay with dual micro-servos and a <em>four-bar linkage</em> for ~90° door opening</li>
      <li>Return springs preload doors to closed; linkage geometry biased to self-lock near closed to reduce idle servo load</li>
    </ul>
<h3 id="bay-door-design">Bay Door Design</h3>

<figure>
  <!-- Static CAD image -->
  <img src="/images/delivery_plane/Delivery_Assembly_CAD.jpg"
       alt="Bomb-bay four-bar linkage CAD">

  <!-- Animated GIF (scaled down with CSS or width attribute) -->
  <img src="/images/delivery_plane/fourbar_animation.gif"
       alt="Four-bar linkage animation showing door motion"
       class="media-img small-gif">

  <!-- Video 1 -->
  <video autoplay muted loop playsinline class="media-video">
    <source src="/videos/delivery_plane/20250521_174541.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <figcaption>
    Four-bar door geometry—quick open at small servo rotation, stable closure at neutral.
  </figcaption>
</figure>
  </div>

  <div class="concept__sub">
    <p class="subhead">Airframe &amp; controls</p>
    <ul>
      <li><strong>Wing:</strong> balsa ribs with ply center section; semi-monocoque leading edge; 3° dihedral</li>
      <li><strong>Ailerons:</strong> span ~40% of wing, chord ~20% of local; ±30° travel</li>
      <li><strong>Fuselage:</strong> 2 mm ply primary structure; wing hooks + carbon tubes with rubber-band retention</li>
      <li><strong>Empennage:</strong> foam-core V-stab with CF spar + balsa/monokote; balsa H-stab</li>
      <li><strong>Taildragger gear:</strong> main gear bent for higher rotation; tailwheel on 3D-printed pivot aligned to rudder hinge (single-servo steering)</li>
      <li><strong>Pushrods:</strong> routed in plastic guide tubes to prevent interference and reduce column buckling</li>
    </ul>
  </div>

  <div class="concept__sub">
    <p class="subhead">Propulsion &amp; alignment</p>
    <ul>
      <li>3D-printed thrust-line shim: **~+2° right, ~+3° down**; plywood standoff shifts motor ~15 mm forward for CG</li>
      <li>Avionics bay: Cobra C-2217/16, 40 A ESC, inline watt-meter, 3S 1800 mAh LiPo, FrSky X8R</li>
    </ul>
    <div class="inline-figs">
      <img src="/images/delivery_plane/motor_extension_and_shim.jpg" alt="Motor thrust-line shim">
    </div>
    <figcaption>
    Angled motor mount shim and motor extension 
    </figcaption>
  </div>

  <div class="concept__sub">
    <p class="subhead">Fabrication notes</p>
    <ul>
      <li>Printed parts: nose cone, spinner, thrust-line shim, tailwheel pivot, bomb-bay frame/doors</li>
      <li>Covering: monokote on wing/empennage; quick field repairable</li>
      <li>Assembly tips:
        <ul>
          <li>Dry-fit bomb-bay module and doors before covering to verify clearances</li>
          <li>Tune horn radius/link length to avoid end-point binding at ±30° throws</li>
          <li>Set spring preload so doors close without holding torque</li>
        </ul>
      </li>
    </ul>
  </div>

  <div class="concept__sub">
    <p class="subhead">Specs (as-flown)</p>
    <table class="params">
      <thead><tr><th>Item</th><th>Value</th></tr></thead>
      <tbody>
        <tr><td>Empty / Gross</td><td>~1.4 kg / ~2.125 kg</td></tr>
        <tr><td>Payload 1 (weights)</td><td>~0.68 kg</td></tr>
        <tr><td>Payload 2 (volume)</td><td>~700 cm³</td></tr>
        <tr><td>Thrust-to-weight</td><td>~0.5</td></tr>
        <tr><td>Cruise speed</td><td>~20 m/s</td></tr>
        <tr><td>CG (empty / P1+P2)</td><td>~24.7% / ~24.0% MAC</td></tr>
        <tr><td>Neutral point / SM</td><td>~58% MAC / ~17%</td></tr>
        <tr><td>Stall / Takeoff / Climb</td><td>~10–11 m/s / ~15 m / ~15°</td></tr>
        <tr><td>Airfoils</td><td>NACA 4412 (wing), NACA 0012 (empennage)</td></tr>
      </tbody>
    </table>
  </div>

  <div class="concept__sub">
    <p class="subhead">Test Flight &amp; Results</p>
    <ul>
      <li>Nose cone was removed due to imbalance caused</li>
      <li>Initial flight test revealed that the tail was to heavy and moved Center of Gravity from the ideal 25-33% of chord to 60% of the chord</li>
      <li>Payload Delivery system was unable to be tested during initial test flight due to servo mount failure</li>
      <li>Motor vibrations caused mounting hardware to back out, causing the motor to fall out of the aircraft. Luckily this happened during landing and pilot was able to glide for safe landing.</li>
      <li>Rubber-band wing retention works great with properly backed hooks and CF tubes</li>
    </ul>
  </div>

  <div class="concept__sub">
    <p class="subhead">Lessons learned</p>
    <ul>
      <li>Rebuild tail assembly to be lighter weight. Done by changing from foam elevators and rudder to balsa wood semi-monocoque</li>
      <li>Extended motor further out from fusealage to help counter the tail weight. Mount extension also had space for more weight to be added to assist further</li>
      <li>Motor mounting hardware was secured utilizing LOCTITE threadlocker</li>
      <li>Delivery system mount was rebuilt with updated mounts that were stronger and less prone to breakage</li>

    </ul>
  </div>

</div>

## Reports and Presentations
{% if page.attachments and page.attachments.size > 0 %}
<div class="doc-grid">
{% for d in page.attachments %}
  <div class="doc-card">
    <h4>{{ d.title }}</h4>
  
    <p class="doc-actions">
      {% if d.pdf %}
        <a class="btn doc-btn"
           href="{{ d.pdf | relative_url }}"
           target="_blank" rel="noopener">View PDF</a>
      {% endif %}

       {% if d.pptx %}
        <a class="btn doc-btn"
          href="{{ d.pptx | relative_url }}"
          target="_blank" rel="noopener">Download PPTX</a>
        {% if jekyll.environment == "production" %}
          <a class="btn doc-btn"
            href="https://view.officeapps.live.com/op/view.aspx?src={{ d.pptx | absolute_url | uri_escape }}"
            target="_blank" rel="noopener">Open PPTX Online</a>
        {% endif %}
      {% endif %}
  </p>
  </div>
{% endfor %}
</div>
{% else %}
<p><em>No documents uploaded yet.</em></p>
{% endif %}


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