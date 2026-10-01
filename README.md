# SCM_Simulation

A vectorized MATLAB implementation of the Shrinking Core Model (SCM) to simulate gas-solid reduction kinetics and evaluate mass transfer resistances in iron ore (Fe₂O₃ + 3CO → 2Fe + 3CO₂).

## Overview
This repository contains a computational simulation developed to determine the rate-controlling mechanisms during the isothermal reduction of iron ore pellets. By calculating characteristic times and mass transfer Biot numbers across varying pellet geometries (5 mm to 20 mm), the model mathematically identifies whether the reduction process is limited by external gas film diffusion, internal ash layer diffusion, or interfacial chemical reaction.

## Repository Contents
* **`shrinking_core_model.mlx`**: The primary MATLAB Live Script containing the vectorized solver, physical constants, and plotting functions.
* **`SCM_Report.pdf`**[cite: 6]: A comprehensive project report detailing the methodology, mathematical framework, and an analysis of the computational results.

## Theoretical Background
The Shrinking Core Model decouples the overall reaction time to reach a conversion fraction ($X$) into three distinct mass transfer and kinetic resistances:
1. **Gas Film Diffusion:** Transport of CO gas through the stagnant boundary layer.
2. **Ash Layer Diffusion:** Diffusion of gas through the porous, newly formed iron product layer.
3. **Chemical Reaction:** The intrinsic reaction kinetics at the unreacted hematite core.

The model dynamically evaluates the Mass Transfer Biot Number ($Bi_m = \frac{k_g R}{D_e}$) to quantify the ratio of internal diffusion resistance to external film resistance.

## Key Findings
* **Small geometries (R = 5 mm):** Reduction is strictly bounded by interfacial chemical reaction kinetics ($Bi_m = 25.0$).
* **Large geometries (R = 20 mm):** As the radius scales, the Biot number increases ($Bi_m = 100.0$) and internal ash layer diffusion strongly throttles the overall reduction rate due to its quadratic ($R^2$) dependence on the pellet radius.

## Usage
To run the simulation locally:
1. Clone the repository to your local machine.
2. Open `shrinking_core_model.mlx` in MATLAB (R2021a or newer recommended for Live Scripts).
3. Run the script to instantly generate the Conversion vs. Time ($X$ vs. $t$) plots and output the dominant resistance parameters to the console.

---
**Author:** Prabhat Solanki  
**Institution:** National Institute of Technology (NIT), Rourkela  
**Field:** Metallurgical and Materials Engineering
