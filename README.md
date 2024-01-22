# Cellular-Automaton-Simulation
Cellular Automaton computational model used to simulate diffusion of gas

One of the principles of computational physics is that we can often see universal behavior from simple microsocopic rules. We are going to start by writing down a simple cellular automata for the diffusion of gas in a room. From this cellular automata we are going to measure entropy as a function of time.

In our automata, we have two colors (black and white). We  treat the black color as the gas and the white color as empty space.
We will start with the right half of the system filled with gas and the left half empty (i.e. the right half is black and the left half is white).

The rule then for a single step is:

randomly select a pair of nearest-neighbors sites.

A nearest-neighbor site is one which is up, down, left, or right.

swap those two sites (even if they are the same color).

Entropy is essentially a measure of how “random” a state is. The more random a state, the more entropy it should have. A state where the “gas” is randomly placed is going to have the highest entropy. There are various ways then of measuring entropy. One approach is to take a configuration and ask how easy it is to compress it. If it compresses efficiently then it has low entropy. If it’s completely “random” then it’s hard to compress and has high entropy. After we’ve produced configurations (in memory or as a file), we can load the configuration using python, compress the state, and measure its size as a function of time. This will be our heurestic for the entropy of the state (if a state is very disordered, it should be hard to describe compactly).
