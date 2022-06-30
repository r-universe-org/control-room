# Control room

Tools and scheduled actions (cron-jobs) to trigger actions in the r-universe system:

 - [sync.yml](.github/workflows/sync.yml) hourly cron which checks for all monorepos in [r-universe](https://github.com/r-universe/) if any of the submodules needs to be updated.
 - [rebuilds.yml](.github/workflows/rebuilds.yml) nightly cron which triggers retries of failed actions, and montly full rebuilds for all packages on r-universe.
 - [setup.yml](.github/workflows/setup.yml) on demand + nightly job which created and deletes [r-universe monorepos](https://github.com/r-universe) based changes on CRAN and app (un)installations.
 - [rforge.yml](.github/workflows/rforge.yml) cron job to sync the [r-forge mirror](https://github.com/r-forge)

