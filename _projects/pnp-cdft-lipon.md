---
layout: page
title: Li⁺ transport in LiPON via PNP–cDFT
description: A Poisson–Nernst–Planck + classical DFT framework for solid-electrolyte ion transport, implemented in Python/JAX
img:
importance: 1
category: research
related_publications: false
---

**Status: ongoing** · University of Waterloo, Prof. Tetsassi Feugmo's group · Jan 2026 – present

## The problem

Solid-state batteries need electrolytes that conduct Li⁺ quickly and reliably. LiPON (lithium phosphorus oxynitride) is a workhorse thin-film solid electrolyte, but the link between its microscopic structure and its macroscopic transport behavior — how fast ions actually move, and how that changes with temperature — is not fully resolved. Continuum models alone miss the structure of the ion environment; fully atomistic simulations are expensive and hard to connect to device-scale behavior.

## The approach

I am implementing and analyzing a coupled **Poisson–Nernst–Planck (PNP) + classical density functional theory (cDFT)** model:

- **PNP** describes ion migration and diffusion under electrochemical gradients at the continuum level.
- **Classical DFT** supplies a statistical-mechanical description of the local ion environment, correcting the mean-field picture with correlations and finite-size effects.
- The framework is implemented in **Python with JAX**, which gives automatic differentiation and easy GPU acceleration for the nonlinear solves.

Using transport parameters from the literature, I study **temperature-dependent Li⁺ diffusion** and transport trends in LiPON.

## Why this matters (and what's next)

This bridges two scales that are usually treated separately: statistical-mechanical structure and device-level transport. Next steps include validating against published conductivity data and extending the framework to other amorphous solid electrolytes.

*Notes and updates on this project appear in the [blog](/blog/).*
