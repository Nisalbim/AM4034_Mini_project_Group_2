# Monkeypox Transmission Dynamics Simulation

This repository contains the source code and documentation for a project that uses Agent-Based Modeling (ABM) to simulate the transmission dynamics of Monkeypox (Mpox) based on human transportation modes in a 1 km² area of Colombo city.

## Project Overview

Monkeypox is a contagious disease caused by a virus that can be transmitted from person to person and from animals to humans. This project explores the transmission dynamics of Mpox using an ABM approach, which provides a more detailed and individual-level perspective compared to traditional compartmental models.

## Table 1: Parameter Values

Here are the parameter values used in the simulation:

| Parameter                  | Description                                   | Value       | Source         |
|----------------------------|-----------------------------------------------|-------------|----------------|
| θh                         | Recruitment rate into susceptible humans      | 0.5 per week | [Assumed]      |
| θr                         | Recruitment rate into susceptible rodents     | 0.2 per week | [6]            |
| ϕ                          | Fraction of private transport users           | 0.441       | [7]            |
| β1                         | Contact rate of susceptible humans and infectious rodents | 0.3632 per week | [8] |
| ... (other parameters)     |                                               |             |                |

## Simulation Results

The simulation results show that the fraction of private transport users has an impact on the transmission dynamics of Mpox. Detailed results and figures can be found in the project documentation.

## Getting Started

To run the simulation or explore the code, please follow the instructions provided in the project documentation.

## Contributors

- [Your Name](https://github.com/yourusername)

## License

This project is licensed under the [MIT License](LICENSE).

