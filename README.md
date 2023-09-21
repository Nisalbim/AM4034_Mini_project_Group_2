# Agent-based modeling simulation of Monkeypox transmission in Colombo city that incorporates transportation dynamics to examine its spread and impact.

## Background
The highest population density in Sri Lanka is found in Colombo City, with a density of 13,364 km^2. In this study, we simulate the transmission dynamics of Mpox within a 1 km^2 region of Colombo City. Our employs agent-based modeling to represent interactions between humans based on their travel modes. To simulate this, Analogic software was used. There are only three classes. Rodent and human agents are the two primary classes. Define all parameters in the main class. For each agent, a class-state diagram for humans and rodents is defined.

## Model Parameters

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

## Population Assumptions
- The total population of Colombo District uses both private and public transportation methods.
- Initially, one rodent was infected. 

## Disease Dynamics
- All individuals in the total population are initially in the susceptible state.
- Exposed humans do not get infected, and only α_h fraction of the exposed humans become infected with a transmission rate of σ_h. Others return to the susceptible state.
- Infected humans can move into an isolated state with a probability of ρ. Isolated individuals are infected but not infectious.
- Infectious individuals can move to the recovered state with rates τ (isolated) and γ (infectious).
- After recovery, individuals gain natural immunity and do not return to the susceptible state.
- Infected humans in the infectious state die at a rate of δ_h due to Mpox, higher than the natural mortality rate μ_h.
- Monkeypox can be transmitted to humans by both humans and rodents. Susceptible humans can be exposed to infected rodents with a contact rate of β_1.

## Rodent Dynamics
- Susceptible rodents become exposed to infected rodents with a contact rate of β_2.
- Disease transmission to rodents is assumed to occur only between rodents with a rate of σ_r.
- Only α_r fraction of exposed rodents move to the infectious state, while others return to the susceptible state.
- Rodent recovery and death rates are not discussed.

This simulation investigates the complex dynamics of Mpox transmission in an urban environment, considering transportation-type factors.
