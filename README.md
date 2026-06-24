# Effect of seasonal migration in selection for geographically-divided population

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)

## Overview

**Evolutionary Dynamics of Migration Timing under Spatially Heterogeneous Selection**

Evolutionary dynamics studies how new heritable strategies arise and spread through a population. The fate of a mutant type is most simply determined by its intrinsic fitness advantage over the resident, or wild-type, population. However, this simple picture is substantially complicated once spatial structure, environmental heterogeneity, or game-theoretic interactions with neighboring types are introduced — any of these can convert a mutant that would be unconditionally advantageous in a well-mixed population into one that is effectively neutral or even deleterious.

A particularly important and broadly studied factor is the migration, or motility, potential of competing types. A long-standing question in theoretical evolution concerns the conditions under which the acquisition of motility as a new trait increases or decreases a mutant's probability of fixation or its steady-state frequency — there is no universal answer, and the sign of the effect depends sensitively on the details of population structure and how migration is implemented.

A closely related factor is environmental heterogeneity across habitats, which often drives the evolution of "specialist" versus "generalist" strategies. In general, a mutant may be favored in one habitat — for instance, one with more abundant nutrients — while being neutral or actively disfavored relative to residents in another. Migration between such habitats can raise a mutant's overall steady-state frequency by allowing it to colonize and persist in its favorable habitat while continually reseeding the less favorable one.

This project investigates the **effect of temporal (seasonal) fluctuations in migration** on evolutionary dynamics in a spatially subdivided (two-island) metapopulation. We examine how the *temporal structure* of migration (period, phase, and symmetry) interacts with spatially heterogeneous selection to shape a mutant's long-term success — independent of changes in the time-averaged migration rate.

## Research Gap

Previous studies have examined migration in spatially structured and temporally varying environments from complementary angles (Princepe et al. on intermittent connectivity and speciation; Blanquart & Gandon 2011/2014, Griswold et al. 2010, Donohue & Piiroinen 2015 on the evolution of migration; Wei et al. 2015 on constant migration under heterogeneous selection). 

This work bridges these threads by focusing specifically on **periodic migration timing** under fixed spatial selection differences.

## Model

We employ the **Death-Birth Moran process** in a two-island system, each with constant population size \(N\).

- Mutants (type A) have island-specific fitness (birth rates \(r_{A1}\), \(r_{A2}\)).
- Residents (type B) have baseline fitness.
- Migration is a **property of place** (identical for both types) but varies **periodically** in time, mimicking seasonal patterns.

### Migration Scenarios

1. **Symmetric In-Phase Periodic Migration**  
   \( W_{12} = W_{21} = \alpha_0 \cos^2(\pi t / T) \)

2. **Symmetric Out-of-Phase Periodic Migration**  
   \( W_{12}(t) = \alpha_0 \cos^2(\pi t / T) \),  
   \( W_{21}(t) = \alpha_0 \sin^2(\pi t / T) \)

3. **Asymmetric In-Phase Periodic Migration**  
   Different amplitudes \(\alpha_0\) and \(\beta_0\) with in-phase oscillation.

4. **Asymmetric Out-of-Phase Periodic Migration**  
   Phase-shifted asymmetric flows.

Key observables include the long-term average mutant frequency \(\bar{\phi}\) and the phase difference \(\Phi\) between islands.

The deterministic mean-field equations in the large-\(N\) limit govern the dynamics.

## Repository Structure



