---
layout: default
title: Pandemic Simulation Case Study
---

# Modeling Disease Spread with Python

In this project, I developed a simulation engine that models the "attack rate" of a pandemic within a population. Each individual (agent) in the system is represented by a dictionary tracking their health state, vaccination status, and social behaviors.

## How it Works
The simulation runs on a day-by-day loop. Each day, "infectious" agents interact with "susceptible" agents. The probability of transmission is determined by a complex set of factors:
* **Vaccination Effectiveness:** Reduces the likelihood of a susceptible agent becoming infected.
* **Masking & Social Isolation:** Decreases the "shedding" rate of infected agents.
* **Asymptomatic Carriers:** Modeled as agents who do not isolate because they are unaware of their status.



## The Technical Challenge: `binnedSample()`
One of the core challenges was implementing a sampling algorithm that could handle both individual integers and "sub-population" tuples. This required writing robust logic to ensure the simulation could scale from a single group to multiple interacting demographics.

## Results & Analytics
The simulation outputs a "Pandemic Curve," which tracks total infections over time. This data can be used to visualize how "flattening the curve" works when you adjust parameters like masking frequency (`mp`) or vaccination probability (`vp`).

---
*Note: This project was completed as part of my CS1210 coursework. The logic focuses on the implementation of agent-based modeling and random distribution.*
<div style="margin-top: 50px; padding-bottom: 50px; text-align: center;">
  <a href="./" style="
    display: inline-block;
    background-color: #0366d6; 
    color: #ffffff !important; 
    padding: 12px 24px; 
    text-decoration: none; 
    border-radius: 6px; 
    font-weight: bold;
    border: 1px solid #0366d6;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    ← Back to Home
  </a>
</div>
