# Agent-based modeling simulation of Monkeypox transmission in Colombo city that incorporates transportation dynamics to examine its spread and impact.

## Background
The highest population density in Sri Lanka is found in Colombo City, with a density of 13,364 km^2. In this study, we simulate the transmission dynamics of Mpox within a 1 km^2 region of Colombo City. Our approach employs agent-based modeling to represent interactions between humans based on their travel modes.

## Model Parameters
- **μ_h (Natural Mortality Rate of Humans)**: Estimated from Sri Lankan data, with an average lifespan of approximately 76 years. Calculated as μ_h = 1 / (76 × 54) per week.
- **θ_h (Recruitment Rate of Humans)**: Assumed to be very low.

Other parameters are obtained from literature sources, except for:
- Contact rates of public transportation using susceptible and infectious humans (β_3).
- Contact rates of private transportation using susceptible and infectious humans (β_4).
- Contact rates of public/private transportation using susceptible humans and private/public transportation using infectious humans (β_5).
- Fraction of exposed humans who do not get infected (α_r). These values are assumed.

## Population Assumptions
- The total population of Colombo District uses both private and public transportation methods.


## Disease Dynamics
- All individuals in the total population are initially in the susceptible state.
- Exposed humans do not get infected, and only α_h fraction from the exposed humans becomes infected with a transmission rate of σ_h. Others return to the susceptible state.
- Infected humans can move into an isolated state with a probability of ρ. Isolated individuals are infected but not infectious.
- Infectious individuals can move to the recovered state with rates τ (isolated) and γ (infectious).
- After recovery, individuals gain natural immunity and do not return to the susceptible state.
- Infected humans in the infectious state die at a rate of δ_h due to Mpox, higher than the natural mortality rate μ_h.
- Monkeypox can be transmitted to humans by both humans and rodents. Susceptible humans can be exposed to infected rodents with a contact rate of β_1.

## Rodent Dynamics
- Susceptible rodents become exposed to infected rodents with a contact rate of β_2.
- Disease transmission to rodents is assumed to occur only between rodents with a rate of σ_r.
- Only α_r fraction from exposed rodents move to the infectious state, while others return to the susceptible state.
- Rodent recovery and death rates are not discussed.

This simulation investigates the complex dynamics of Mpox transmission in an urban environment, considering various human and rodent factors.
