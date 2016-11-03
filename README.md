[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# GitHub Pages Deployment Guide

## Objectives

By the end of this, developers should be able to:

-   Deploy a client application to GitHub Pages

## Deployment Steps

These steps assume that work has been done on a `master` branch and is ready to
be deployed.

1.  Begin by creating a new branch called `gh-pages`

    ```sh
    git branch gh-pages
    ```

1.  Ensure you are on your master branch.

    ```sh
    git checkout master
    ```

1.  And check that all updates on your `master` branch are committed and pushed
 up to GitHub.

The last thing we're going to do is **deploy** (i.e. host) this web page through
a service that GitHub provides called GitHub pages. To do this, go through the
following steps.

1.  Move to the `gh-pages` branch that you created earlier.

    ```sh
    git checkout gh-pages
    ```

1.  Merge master `master` into `gh-pages`

    ```sh
    git merge master
    ```

1.  In your `.gitignore` file, comment out the lines `*bundle.js` and
`dependencies.js` so git no longer ignores those files e.g., `# *bundle.js`.
Alternatively you can remove those lines altogether.

  > This tells Git to no longer ignore those files so Git can track them.

1.  Next run `grunt build`.

  > This bundles your code and creates the bundle.js and dependencies.js files
  > that you just un-ignored.

1.  Now `add` and `commit` your code and run `git push origin gh-pages`

  > This will push your code to GitHub Pages

1.  Go to the URL `<your-username>.github.io/<repository-name>` in your browser, you
should be able to see your page! If you don't, be patient. Sometimes, it takes
up to 15 minutes for GH Pages to display your deployed page.

  > As a general rule, the formula for a GitHub Pages URL is:
  >`<your-username>.github.io/<repository-name/path-to-location-of-index.html>`

## Wokflow rules

1. NEVER work on the `master` branch.
2. Merge `feature` branch onto `master` when your feature is done.
3. Make `gh-pages` branch from `master`.
4. Edit `.gitignore` ONLY on `gh-pages`.
5. NEVER merge `gh-pages` into `master`.

## Additional Resources

-   [GitHub Pages](https://pages.github.com/)

## [License](LICENSE)

Source code distributed under the MIT license. Text and other assets copyright
General Assembly, Inc., all rights reserved.
