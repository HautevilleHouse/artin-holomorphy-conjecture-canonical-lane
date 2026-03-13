# EG2 Public Note

The `EG2` package establishes admissible capture across deformation and restart.

Raw theorem constant:

`sigma_local^(raw) := local_floor_raw - ramification_loss_raw - restart_loss_raw`.

Closure criterion:

- the admissible defect ledger remains above the declared capture floor,
- restart losses are explicitly budgeted,
- the canonical transport remains inside the admissible tube.

Main interpretation: the tracked local-factor defect does not consume the full closure budget.
