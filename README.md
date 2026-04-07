
Computational Framework & Visualizations
While the paper provides the game-theoretic proofs for the signalling equilibrium, the accompanying Python implementation serves two critical roles: Sensitivity Analysis and Stochastic Validation.In economic theory, closed-form solutions (like the derivation of p*) tell us that a boundary exists. The computational model tells us where that boundary moves when human psychological factors—like loss aversion or the sting of rejection—change.Why use a Computational Approach?High-Dimensional Sensitivity: The model depends on four interacting variables (k, e, r2, p). Algebraically solving for every combination is impractical; the code allows us to visualize the "stability" of the equilibrium across thousands of parameter permutations.Bridging Theory and Data: By using Monte Carlo simulations, we move from a "perfectly rational agent" to a "population" of 10,000 simulated dates. This allows us to apply machine learning metrics (Precision, Recall, F1-Score) to a social interaction.

Figure V1: The Bifurcation Surface (p*)
What it shows: This figure maps the threshold attractiveness level (p*) across a range of psychological costs.
The Heatmap: Darker regions indicate a lower p*, meaning even moderately attractive men should start "screening" (using the bill-split signal).
The Collapse Zone: It identifies "Equilibrium Breakdown" points—parameter sets where the cost of embarrassment is so low that the man never bothers to screen, rendering the bill-split signal irrelevant.
Why it is useful: It proves the robustness of the paper’s thesis. It shows that the "Two-Zone" behavior (Always Propose vs. Screening) is not a mathematical fluke of specific numbers, but a fundamental feature of the model that persists across a wide variety of personality types (varying k and e).

Figure V2: Expected Utility (EU) Gain Landscape
What it shows: This 3D surface plot calculates the "Payoff Premium": EU(Signal-Optimal) - EU(Naïve Strategy).
Zone 1 (p < p*): The surface is perfectly flat at zero. Here, the "naïve" strategy (always asking) is already optimal. 
Zone 2 (p > p*): The surface rises sharply. This represents the "economic value" of the woman's signal. 
Why it is useful: It answers the "So what?" question. It quantifies the benefit of being socially observant. By showing that the gain increases as attractiveness (p) increases, it illustrates why high-status or highly attractive individuals have a higher "incentive" to look for subtle signals of disinterest to protect their utility.

Figure V3: Monte Carlo Screening Efficiency
What it shows: This figure treats the man’s decision-making as a Binary Classifier (predicting if the woman is "Interested" or "Uninterested").
F1-Score: The simulation shows the signal-optimal strategy achieves an F1 ~0.84, significantly outperforming the naïve approach (~0.72).
Precision-Recall Trade-off: It visualizes how "Embarrassment Cost" acts as a tuning knob—high costs force the man to have high "Precision" (he only asks when he’s certain), while low costs allow for high "Recall" (he asks everyone to avoid missing a chance). 
Why it is useful? This is the "stress test: by drawing 10,000 dates from a Beta distribution (a realistic bell curve of attractiveness), we confirm that the mathematical equilibrium holds up in a noisy, stochastic environment. It provides empirical-style evidence that "screening" via the bill-split is a statistically superior strategy for maximizing successful matches while minimizing social rejection.
