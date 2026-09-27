# Effect of seasonal migration in selection for geographically-divided population

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue.svg)](https://www.python.org/)
- NumPy
- Matplotlib

## Model

We employ the **Death-Birth Moran process** in a two-island system, each with constant population size \(N\).

- Mutants (type A) have island-specific fitness (birth rates \(r_{A1}\), \(r_{A2}\)).
- Residents (type B) have baseline fitness.
- Migration is a **property of place** (identical for both types) but varies **periodically** in time, mimicking seasonal patterns .

### Migration Scenarios

1. **Symmetric In-Phase Periodic Migration**  
   $$\( W_{12} = W_{21} = \alpha_0 \cos^2(\pi t / T) \)$$

2. **Symmetric Out-of-Phase Periodic Migration**  
   $$\( W_{12}(t) = \alpha_0 \cos^2(\pi t / T) \)$$,  
   $$\( W_{21}(t) = \alpha_0 \sin^2(\pi t / T) \)$$

3. **Asymmetric In-Phase Periodic Migration**  
   Different amplitudes $$\(\alpha_0\) $$ and $$\(\beta_0\)$$ with in-phase oscillation.

4. **Asymmetric Out-of-Phase Periodic Migration**  
   Phase-shifted asymmetric flows.

Key observables include the long-term average mutant frequency$$\bar{\phi}$$ and the phase difference $$\(\delta \theta\)$$ between islands.

The deterministic mean-field equations in the large-\(N\) limit govern the dynamics.

## Features

- Numerical integration of population dynamics with seasonal forcing
- Parameter sweeps over seasonal period $$\(T\)$$, migration rates, and island-specific birth rate
- Computation of long-term average mutant populations
- Phase analysis for synchronization between population of islands 

## Model Parameters

We provide a code written in Python , "Seasonal_Migration.ipynb" which :

### Default / Base Parameters

| Parameter                        | Symbol       | Value          | Description |
|-------------------------------|--------------|----------------|-----------|
| Initial population (Island 1) | $$\( n_1(0) \)$$ | 0.01           | Mutants on Island 1 |
| Initial population (Island 2) | $$\( n_2(0) \)$$ | 0.00           | Mutants on Island 2 |
| Total simulation time         | $$\( t_{f} \)$$ | 100,000      | Time units |
| Time step                     | $$\( \delta t \)$$ | 0.01            | Integration step |
| Resident birth rate           | $$\( r_{B} \)$$        | 1              | Both islands |
| Resident death rate           | $$\( d_{B} \)$$        | 1              | Both islands |
| Mutant death rate             | $$\( d_{A} \)$$      | 1              | Both islands |

### Variable Parameters 

- **Seasonal period** $$(\( T \))$$
- **Migration rates** $$(\( \alpha_0 \), \( \beta_0 \))$$
- **Mutant birth rates in each island** $$(\( r_{A1} \), \( r_{A2} \))$$

---

## Outputs
This program includes multiple scenarios, each with its own dedicated dataset stored in the "Data" folder.
In these Excel files, the following parameters are reported : 

- Mutant population in each island: $$\( n_1(t) \), \( n_2(t) \)$$ 
- Phase differences (phases)
- Birth rate for each island $$(r_{A1} , r_{A2})$$
- Amplitude of migration rate $$(\alpha_0 , \beta_0)$$
- The time step for saving data (time)
- Average population of mutants which is variable (average_population)
- Average of the average population in the constant migration case (constant_migration) 
  
> [!Note]
> 
> Phase parameter calculations use the same input parameters as the average population but we calculate phase parameter just for the symmetric in_phase case because in the other scenarios it is negligible.  



