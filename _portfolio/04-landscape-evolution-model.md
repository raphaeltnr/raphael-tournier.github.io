---
title: "Landscape Evolution Model (gospl)"
excerpt: "Long-term landscape evolution modelling.<br/><img src='/images/portfolio-gospl.png'>"
collection: portfolio
---

Landscape evolution is modelled using gospl, developed by Tristan Salles, and used to reconstruct the physiography of the East African Rift through time.

To do so, I use the outputs of the climate and elevation models as inputs, and calibrate gospl to account for erodibility and evaporation, using two complementary approaches:

- **Continuous approach**: a single run spanning the full 30 Ma period
- **Guided approach**: a discontinuous run, with control and recalibration at each 1 Ma time step
