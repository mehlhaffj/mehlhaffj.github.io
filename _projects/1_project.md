---
layout: page
title: black hole accretion disk coronae
description: how magnetic reconnection powers flaring and throttles jet production
img: assets/img/kinetic_corona_zoomed.png
importance: 1
category: by theme
related_publications: true
---

<h2>
What is a black hole accretion disk corona?
</h2>
Originally, the accretion disk coronae were proposed to explain the hard X-ray emission, in excess of 10 keV, coming from black hole X-ray binaries. A classic geometrically thin accretion disk (e.g., Shakura & Sunyaev 1973) would never be hot enough to produce X-rays beyond a keV or so. Thus, another emitting plasma region, beyond the surface of the disk itself, was needed to explain the observations. This hot, dilute, X-ray-bright plasma region was called a corona in analogy with the hot, dilute, X-ray emitting plasma surrounding the Sun.
<div class="row align-items-center">
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/solar_corona.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            An image of the Sun's corona from the Solar Dynamics Observatory. Technically, this image is in the ultraviolet band (not the X-rays).
        </div>
    </div>
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/galeev_rosner_viana_1979.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            A drawing of an accretion disk corona, as imagined early on by Galeev, Rosner, and Viana (1979).
        </div>
    </div>
</div>

<h2>
Coronal X-ray emission is tied to jet activity
</h2>
<div class="row align-items-center">
    <div class="col-sm mt-0">
        <p>
            The X-ray emission from the accretion disk and corona is known to go through a series of states, diagrammed here. First, a hard state where the high-energy (>10 keV or so) X-rays dominate; next a luminous/flaring transition to a soft state where the low-energy (~1 keV) X-rays dominate; and a fading followed by a return to the hard state. 
        </p>
        <p>
            <strong>These X-ray states coincide with observed jet activity.</strong> In the hard state, a steady, relatively slow jet is observed. In the soft state, the jet is quenched. During the flaring transition between the two, a "jet line" is crossed, across which the jet sputters, launching discrete, rapidly moving ejecta.
        </p>
    </div>
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/xray_jet_connection.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            A drawing of an accretion disk corona, as imagined early on by Galeev, Rosner, and Viana (1979).
        </div>
    </div>
</div>

<h2>
Could reconnection link the corona and jet behavior?
</h2>
Given the considerable energy stored in the magnetic fields threading the corona, it has long been thought that <a href="https://en.wikipedia.org/wiki/Magnetic_reconnection">magnetic reconnection</a> (see also my [black hole jets](/projects/2_project/) page) might power the coronal X-ray emission -- much like in the solar corona. Could the same reconnection process powering the X-rays also be governing the jet's behavior? This question motivated a lot of my work on black hole accretion disk coronae.

<h3>
What I did
</h3>
<div class="row align-items-center">
    <div class="col-sm mt-0">
        <p>
            I designed a of a black hole accretion disk corona based on kinetic plasma physics {% cite mehlhaff_etal_2025b %}. To do this, I modified and used the <span style="font-family: 'Courier New', Courier, monospace;"><a href="https://ui.adsabs.harvard.edu/abs/2019PhRvL.122c5101P/abstract">GRZELTRON</a></span> particle-in-cell code, a general relativistic extension of the <span style="font-family: 'Courier New', Courier, monospace;"><a href="https://ui.adsabs.harvard.edu/abs/2019ascl.soft11012C/abstract">ZELTRON</a></span> code. A snapshot from the resulting simulations is shown here.
        </p>
    </div>
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/labeled_jet.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Spatial snapshot of local plasma temperature from a particle-in-cell simulation of a black hole accretion disk corona. Solid and dashed black lines are magnetic field lines. Reconnection layers accelerate particles, yielding red-hot regions which, in turn, produce X-ray emission.
        </div>
    </div>
</div>

<h3>
What I found
</h3>
The simulations show that the most intense site of reconnection is actually along the jet wall. Thus, as reconnection powers the X-ray output of the corona, it also preys on the energy being pumped into the jet. This could explain correlated X-ray flaring and jet ejections witnessed during hard-to-soft X-ray state transitions. Vigorous reconnection events close up the jet nozzle, causing it to sputter, giving rise to the observed discrete, rapidly propagating ejecta.

<h2>
Conclusions
</h2>
Reconnection has long been recognized as an efficient mechanism for dissipating energy. However, in the context of highly magnetized accretion disk coronae, magnetic field lines transport electrical current, energy, and angular momentum. By changing the connectivity of field lines, magnetic reconnection doesn't just dissipate energy; it modifies global structure and changes the transport of important conserved quantities.

This study illustrates a case in point. Here, reconnection closes off the magnetic field lines forming the jet funnel, quenching the release of energy into a powerful jetted outflow. In the future, I hope to explore other systems where reconnection plays important roles not just in generating observable signatures, but also in regulating large-scale properties of its host system.
