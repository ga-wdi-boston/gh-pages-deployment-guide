[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# GitHub Pages Deployment Guide

## Objectives

By the end of this, developers should be able to:

-   Deploy a client application to GitHub Pages

## Deployment Steps

To start, indentify one member of your squad to be the 'project lead'. This
person will create three new branches: `gh-pages`, `css`, and `html`; **CREATE
THESE BRANCHES FROM THE MASTER BRANCH**. The 'project lead' will be the only
squad member to code during the lab, everyone else will advise them what to
code.

Then, check out the `html` branch and begin working there.

1.  `grunt serve`

  > `grunt serve` spins up a local server via Grunt. This local server allows
  > us to work in a 'Development' environment to replicate what the 'Deployed'
  > environment will  be like.

Once you finish writing your HTML, add the changes you've made to `index.html`
and make a commit. Then, run the following commands:

1.  `git checkout master`

  > Move to the master branch

1.  `git merge html`

  > Add the changes on the `html` branch to the `master` branch. Depending on
  > what you've done, you may get a warning about a 'merge conflict' - if that
  > happens, flag down one of the consultants.

1.  `git push origin master`

  > Push your updated `master` branch up to GitHub

At this point, the `master` branch on your GitHub fork should include your new
HTML page.

Now checkout the `css` branch that you created earlier and style your site using
the `main.css` file in the `assets/styles/` directory as follows. Don't worry
about creating a link tag as the two script tags in the head of `index.html`
take care of that for you.

-   Make the recipe title ("The Best Chocolate Chip Cookies") match [this shade
of
brown](http://en.wikipedia.org/wiki/Shades_of_brown#Chestnut), and make it
larger than the rest of the text on the page.
-   The font for the whole page should be 'arial', except for the recipe title
(which should be in 'cursive').
-   All text in the page should be centered.
-   In the ingredients list, give each ingredient a unique color; any time that
ingredient appears in the recipe, make it that same color.
-   And feel free to experiment and add whatever else you want!

Once you are finished styling your site, commit your changes and merge it with
master like you did with your html branch

1.  `git checkout master`

1.  `git merge css`

1.  `git push origin master`

The last thing we're going to do is **deploy** (i.e. host) this web page through
a service that GitHub provides called GitHub pages. To do this, go through the
following steps.

1.  `git checkout gh-pages`

  > Move to the `gh-pages` branch that you created earlier.

1.  `git merge master`

  > Add the new changes that have been made on `master` to the `gh-pages`
  > branch on your local repo.

1.  In your `.gitignore` file, comment out the lines `*bundle.js` and
`vendor.js` so git no longer ignores those files e.g., `# *bundle.js`.
Alternatively you can remove those lines altogether.

  > This tells Git to no longer ignore those files so Git can track them.

1.  Next run `grunt build`.

  > This bundles your code and creates the bundle.js and vendor.bundle.js files
  > that you just un-ignored.

1.  Now add and commit your code and run `git push origin gh-pages`

  > This will push your code to github pages!

This process should add your HTML and CSS code to the `gh-pages` branch of your
GitHub repo. Now, GitHub can work its magic and make that page visible on the
web. If you go to the URL `yourUsername.github.io/html-css/` in your browser,
you should be able to see your page!

  > As a general rule, the formula for a GitHub Pages URL is
  > `your-username.github.io/repository-name/path-to-location-of-index.html`


## Additional Resources

- [GitHub Pages](https://pages.github.com/)

## [License](LICENSE)

Source code distributed under the MIT license. Text and other assets copyright
General Assembly, Inc., all rights reserved.
