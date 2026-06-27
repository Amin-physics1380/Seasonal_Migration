# Effect of seasonal migration in selection for geographically-divided population

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue.svg)](https://www.python.org/)

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

## Features

- Numerical integration of population dynamics with seasonal forcing
- Parameter sweeps over seasonal period \(T\), migration rates, and island-specific birth rates
- Transient period exclusion for robust stationary-state analysis
- Computation of long-term average mutant populations
- Phase analysis for synchronization 

## Model Parameters

### Default / Base Parameters

| Parameter                        | Symbol       | Value          | Description |
|-------------------------------|--------------|----------------|-----------|
| Initial population (Island 1) | \( n_1(0) \) | 0.01           | Mutants on Island 1 |
| Initial population (Island 2) | \( n_2(0) \) | 0.00           | Mutants on Island 2 |
| Total simulation time         | \( T_{\max} \) | 100,000      | Time units |
| Time step                     | \( \Delta t \) | 0.1            | Integration step |
| Resident birth rate           | \( r \)        | 1              | Both islands |
| Resident death rate           | \( d \)        | 1              | Both islands |
| Mutant death rate             | \( d_m \)      | 1              | - |
| Transient exclusion period    | -            | 40,000         | Time units discarded |

### Variable Parameters (Sweeps)

- **Seasonal period** (\( T \))
- **Migration rates** (\( \alpha_0 \), \( \beta_0 \))
- **Mutant birth rates** (\( r_{A1} \), \( r_{A2} \))

---

## Outputs

- Time series: \( n_1(t) \), \( n_2(t) \)
- Long-term average mutant population (average_of_averages)
- Phase values and phase differences 




