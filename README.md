# jail.nix mirror

Read-only mirror of [jail.nix](https://sr.ht/~alexdavid/jail.nix/) by
~alexdavid (GPL-3.0), kept so Nix flakes can fetch it from GitHub instead of
hitting sourcehut on every evaluation. Four times a day
`.github/workflows/mirror.yml` compares upstream's branches and tags with this
repository's. When one moved, it overwrites them from upstream and then runs
upstream's own test suite on the new `main`; a failing suite fails that run, and
the mirror keeps the new refs. A ref deleted upstream stays here. Nothing is
edited by hand, and this default branch, `gh-mirror-meta`, holds only this
README and the workflow. Report issues upstream, not here.
