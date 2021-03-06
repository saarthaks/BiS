---
title: Neurogrid - The Board
date: '2016-05-25'
author: src/data/alumni/ben-varkey-benjamin.yaml
categories:
  - src/data/categories/general.yaml
tags:
image: images/BoardNoCovers288x194.jpg
image_alt: Neuromorphic Chip
figure: images/BoardNoCovers288x194.jpg
figure_caption: >-
  <b>Neurogrid.</b> With sixteen 12x14 sq-mm chips (Neurocores) assembled on a 6.5x7.5 sq-in circuit board (shown above), Neurogrid can model a slab of cortex with up to 16x256x256 neurons—over a million! The chips are interconnected in a binary tree by 80M spike/sec links. An on-chip RAM (in each Neurocore) and an off-chip RAM (on a daughterboard, not shown) softwire vertical and horizontcal cortical connections, respectively [<a href="http://web.stanford.edu/group/brainsinsilicon/documents/BenjaminEtAlNeurogrid2014.pdf" target="_blank">B V Benjamin 2014</a>].
excerpt: >-
  Recent breakthroughs in neuromorphic engineering make it possible to combine analog's parallel operation with digital's programmability, reaping the best of both worlds.
seo:
  title: Neurogrid - The Board
  description: 'Neurogrid simulates one million neurons with two subcellular compartments each.'
  extra:
    - name: 'og:type'
      value: article
      keyName: property
    - name: 'og:title'
      value: Neurogrid - The Board
      keyName: property
    - name: 'og:description'
      value: 'Neurogrid simulates one million neurons with two subcellular compartments each.'
      keyName: property
    - name: 'og:image'
      value: images/3.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Neurogrid - The Board
    - name: 'twitter:description'
      value: 'Neurogrid simulates one million neurons with two subcellular compartments each.'
    - name: 'twitter:image'
      value: images/3.png
      relativeUrl: true
template: post
---
Inspired by GRAPE-6, a $60K supercomputer that has revolutionized astrophysics, Neurogrid provides an affordable option for brain simulations. It uses analog computation to emulate ion-channel activity and uses digital communication to softwire synaptic connections. These technologies impose different **constraints**, because they operate in parallel and in serial, respectively. Analog computation constrains the number of distinct ion-channel populations that can be simulated—unlike digital computation, which simply takes longer to run bigger simulations. Digital communication constrains the number of synaptic connections that can be activated per second—unlike analog communication, which simply sums additional inputs onto the same wire. Working within these constraints, Neurogrid achieves its goal of simulating multiple cortical areas in real-time by making judicious choices.

> Recent breakthroughs in neuromorphic engineering make it possible to combine analog's parallel operation with digital's programmability, reaping the best of both worlds.

Neurogrid simulates one million neurons with two subcellular compartments each, a choice motivated by neurophysiological studies. Nonlinear interactions between projections that terminate in distinct cortical layers have been replicated in a pyramidal-cell model with just **two compartments**. Furthermore, varying the compartments' electrical coupling replicates the firing patterns of various pyramidal-cell types. Capturing these behaviors using the smallest number of compartments minimizes the number of distinct ion-channel populations that need to be simulated, thereby maximizing the number of neurons a model can have.

> Neurogrid simulates a million neurons connected by billions of synapses in real-time, rivaling a supercomputer while consuming a 100,000 times less energy—five watts instead of a megawatt!

Neurogrid simulates six billion synapses connected in structured patterns, a choice motivated by neuroanatomical studies. Cortical axons synapse profusely in a local area, course along for a while, then do it again. Thus, nearby neurons receive inputs from largely the same axons, as expected from the contiguous (map-like) organization of cortical areas. Local wires running between neighboring silicon neurons emulate these **patchy arbors** using analog communication, invoking postsynaptic potentials within a programmable radius. A patch radius of 6 neurons, for example, lets a single softwired axon make a hundred synapses—increasing the total number of synaptic connections possible from 60 million to six billion.
