# HNN-for-Maxcut-using-AER
A fully digital solution for the NP-hard MaxCut problem using a Hopfield Neural Network (HNN) on FPGA. Integrated a FIFO-based Address Event Representation (AER) mechanism to enhance event-driven updates within the network. This approach demonstrates efficient parallel computation and energy-aware neural processing on hardware.

A Hopfield network consists of a single layer of interconnected neurons. Each neuron is connected to other neurons, but not to itself. Neurons in a Hopfield network typically have binary states (e.g., -1 and 1, or 0 and 1), which change according to specific rules to minimize the network's energy function.

The network operates based on an energy function, and it evolves towards stable states (local minima of the energy function). These stable states correspond to patterns that the network has learned.

Hopfield networks can recall an entire pattern from partial or noisy inputs, making them ideal for tasks like image reconstruction or pattern recognition

The Max-Cut problem involves dividing the vertices of a graph into two subsets such that the total weight of the edges between the two subsets is maximized. In simpler terms, the goal is to "cut" the graph in a way that maximizes the sum of the edge weights across the cut.
 
What maximises the cut of a node? If a node in state S0 has more neighbouring node as S1, it will have maximum number of cuts. Similarly a node with most neighbouring nodes as S0 will have maxcut if it is S1. So basically a node will have maximum cut value if it is in opposite state to majority of neurons connected to it. So we should maximise the xor value of connected neurons to maximise cut.

So the energy function to minimise is:


<img width="261" height="102" alt="image" src="https://github.com/user-attachments/assets/17a1a9a2-8d0d-4d15-88d6-a57f513c975b" />
