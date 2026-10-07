Finite-Noise Dynamics in a Quantum Graph Neural Network for Molecular Property Prediction
Goal
This notebook tests one specific hypothesis:

Intermediate physical quantum noise can reduce overfitting and improve test generalization before high noise causes trainability collapse.

The experiment uses the QM9 molecular benchmark, with the HOMO–LUMO energy gap (Δε) as the regression target.

The notebook deliberately uses a small, reproducible experiment first. It does not claim quantum advantage or molecular discovery. It tests the finite-noise phenomenon only.

What the experiment measures
For several physical depolarizing-noise rates β, the notebook measures:

Training MSE
Test MSE
Generalization gap = Test MSE − Training MSE
Gradient norm with respect to trainable quantum parameters
Effective model complexity using a local Jacobian/hat-matrix estimate
The quantum circuit is graph-aware: molecular heavy atoms are mapped to qubits and CNOT–RZ–CNOT interaction blocks are created from the molecular bonds.

Important: The first run is intentionally small so that it can run in Google Colab. After the pipeline works, increase the sample sizes and repetitions for publication-quality experiments.
