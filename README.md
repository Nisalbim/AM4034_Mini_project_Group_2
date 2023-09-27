# Monkeypox Transmission Dynamics Simulation

## Introduction

This repository presents an Agent-Based Modeling (ABM) approach to simulate the transmission dynamics of Monkeypox (Mpox) based on human transportation modes in a 1 km² area of Colombo city. Monkeypox is a contagious disease caused by a virus, with potential transmission routes from person to person and from animals to humans.

### Background

Mpox transmission dynamics have traditionally been modeled using compartmental models with Ordinary Differential Equations (ODEs). However, this project employs an ABM approach to provide a more detailed individual-level perspective of the population, allowing us to observe how infection dynamics change with varying fractions of private transportation users.

## Methodology

### Transmission Model Parameters

The model utilizes the following parameter values:

| Parameter | Description                                      | Value     | Unit          |
|-----------|--------------------------------------------------|-----------|---------------|
| θ_h       | Recruitment rate into susceptible humans        | 0.5       | Per week      |
| θ_r       | Recruitment rate into susceptible rodents       | 0.2       | Per week      |
| ϕ         | Fraction of private transport users             | 0.441     |               |
| β_1       | Contact rate of susceptible humans and rodents  | 0.3632    | Per week      |
| β_2       | Contact rate of susceptible rodents and rodents | 0.1802    | Per week      |
| β_3       | Contact rate of susceptible public and humans   | 0.5       | Per week      |
| β_4       | Contact rate of susceptible private and humans  | 0.2       | Per week      |
| β_5       | Contact rate of susceptible public/private and infectious private/public human | 0.4 | Per week |
| α_h       | Fraction of exposed humans being infected       | 0.132     |               |
| α_(r)     | Fraction of exposed rodents being infected      | 0.11      |               |
| ρ         | Probability of being an isolated human from an infected human | 0.8 |             |
| σ_h       | Transition rate of exposed human to infected human | 0.3966 | Per week    |
| σ_r       | Transition rate of exposed rodents to infected rodents | 0.541 | Per week |
| γ         | Humans' recovery rate                           | 0.83      | per year     |
| τ         | Recovery rate from isolated to recovery state   | 0.036246  | per week     |
| δ_h       | Human death rate induced by Mpox                | 0.0012    | per week     |
| δ_r       | Rodent death rate induced by Mpox               | 0.5       | per year     |
| μh        | Natural mortality rate of humans                | 0.000243665 | per week   |
| μr        | Natural mortality rate of rodents               | 0.0012    | per week     |

(Include the rest of the parameter values from Table 1)

### Agent-Based Modeling

The simulation utilizes an ABM approach, where agents represent individuals in the system. Two agent classes, human and rodent agents, are considered. Human transportation mode (public or private) is a characteristic of human agents. The model accounts for various states, such as susceptible, exposed, isolated, infectious, and recovered, for both human and rodent agents.

## Results

The simulation results demonstrate how the transmission dynamics of Mpox change with varying fractions of private transportation users. Three experiments were conducted with different fractions: 0.3, 0.441, and 0.5. The number of infected individuals and deaths were tracked over 1000 days for each experiment. Detailed graphs and data can be found in the project documentation.

### Experiment 1: ϕ = 0.3

- Total Infected: 29
- Total Deaths: 6
- Public Infected: 17
- Private Infected: 12

(Include results for experiments 2 and 3)

## Discussion

(Add a discussion section where you analyze the results and discuss their implications.)

## Conclusion

(Include a conclusion summarizing the findings and potential future work.)

## Usage

(Provide instructions on how to run the simulation or use the code.)

## Contributors

- [Your Name](https://github.com/yourusername)

## License

This project is licensed under the [MIT License](LICENSE).

