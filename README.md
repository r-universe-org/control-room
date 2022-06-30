# Control room

Tools and scheduled actions (cron-jobs) to trigger global/meta operations in the r-universe platform. Each of these can also be triggered manually with a dispatch event.

## Sync universes

[![sync badge](https://github.com/r-universe-org/control-room/actions/workflows/sync.yml/badge.svg)](https://github.com/r-universe-org/control-room/actions/workflows/sync.yml)

Action source: https://github.com/r-universe-org/sync

Hourly cronjob which checks for all monorepos in [r-universe](https://github.com/r-universe/) if there are any updates in the registry or R packages. If any of the submodules needs to be updated, it triggers a dispatch action in the respective monorepo.

## Rebuilds

[![rebuilds badge](https://github.com/r-universe-org/control-room/actions/workflows/rebuilds.yml/badge.svg)](https://github.com/r-universe-org/control-room/actions/workflows/rebuilds.yml)

Action source: https://github.com/r-universe-org/rebuilds

Nightly cron which triggers __retry failures__ for recently failed build jobs, and monthly __full rebuilds__ for all existing packages on r-universe.


## Setup universes

[![setup badge](https://github.com/r-universe-org/control-room/actions/workflows/setup.yml/badge.svg)](https://github.com/r-universe-org/control-room/actions/workflows/setup.yml)

Action source: https://github.com/r-universe-org/setup-universes

On demand + nightly job which created and deletes [r-universe monorepos](https://github.com/r-universe) based [changes on CRAN](https://github.com/r-universe-org/cran-to-git) and new (un)installations of the [github app](https://github.com/apps/r-universe).


## R-forge mirror

[![rforge badge](https://github.com/r-universe-org/control-room/actions/workflows/rforge.yml/badge.svg)](https://github.com/r-universe-org/control-room/actions/workflows/rforge.yml)

Action source: https://github.com/r-universe-org/rforge-mirror

Cron job to update the [r-forge git-to-svn](https://github.com/r-forge) mirrors.
