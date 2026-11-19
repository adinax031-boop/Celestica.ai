# Convergence exhibition experiment protocol

Before running the exhibit-scale comparison, freeze five seeds (917–921), 44 scheduled updates per task and batch size 24. Compare sequential SGD, 8/24 replay, and risk-gated replay with rollback. The first 16 fresh draws are shared for replay variants. Plain SGD trains on all 24 fresh draws. Count scheduled updates, examples, replayed examples, diagnostic gradient/forward examples and rejected updates. Report that monitoring costs differ. Models start from the same parameters for each matched seed.

## Memory

Use scikit-learn's UCI handwritten-digits subset, five class-incremental tasks with two successive digit classes and a shared output head. Fix per-class disjoint partitions before training. Train, replay, policy monitor, risk diagnostics and final test have disjoint examples. The policy sees short-horizon old-monitor gradients, never the held-out risk or test labels. Predict increase in old loss from the gradient dot product before the step. Score average precision for a >0.007 mean old-loss increase under a virtual new-only step. Use per-policy means and paired seed differences. This exhibit mechanism is inspired by FRI/VAC. The archived FRI CNN and its governors use distinct protocols.

## Integrated Memory × Axiom

Generate disjoint seeded train, replay, monitor, risk and test examples for nominal and degraded spacecraft environments. Use time-step physics to label feasibility. The MLP predicts those synthetic scenario labels. Hold all settings fixed across conditions. Accuracy does not establish validity beyond the modeled scenarios. It is an engineering feasibility predictor, not a design certifier.

## Axiom

The predeclared stress bench is 160 deterministic cases (seed 7264), alternating normal and degraded. Compare one fixed design, analytic screen with independent timestep verification, and exhaustively applied timestep verification. Compare feasibility, minimum mass agreement, false accepted designs, and paired gains/losses. Design universe is 64 synthetic catalog pairs. Assume circular orbit, cylindrical shadow, constant electrical load, simplified array derating and battery efficiency, four repeated orbits beginning fully charged, and finite mass ceiling. No launch, lifetime or flight-readiness claim. CPU-only budget, ₹0 additional cloud, API or hardware spend.
