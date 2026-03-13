# Extraction Specification

This repository uses the standard canonical-lane extraction pipeline.

Required constants:

- `kappa_holomorphic` from `c_holomorphic_raw * regularity_gain_raw - e_holomorphic_raw`
- `sigma_local` from `local_floor_raw - ramification_loss_raw - restart_loss_raw`
- `kappa_compact` from `1.0 / (1.0 + delta_comp_sup_raw)`
- `rho_rigidity` from `rho_rigidity_raw`
- `regularity_transfer` from `c_transfer_raw * transfer_gain_raw - e_transfer_raw`
- `eps_coh` from `eps_coh_raw`
- stitch constant `sigma_star_can` from `sigma_star_can_raw`

Pipeline order:

1. `scripts/extract_constants.py`
2. `scripts/promote_constants.py`
3. `scripts/ah_closure_guard.py`
4. `scripts/update_manifest.py`
5. `scripts/release_gate.py --mode fully_extracted`
