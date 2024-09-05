Numerical Analysis of 1D Steady-State Heat Equation with Discontinuity

Project Overview

This project investigates the behavior of heat transfer in a one-dimensional rod with a discontinuity in thermal conductivity. The analysis is based on solving the steady-state heat equation, a fundamental partial differential equation used in thermal engineering. The main focus is on understanding how a sudden change in material properties, such as thermal conductivity, affects the temperature distribution along the rod.

Objectives

The primary goals of this project include:

Analyzing the impact of a discontinuity in thermal conductivity on the temperature profile of the rod.
Comparing the numerical solutions obtained using the Finite Difference Method (FDM) with exact analytical solutions to validate the accuracy of the model.
Investigating the effects of varying the ratio of thermal conductivities (k1/k2) on heat transfer efficiency.
Exploring how the position of the discontinuity, whether at a computational node or between nodes, influences the temperature distribution and heat flux.

Methodology

Analytical Solution:

The problem is first approached analytically by dividing the rod into two regions based on the discontinuity:

Region 1: Where the thermal conductivity is k1.

Region 2: Where the thermal conductivity changes to k2.

The exact solution is derived by solving the steady-state heat equation in each region separately, applying appropriate boundary conditions, and ensuring continuity at the interface.

Numerical Solution:

The Finite Difference Method (FDM) is used to numerically solve the heat equation. The rod is discretized into a grid, and the second derivative of temperature is approximated using central differences. The key steps include:

Discretizing the spatial domain into grid points.

Setting up difference equations for each region, applying the respective thermal conductivities.

Handling the discontinuity by ensuring continuity of temperature and heat flux at the interface.

Solving the resulting system of linear equations using MATLAB.

Scenarios Analyzed:

The project examines two primary scenarios based on the ratio of thermal conductivities:

k1/k2 < 1: Where the thermal conductivity in the first region is less than in the second region.

k1/k2 > 1: Where the thermal conductivity in the first region is greater than in the second region.

Additionally, the project explores the effect of the discontinuity's position:

At a Computational Node: A sharp transition is expected, accurately captured by the numerical method.

Between Computational Nodes: A smoother transition is observed, representing a more realistic scenario where material properties gradually change.

Findings:

The analysis reveals several key insights:

Temperature Gradient: In cases where k1/k2 < 1, the temperature gradient increases after the discontinuity, indicating a slower heat transfer in the first region. Conversely, when k1/k2 > 1, a steeper temperature increase occurs in the first region, reflecting higher heat conduction efficiency.

Discontinuity Location: When the discontinuity is exactly at a computational node, the transition in temperature is abrupt, which aligns well with the analytical solution. However, when the discontinuity lies between nodes, the numerical method provides a more gradual transition, better suited for modeling materials with smooth property changes.

Numerical vs. Analytical Comparison:

The FDM effectively captures the key characteristics of the temperature profile, closely matching the analytical solution, especially in scenarios where the discontinuity is at a node.

Conclusion:

This project provides a comprehensive analysis of heat transfer in a composite material with varying thermal conductivity. The combination of analytical and numerical approaches offers valuable insights into the thermal behavior of materials, which is crucial for applications in engineering, such as in the design of heat exchangers and thermal management systems.

Installation:

No installation is necessary, but the following tools are required to run the analysis:

MATLAB (for executing the provided scripts):

Usage:

The MATLAB scripts provided in this repository perform the following tasks:

Load and discretize the spatial domain.

Implement the Finite Difference Method to solve the heat equation.

Handle the discontinuity at a node or between nodes.

Compare the numerical solution with the analytical solution.

Visualize the temperature distribution across the rod.

To run the scripts, simply execute them in MATLAB. Each script corresponds to different scenarios based on the thermal conductivity ratio and the discontinuity's location.

Contributing:

Contributions are welcome! If you'd like to improve the analysis or extend the project, please:

Fork the repository.

Create a new branch (git checkout -b feature-branch).

Make your changes and commit them (git commit -am 'Add new feature').

Push to the branch (git push origin feature-branch).

Open a pull request.

Acknowledgments

Special thanks to Professor Schreyer Lynn and Professor Manoranjan at WSU for the guidance and resources provided during this project. The project is based on fundamental concepts in heat transfer, with implementation facilitated by MATLAB.
