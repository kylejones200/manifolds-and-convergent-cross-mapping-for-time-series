# Manifolds and the Geometry of Dynamics for Time Series Analysis

Time series data often represent observations from complex systems governed by non-linear, deterministic processes. Traditional linear models fail to capture such intricacies, but manifold reconstruction methods, particularly the pioneering work by George Sugihara and colleagues, offer powerful tools for studying these systems. This chapter explores time series manifolds, embedding theory, and their applications in uncovering the geometry of dynamic systems.

## The Geometry of Time Series: Manifolds and Attractors

In non-linear dynamics, systems evolve on structures called manifolds. These are smooth, high-dimensional surfaces that describe the system's state space. Over time, these dynamics may collapse into an attractor, a lower-dimensional structure capturing the system's essential behavior.

Examples include:

- A dripping faucet's dynamics following a chaotic yet deterministic pattern represented by an attractor.

- Climate systems evolving on a manifold defined by interacting variables such as temperature, pressure, and ocean currents.

The central challenge lies in reconstructing these manifolds from one-dimensional time series data.

## Takens' Embedding Theorem and State Space Reconstruction

Takens' Embedding Theorem demonstrates that it is possible to reconstruct the state space of a system using time-delayed observations of a single variable.

Under suitable conditions, the reconstructed manifold is topologically equivalent to the true state space, preserving the system's dynamics.

## Nonlinear Forecasting and Causality

Building on manifold reconstruction, Sugihara developed practical tools for analyzing time series, emphasizing:

- Nonlinear Forecasting: Predicting system behavior using reconstructed manifolds.

- Causal Inference: Distinguishing causation from correlation by analyzing interactions between manifolds.

## Convergent Cross Mapping (CCM)

A key innovation by Sugihara is Convergent Cross Mapping (CCM), a method for inferring causality from time series data. CCM exploits the geometry of reconstructed manifolds to determine whether one variable's dynamics are influenced by another.

Principle: If variable $X$ drives $Y$, the dynamics of $Y$ should encode information about $X$. This information can be extracted by:

- Reconstructing $Y$'s manifold.

- Using it to estimate $X$'s values.

- Evaluating estimation accuracy to infer causality.

## Advantages of Time Series Manifolds

- Preserving Nonlinear Dynamics: Manifolds capture the system's true geometry, preserving non-linear dynamics that linear models cannot represent.

- Causality Testing: Manifold approaches explicitly test causation rather than relying on correlation.

## Applications

Ecology

- Marine ecosystems: CCM uncovers predator-prey relationships, such as sardine and anchovy populations in the California Current.

- Biodiversity dynamics: Reconstructed manifolds reveal species interaction effects on population changes.

Climate Science

- El Niño-Southern Oscillation (ENSO): Manifolds help uncover causal links between ocean temperature anomalies and global climate patterns.

- Tipping points: Early warning signals for climate shifts emerge from changes in attractor geometry.

Financial Systems

- Nonlinear forecasting models market dynamics and identifies causal drivers of financial crises.

Medicine and Physiology

- Cardiac dynamics: Reconstructed manifolds of ECG data reveal arrhythmias.

- Neural systems: CCM distinguishes causative from incidental neural interactions in brain activity.

## Constructing and Analyzing Manifolds: Practical Steps

- Selecting Time Delay ($\tau$): Use the autocorrelation function or mutual information to determine an optimal delay that balances redundancy and information content.

- Choosing Embedding Dimension (m): Apply methods like false nearest neighbors (FNN) to identify the minimal $m$ that unfolds the manifold without overlapping trajectories.

- Reconstruction: Form the embedded vectors and visualize the reconstructed attractor using techniques like 3D phase plots.

- Validation: Validate the reconstructed manifold using forecasting skill (e.g., predicting future states) or CCM results.

## Case Study: Sardine-Anchovy Dynamics

The classic example is using this to measure sardine and anchovy populations in the Pacific Ocean. Sugihara used historical population data to build separate manifolds for sardines and anchovies. Then Sugihara applied CMM to test whether changes in sardine abundance predict anchovy dynamics (and vice versa).

CCM revealed a causal relationship where environmental conditions mediate sardine-anchovy cycles. The reconstructed manifolds provide a geometric interpretation of this interaction.

## Challenges and Future Directions

High-Dimensional Systems

- Reconstructing manifolds in high-dimensional systems quickly becomes computationally intensive as the number of dimensions grows. To overcome this challenge, researchers are focusing on creating more efficient algorithms and exploring advanced dimensionality reduction techniques to streamline the process.

Noise and Data Quality

- Time series data from real-world scenarios often come with noise and missing values, complicating analysis. Developing robust methods to reconstruct manifolds in noisy environments remains a critical area of ongoing research, ensuring accurate insights despite imperfect data.

Integrating Multivariate Data

- While many current applications center on single-variable reconstructions, extending manifold techniques to multivariate time series unlocks deeper insights into complex system dynamics. This approach holds the potential to reveal interconnected patterns across multiple variables, enriching our understanding of underlying processes.

## So What?

Time series manifolds come with limitations but provide a more intuitive understanding of system dynamics compared to traditional methods like neural networks. They help preserve the geometry of non-linear systems, allowing for improved causal inference and forecasting accuracy.

## Key Takeaways

- A dripping faucet's dynamics following a chaotic yet deterministic pattern represented by an attractor.
- Climate systems evolving on a manifold defined by interacting variables such as temperature, pressure, and ocean currents.
- Nonlinear Forecasting: Predicting system behavior using reconstructed manifolds.
- Causal Inference: Distinguishing causation from correlation by analyzing interactions between manifolds.
