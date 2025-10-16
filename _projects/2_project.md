---
layout: page
title: black hole jets 
description: their energy dissipation, composition, and appearance 
img: assets/img/cygnusa.jpg
importance: 2
category: themes
giscus_comments: false
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
To characterize magnetic reconnection in the presence of this radiative feedback, I first performed an [analytic study](https://ui.adsabs.harvard.edu/abs/2021MNRAS.508.4532M/abstract) where I scoped out the parameter space and laid out a basic framework for understanding the regime. Fully characterizing it, though, required a follow-up [numerical study](https://ui.adsabs.harvard.edu/abs/2024MNRAS.52711587M/abstract). To power this study, I outfitted the <span style="font-family: 'Courier New', Courier, monospace;"><a href="https://ui.adsabs.harvard.edu/abs/2019ascl.soft11012C/abstract">ZELTRON</a></span> particle-in-cell code to self-consistently account for the relevant gamma-ray transport and pair production.

<h4>
What I found
</h4>
The coupling of reconnection to gamma-ray radiation and pair production has pronounced effects on the **observable radiation spectrum** and on the **ambient plasma**. 

Pair production tends to reprocess energy injected into extremely energetic particles -- those whose radiation emerges almost exclusively above pair-production threshold -- to lower energies. This stabilizes the observable (i.e., below pair-production threshold) gamma-ray spectrum. Thus, the prominent harder-when-brighter trend observed in many types of blazars is replaced by a universal spectral slope independent of gamma-ray luminosity. This indeed seems to reflect <em>Fermi</em> observations of flat-spectrum radio quasars. 

Meanwhile, pair production also loads the plasma processed by reconnection with new electron positron pairs. We identified a regime where reconnection might pump copious pairs into the jet, substantially changing its composition <em>in situ</em>.

<h3>
Scenario 2: Magnetized turbulence 
</h3>

<div class="row align-items-center">
</div>

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
