[![gh-pages](https://github.com/FmTod/satis/actions/workflows/pages.yml/badge.svg)](https://github.com/FmTod/satis/actions/workflows/pages.yml)
[![pages-build-deployment](https://github.com/FmTod/satis/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/FmTod/satis/actions/workflows/pages/pages-build-deployment)

----

*This repository is intended for internal usage only.*
 
----

## How does it work?

#### Build the repository

1. `composer init`
2. `composer require composer/satis`
3. Generate `satis.json`. See [Satis Setup](https://getcomposer.org/doc/articles/handling-private-packages.md#setup) for syntax

#### GitHub Actions

**`pages.yml`**

`.github/workflows/pages.yml` has three simple steps:
1. Install composer dependencies (Satis)
2. Build Satis using `satis.json` and write to `public`
3. Deploy `public` to `gh-pages` branch

The workflow runs on pushes to the `main` branch and also nightly at midnight in order to
ensure dependencies are kept up to date.

