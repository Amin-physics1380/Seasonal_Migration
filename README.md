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
We provide a code written in Python , "Seasonal_Migration." : 
> [!IMPORTANT]

> a)The input parameters in code :
> 
> a1) Population of mutans in the first island and second island (0.01  , 0.00)
> 
> a2) Total time of the process (100000)
> 
> a3) Step time (0.1)
> 
> a4) Death rate and birth rate of residents (1 , 1)
> 
> a5) Death rate of mutants (1) 




