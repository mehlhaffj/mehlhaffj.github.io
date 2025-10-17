---
layout: page
title: black hole jets 
description: their energy dissipation, composition, and appearance 
img: assets/img/cygnusa.jpg
importance: 2
category: by theme
related_publications: true
---

<h2>
Two of many unsolved mysteries surrounding black hole jets
</h2>
<ol>
<li>How they shine</li>
<li>What they are made of</li>
</ol>

<h2>
How I think about these questions
</h2>

<div class="row align-items-center">
    <div class="col-md mt-3 mt-md-0">
        <p>
            The light we observe from black hole jets comes from a chain of processes that might be diagrammed as in <span class="d-inline d-sm-none">the</span><span class="d-none d-sm-inline">this</span> sketch <span class="d-inline d-sm-none">below</span>.
        </p>
        <p>
            First the jet is launched. Then it propagates for some distance. Eventually, something -- like an instability -- triggers a dissipative plasma process. This process expends energy locally in the jet, using it to accelerate particles to highly relativistic energies. The energized particles are what produce the light that we observe.
        </p>
    </div>
    <div class="col-md mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jet_schematic.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            The main sequence of events that results in jets being observed.
        </div>
    </div>
</div>

A crucial step in this sequence is the dissipation, since it is responsible for the particle acceleration and ultimate radiation. Furthermore, because black hole jets are often very efficient gamma-ray sources, some of the photons produced at dissipation sites might get absorbed within the jet to produce electron-positron pairs. In this sense, the dissipation step links together the mysteries of jet composition and radiation: they may go hand-in-hand. These remarks highlight the importance of understanding:

<h2>
What plasma process governs dissipation in the jet?
</h2>

A lot of my research on black hole jets concerns looking at different potential answers to this question. I have considered two possibilities: magnetic reconnection and magnetized turbulence. Below are some highlights from my studies of each scenario.

<h3>
Scenario 1: Magnetic reconnection
</h3>
<div class="row align-items-center">
    <div class="col-sm">
        <p>
            <a href="https://en.wikipedia.org/wiki/Magnetic_reconnection">Magnetic reconnection</a> is a basic plasma physics process that is very efficient at liberating magnetic energy in plasmas. It does this by rearranging the magnetic field from a stressed, high-energy configuration to a more relaxed, lower-energy one (see cartoon). The difference in magnetic energy between the two states is given to the plasma. Since jets are thought to contain a lot of magnetic energy, reconnection might be one way that jets dissipate.
        <br>
        <br>
        </p>
    </div>
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/reconnection.gif" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            A <a href="https://en.wikipedia.org/wiki/Magnetic_reconnection">Wikipedia cartoon</a> of a reconnection event. The initially horizontal magnetic field switches direction across a current sheet (grey X's). The field lines reconnect with each other at the center point and release energy. 
        </div>
    </div>
</div>

<h4>
A regime with radiative feedback from pair production
</h4>
<div class="row align-items-center">
    <div class="col-sm mt-3 mt-md-0">
        <p>
            The channeling of magnetic energy into the motion of relativistic particles and gamma-ray radiation is a bit complicated in many black hole jets. This is due to a radiative feedback mechanism sketched <span class="d-inline d-sm-none">below</span><span class="d-none d-sm-inline">here</span>.
        </p>
        <p>
            The reconnecting current sheet accelerates particles that produce gamma-ray photons (step 1 in the sketch). These photons propagate upstream into the plasma fueling reconnection (step 2) where they produce new electron-positron pairs (step 3). This weighs down the plasma fed into the reconnection zone (step 4), dampening subsequent particle acceleration and photon emission, thereby closing the feedback loop.
        </p>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/knpp_schematic.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            How gamma-ray radiation and pair production can feed back on reconnection in black hole jets {% cite mehlhaff_etal_2021 %}.
        </div>
    </div>
</div>

