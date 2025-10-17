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
    <div class="col-md mt-0">
        <p>
            The light we observe from black hole jets comes from a chain of processes that might be diagrammed as in this sketch.
        </p>
        <p>
            First the jet is launched. It then propagates some distance before something -- like an intrinsic instability in the jet plasma -- triggers a dissipative plasma process. This plasma process expends energy locally in the jet, using it to accelerate particles to highly relativistic energies. The energized particles are what produce the light that we observe.
        </p>
    </div>
    <div class="col-md mt-0">
        {% include figure.liquid loading="eager" path="assets/img/jet_schematic.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            The main sequence of events that results in jets being observed.
        </div>
    </div>
</div>

A crucial step in this sequence is the dissipation, particle acceleration and radiation. Also, because black hole jets are often very efficient gamma-ray sources, it may be that some of the emitted photons get absorbed within the jet to produce fresh plasma in the form of electron-positron pairs. In this sense, the dissipation step links together the mysteries of jet composition and radiation: they may go hand-in-hand. These observations beg the question:

<h2>
What plasma process governs jet energy dissipation?
</h2>

A lot of my research on black hole jets concerns looking at different potential answers to this question. I have considered two possibilities: magnetic reconnection and magnetized turbulence. Here's what I've done and learned in each case

<h3>
Scenario 1: Magnetic reconnection
</h3>
<div class="row align-items-center">
    <div class="col-sm">
        <p>
            <a href="https://en.wikipedia.org/wiki/Magnetic_reconnection">Magnetic reconnection</a> is a basic plasma physics process that is very efficient at liberating magnetic energy. It does this by rearranging the magnetic field threading a plasma from a stressed, high-energy configuration to a more relaxed, lower-energy one (see cartoon). The difference in magnetic energy is given to the plasma. Since jets are thought to contain a lot of magnetic energy, reconnection might be one way that jets dissipate.
        <br>
        <br>
        </p>
    </div>
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/reconnection.gif" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            A <a href="https://en.wikipedia.org/wiki/Magnetic_reconnection">Wikipedia cartoon</a> of a reconnection event. A large-scale horizontal magnetic field switches direction across a current sheet (grey X's). The field lines flow inward, reconnecting with each other at the center point and releasing energy. 
        </div>
    </div>
</div>

<h4>
A regime with radiative feedback from pair production
</h4>
<div class="row align-items-center">
    <div class="col-sm mt-0">
        <p>
            The channeling of magnetic energy through reconnection into the motion of relativistic particles and gamma-ray radiation is a bit complicated. This is due to a feedback mechanism sketched here.
        </p>
        <p>
            The reconnecting current sheet accelerates particles that produce gamma-ray photons (step 1). These photons propagate into the upstream plasma fueling reconnection (step 2) where they produce new electron-positron pairs (step 3). This weighs down the plasma fed into the reconnection zone (step 4), dampening subsequent particle acceleration and photon emission, thereby closing the feedback loop.
        </p>
    </div>
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/knpp_schematic.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            The main sequence of events that results in jets being observed.
        </div>
    </div>
</div>

<h4>
What I did
</h4>
To characterize magnetic reconnection in the presence of this radiative feedback, I first performed an analytic study {% cite mehlhaff_etal_2021 %} where I scoped out the parameter space and laid out a basic framework for understanding the regime. Fully characterizing it, though, required a follow-up numerical study {% cite mehlhaff_etal_2024 %}. To power this study, I outfitted the <span style="font-family: 'Courier New', Courier, monospace;"><a href="https://ui.adsabs.harvard.edu/abs/2019ascl.soft11012C/abstract">ZELTRON</a></span> particle-in-cell code to self-consistently account for the relevant gamma-ray transport and pair production.

<h4>
What I found
</h4>
The coupling of reconnection to gamma-ray radiation and pair production has pronounced effects on the **observable radiation spectrum** and on the **ambient plasma**. 

Pair production tends to reprocess energy injected into extremely energetic particles -- those whose radiation emerges almost exclusively above pair-production threshold -- to lower energies. This stabilizes the observable (i.e., below pair-production threshold) gamma-ray spectrum. Thus, the prominent harder-when-brighter trend observed in many types of blazars is replaced by a universal spectral slope independent of gamma-ray luminosity. This indeed seems to reflect <em>Fermi</em> observations of flat-spectrum radio quasars. 

Meanwhile, pair production also loads the plasma processed by reconnection with new electron positron pairs. We identified a regime where reconnection might pump copious pairs into the jet, substantially changing its composition <em>in situ</em>.

<h3>
Scenario 2: Magnetized turbulence 
</h3>
In addition to the formation and dissipation of large-scale reconnection layers, black hole jets may also become turbulence. Reconnection and turbulence are not necessarily mutually exclusive, since intermittent reconnection layers are often witnessed in magnetized turbulence. However, the resulting current sheets are in any case more random and unpredictable. Magnetized turbulence may also efficiently dissipate jet magnetic field energy.

While the particle acceleration process is somewhat different, the plasma environment is the same. Thus, we expect turbulence to also couple to the same radiative physics and pair production as reconnection would in its place. 

<h4>
What I did
</h4>
<div class="row align-items-center">
    <div class="col-sm mt-0">
        <p>
I used the code developed for my previous reconnection work {% cite mehlhaff_etal_2024 %} to perform a novel numerical study of turbulence {% cite mehlhaff_etal_2025a %} coupled to the same radiation mechanisms and pair production. A snapshot from one of the simulations is shown here.
        </p>
    </div>
    <div class="col-sm mt-0">
        {% include figure.liquid loading="eager" path="assets/img/knpp_turb.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            The main sequence of events that results in jets being observed.
        </div>
    </div>
</div>

<h4>
What I found
</h4>
Like in the case of reconnection, feedback from pair production dictates the main features of magnetized turbulence. Initially, particle acceleration due to turbulence is much more efficient than radiative cooling, leading to a burst of nonthermally distributed energetic particles and, as a result, gamma-ray radiation and pair production. Subsequently, newborn pairs accumulate and weigh down the plasma, slowing particle acceleration down. By producing its own plasma, turbulence self-regulates until an equilibrium is reached between particle acceleration and radiative cooling. 

Because the final equilibrium is so simple, we were able to analytically predict the number of pairs produced as the plasma approaches its terminal state. This we compared to expected plasma conditions in jets from flat-spectrum radio quasars. For jets in these systems, we found that may substantially increase the pair count <em>in situ</em>.

We were also able to predict the observable radiation spectrum produced in the final equilibrium state of the turbulence. It is a thermal one with a very predictable characteristic photon energy. However, we are unsure how observable this spectrum would be since, once turbulence subsides, it would fade away. The imprint left on the pair content of the jet would, however, be a permanently imprinted in the downstream plasma.

<h2>
Conclusions
</h2>
Whether reconnection or turbulence, dissipation in black hole jets may be intimately linked with their material compositions. These works open up the possibility that gamma-ray signatures may encode information about changes in the pair content of the plasma. There is also hope that we may be able to distinguish the particle acceleration mechanisms: reconnection seems to produce a universal power-law spectrum; turbulence, once equilibrated, produces a thermal spectrum. More work needs to be done to understand the jet structure and the dissipative zones that it naturally produces to situate these models more explicitly in a global context.
