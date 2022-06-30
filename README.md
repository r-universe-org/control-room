# Control room

Tools and scheduled actions (cron-jobs) to trigger global/meta operations in the r-universe platform.

## Sync ![sync badge](https://github.com/r-universe-org/control-room/actions/workflows/sync.yml/badge.svg)

Action source: https://github.com/r-universe-org/sync

[sync.yml](.github/workflows/sync.yml) hourly cronjob which checks for all monorepos in [r-universe](https://github.com/r-universe/) if there are any updates in the registry or R packages.

If any of the submodules needs to be updated, it triggers a dispatch action in the respective monorepo.

## Rebuilds ![rebuilds badge](https://github.com/r-universe-org/control-room/actions/workflows/rebuilds.yml/badge.svg)

Action source: https://github.com/r-universe-org/rebuilds

[rebuilds.yml](.github/workflows/rebuilds.yml) nightly cron which triggers __retry failures__ for recently failed actions, and montly __full rebuilds__ for all packages on r-universe.


## Setup ![setup badge](https://github.com/r-universe-org/control-room/actions/workflows/setup.yml/badge.svg)

Action source: https://github.com/r-universe-org/setup-universes

[setup.yml](.github/workflows/setup.yml) on demand + nightly job which created and deletes [r-universe monorepos](https://github.com/r-universe) based changes on CRAN and app (un)installations.


## R-forge mirror ![rforge badge](https://github.com/r-universe-org/control-room/actions/workflows/rforge.yml/badge.svg)

Action source: https://github.com/r-universe-org/rforge-mirror

[rforge.yml](.github/workflows/rforge.yml) cron job to update the [r-forge git-to-svn](https://github.com/r-forge) mirrors.

