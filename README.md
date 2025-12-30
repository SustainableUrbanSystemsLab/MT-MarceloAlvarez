# An urban microclimate comparative study between ENVI-met and Outdoor+

<img src="https://raw.githubusercontent.com/SustainableUrbanSystemsLab/MT-MarceloAlvarez/main/graph_abstract.png" alt="graphical_abstract" style="max-width: 100%;">

## Overview

Cities increasingly face challenges associated with the Urban Heat Island (UHI) effect. Reduced vegetation cover and extensive impervious surfaces in dense built environments result in significantly higher temperatures compared to surrounding rural areas. Key contributing factors include building mass, orientation, heat absorption, and material properties. Accurately capturing the complex interactions between these variables is essential for designers and decision-makers working with urban microclimate simulations.

This repository documents a comparative study between ENVI-met and Outdoor+, focusing on their ability to model fine-scale urban microclimate interactions with respect to air temperature, specific humidity, and wind speed.

## Steps to reproduce this study

1. Download the ENVI-met and Outdoor+ tools from the [ENVI-met](https://www.envimet.com/) and [Outdoor+](https://docs.eddy3d.com/outdoorplus/first_steps/#overview) websites.

2. Work in progress...

## Tools

### ENVI-met

ENVI-met is a well-established, state-of-the-art urban microclimate simulation tool widely used and validated against field measurements for air temperature, solar radiation, thermal comfort, and vegetation-related processes. Existing literature, however, identifies limitations related to wind speed simulation, turbulence representation, and humidity dynamics.

### Outdoor+

Outdoor+ is a parametric user-interface plugin that streamlines the application of the urbanMicroclimateFoam solver, an open-source, multi-region, coupled physical solver based on OpenFOAM. The solver resolves steady-state airflow and captures the unsteady transport of heat, air, and moisture with improved computational efficiency. Known limitations include high sensitivity to mesh quality, limited vegetation modeling, and a steep learning curve.

Outdoor+ embeds the solver within a 3D modeling and parametric environment, exposes primary inputs through visual programming, and avoids text-based case editing.

## Case Studies

Two urban scenarios are used for comparison:

### Stadium

### Educational Center

Both case studies are simulated using ENVI-met and Outdoor+ under harmonized boundary conditions to isolate solver behavior.

## Methodology

The comparative analysis is structured into two categories:

### Probing-Point Analysis

Time-series comparison at pedestrian height

Evaluated under open, exposed, covered, corridor, and entrance conditions

Qualitative assessment of temporal variability and sensitivity

### Full-Domain Comparison

Statistical indicators:

Willmott’s Index of Agreement

Coefficient of Determination (R²)

Root Mean Squared Error (RMSE)

Mean Absolute Error (MAE)

Scatter-plot analysis for spatial agreement

## Outputs

The analysis produces the following outputs for both case studies:

- Heatmaps for air temperature, specific humidity, and wind speed
- Statistical agreement metrics
- Scatter plots
- Temporal profiles at probing points

## Results

Across both case studies:

Air temperature shows weak-to-moderate agreement between tools.

Specific humidity and wind speed exhibit poor agreement.

Outdoor+ captures wider variability and stronger sensitivity to geometry and boundary conditions, while ENVI-met produces more uniform spatial distributions, particularly for wind speed. Outdoor+ more closely follows EPW boundary reference values for air temperature and humidity, whereas ENVI-met exhibits reduced temporal and spatial variation.

Wind speed results show substantial disagreement, with Outdoor+ capturing a wider range of magnitudes and stronger fluctuations, while ENVI-met remains nearly constant across the domain.

## Discussion

Observed discrepancies are attributed to differences in solver physics, boundary condition treatment, model resolution, and sensitivity to geometry, shading, vegetation, and fine-scale aerodynamics. Outdoor+ demonstrates stronger capability in capturing fine-scale microclimate interactions, while ENVI-met simplifies humidity and wind representation. The magnitude of disagreement in specific humidity and wind speed is the most unexpected outcome.

## Limitations

- Focus on raw microclimate indicators only
- Two case studies
- No soil profile or custom terrain modeling

Generalization across urban typologies and climate zones is therefore limited.

## Future Work

Expansion to additional climate zones and urban typologies

Inclusion of human-centered comfort metrics (MRT, UTCI, PET)

Integration of soil and terrain modeling

Improved vegetation representation

## Conclusion

This repository presents a comparative study between ENVI-met and Outdoor+ focused on raw urban microclimate indicators. By harmonizing simulation settings, solver-specific behavior is isolated, enabling detailed analysis of fine-scale urban interactions. The main contribution is positioning Outdoor+ as a feasible and flexible design-oriented tool for advanced urban microclimate analysis, emphasizing trade-offs between accuracy, computational efficiency, and usability.

## Author

- **Marcelo Alvarez**

- MS. in Design Computation

- School of Architecture, Georgia Institute of Technology

- Advisor: Dr. Patrick Kastner

## Contact

- [GT Email](mailto:marcelo.alvarez@gatech.edu)
- [Gmail](mailto:alvarezdm.arch@gmail.com)
- [LinkedIn](https://www.linkedin.com/in/alvarezdm/)
