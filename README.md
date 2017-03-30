[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# GitHub Pages Deployment Guide

## Objectives

By the end of this, developers should be able to:

-   Deploy a client application to GitHub Pages.

## Deployment Steps

If your work has been merged to a `master` branch, it is ready to be deployed.

From the `master` branch, and at the root of your project, run `grunt deploy`.
If the working directory isn't clean, the deploy task will exit and show you
the output of the `git status` command. To fix this, add and commit changes
you wish to keep on the appropriate branch (most likely **not** `master`).

Go to the URL `<your-username>.github.io/<repository-name>` in your browser,
you should be able to see your page! If you don't, be patient. Sometimes, it
takes up to 15 minutes for GH Pages to display your deployed page.

As a general rule, the formula for a GitHub Pages URL is:
`<your-username>.github.io/<repository-name>/path-to-location-of-index.html>`

## Workflow Rules

1. Deploy early and often.
1. NEVER work on the `master` branch.
1. Merge `feature` branch onto `master` when your feature is done.
1. `git push origin` every time you merge to `master`.
1. `grunt deploy` every time you merge to `master`.
1. Inspect your deployment in the browser.
1. NEVER merge `gh-pages` into `master`.

## Deliverable

- After deploying your site, paste the URL into the `url.md` file and open a Pull Request.

## Deployment Commandments

- `gh-pages` is not a replacement for grunt serve.

- `gh-pages` is a production environment.

- **NEVER** test code in production environments.

- **ONLY** deploy when code is verified as working.

## Additional Resources

-   [GitHub Pages](https://pages.github.com/)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
