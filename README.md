# ISAAC data site

**Live site:** https://kevinnavarreteparra.github.io/isaac_data/

## R package management (renv)

Packages are pinned in `renv.lock`. Github restores from it automatically, no need to touch it unless you add a package.

- Restore pinned packages locally:
  ```r
  renv::restore()
  ```
- Add a new package:
  ```r
  install.packages("pkgname")
  renv::snapshot()
  ```
  then commit the updated `renv.lock`.
- R version is pinned separately in `.github/workflows/publish.yml` (`r-version`).

This initially feels complicated, but it makes the site easier to maintain and more stable in the long run.
