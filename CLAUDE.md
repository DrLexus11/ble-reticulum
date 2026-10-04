# DrLexus11 fork of ble-reticulum -- QuakeMesh / IMPR-RAD

This is our fork of torlando-tech/ble-reticulum (the BLE interface), part of the Python Reticulum stack that
Columba (`~/projects/columba`, `rns-backend-py/build.gradle.kts`) installs by
commit. The rules of the main project apply here; read
`~/projects/microReticulum_Firmware/CLAUDE.md` and its
`docs/TAKDeliveryPlan.md`, section "Direction after PR F", before changing
anything.

## Rules

- **DrLexus11 remotes only.** `origin` is this fork. Never add the original
  repository (torlando-tech or markqvist) as a remote, and never open a pull
  request or push a branch to it. `gh repo set-default` is pinned to
  DrLexus11. Compare with the originals in a scratch clone outside this
  repository.
- **Columba pins a commit, on a branch.** Columba pins `07d9413`, on `main`. Do not rewrite or delete that
  branch: a pinned commit that disappears breaks Columba's build.
- **Protocol changes go in lockstep.** The same protocol runs in three
  implementations: C++ firmware (`microReticulum`), Kotlin (`reticulum-kt`, in
  Columba) and Python (this stack). A wire change is versioned, made in all
  three, and pinned by a shared fixture -- never made here alone.
- **Branch and pull request** on this fork; never commit to the default branch
  directly.