<h4>
What I did
</h4>
To characterize magnetic reconnection in the presence of this radiative feedback, I first performed an analytic study {% cite mehlhaff_etal_2021 %} where I scoped out the parameter space and laid out a basic framework for understanding the regime. Fully characterizing it, though, required a follow-up numerical study {% cite mehlhaff_etal_2024 %}. To power this study, I outfitted the <span style="font-family: 'Courier New', Courier, monospace;"><a href="https://ui.adsabs.harvard.edu/abs/2019ascl.soft11012C/abstract">ZELTRON</a></span> particle-in-cell code to self-consistently account for the relevant gamma-ray transport and pair production. An example simulation is illustrated below.
<div class="row align-items-center">
    <div class="col-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/knreconn.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
        A snapshot from a simulation of magnetic reconnection with gamma-ray emission and pair production {% cite mehlhaff_etal_2024 %}. Left: Number density of particles initially placed by hand into the simulation. Middle: Energy density of gamma-rays built up as the result of particle acceleration. Right: Number density of pairs born <em>in situ</em>.
    </div>
</div>


<h4>
What I found
</h4>
The coupling of reconnection to gamma-ray radiation and pair production has pronounced effects on the **radiation spectrum** observed from the jet and on the **ambient plasma**. 

<ul>
<li><strong>Effect on observable radiation</strong></li>
The liberated part of the energy that is pumped into the most energetic particles -- those that radiate photons almost exclusively above pair-production -- cannot be directly observed. Instead, it is absorbed inside the plasma to produce new pairs. Thus, the energy originally emitted at the highest photon energies is reprocessed until it can be carried away by photons below pair-production threshold. As a result, the observable part of the gamma-ray spectrum is remarkably stable. Instead of exhibiting a harder-when-brighter trend, it becomes a power-law with a spectral slope nearly independent of gamma-ray luminosity. What is compelling about this result is that it reflects rather well <em>Fermi</em> observations of flat-spectrum radio quasars. 

<li><strong>Effect on ambient plasma composition</strong></li>
Pair production loads the plasma with new electron positron pairs. For an initial plasma magnetization surpassing a certain threshold, reconnection might pump copious pairs into the jet, substantially changing its composition <em>in situ</em>.
</ul>

<h3>
Scenario 2: Magnetized turbulence 
</h3>
In addition to forming and dissipating large-scale reconnection layers, black hole jets may also become turbulent. If turbulence occurs, it will couple to the same radiative physics and pair production as reconnection would in its place. 

<h4>
What I did
</h4>
<div class="row align-items-center">
    <div class="col-sm mt-3 mt-md-0">
        <p>
I used the code developed for my previous reconnection work {% cite mehlhaff_etal_2024 %} to perform a novel numerical study of turbulence {% cite mehlhaff_etal_2025a %} coupled to radiation and pair production. A snapshot from one of the simulations is shown <span class="d-inline d-sm-none">below</span><span class="d-none d-sm-inline">at the right</span>.
        </p>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/knpp_turb.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Snapshot from a turbulence simulation with gamma-ray radiation and pair production {% cite mehlhaff_etal_2025a %}.
        </div>
    </div>
</div>

<h4>
What I found
</h4>
As in the case of reconnection, feedback from pair production dictates the main features of magnetized turbulence. Initially, turbulent particle acceleration outpaces radiative cooling, leading to a burst of nonthermally distributed energetic particles and, as a result, gamma-ray radiation and pair production. Subsequently, newborn pairs accumulate and weigh down the plasma, slowing particle acceleration down. By producing its own plasma, turbulence self-regulates its particle acceleration rate, eventually bringing it into balance with radiative cooling. 

Because the final equilibrium is so simple, we were able to find an analytic formula for the number of pairs produced as the plasma approaches its terminal state. This allowed us to predict the turbulent pair yield for plasma conditions expected in jets from flat-spectrum radio quasars. According to our predictions, turbulence could substantially increase the pair count in these systems <em>in situ</em>.

We were also able to determine the radiation spectrum produced in the final equilibrium state. It is thermal with a very predictable characteristic photon energy. However, we are unsure how observable this spectrum would be since, once turbulence subsides, it would fade away. The change in the pair content of the jet, however, would be permanently imprinted in the downstream plasma.

<h2>
Conclusions
</h2>
Whether through reconnection or turbulence, dissipation in black hole jets may be intimately linked to their material composition. Maybe we will one day even be able to infer the pair content of such jets from their gamma-ray signatures. It is also possible that we may eventually be able to firmly distinguish which particle acceleration mechanism is at work: already reconnection seems to produce a universal power-law spectrum; turbulence, once equilibrated, produces a thermal spectrum. More work needs to be done to link global jet structure to dissipation in order to situate these models in a more cohesive global context.
