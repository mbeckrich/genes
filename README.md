# Genes

### A personal website for family history and stories

## How it works
This repository makes use of [Hugo's templating logic](/themes/beth/layouts/partials/main-records.html) to build out a personal family history website. It uses an [Ahnentafel-like](https://www.tamurajones.net/AhnenChaos.xhtml) ID system to identify family members in a JSON file (see [Using the Site](#using-the-site) for details). This allows bundling people together through Hugo's [front matter](https://gohugo.io/content-management/front-matter/), creating family units that exist outside the traditional nuclear family.

[//]: # "Screenshot of front matter example"

## How it's made

The site is made using [Hugo](https://gohugo.io), [Volta](https://volta.sh), [Stylelint](https://stylelint.io) (refer to [package.json](package.json) for custom rules and extends), [watchexec](https://github.com/watchexec/watchexec), and [lightningcss](https://github.com/parcel-bundler/lightningcss).

To replicate the development environment:

1. Make sure you have a package manager such as [homebrew](https://brew.sh) or [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget).
2. From the terminal[^1], confirm a recent version of git is installed by typing `git -v`. If `git -v` does not return a positive result, refer to [Github's installation instructions](https://github.com/git-guides/install-git) (or [git-scm](http://git-scm.com) for much more info about git).
3. Use your terminal and package manager to install Hugo, Volta, and Watchexec
4. Clone this repository. Change directory to the cloned repository:(e.g.,`cd /path/to/cloned/genes`)
5. From inside the `genes` folder, run `volta install node` and `volta install npm`. Then, run `npm install` to install dependencies.

## Using the site

After setting up the site, some initial data creation and wrangling currently is required.

This site is designed to use [Gramps](https://gramps-project.org) and a [GEDCOM](https://www.gedcom.org) file of family data. After installing Gramps and importing a GEDCOM file, create an HTML report using Gramps: `Reports` -> `Text Reports` -> `Detailed Ancestor Report`. Underneath the [front matter](https://gohugo.io/content-management/front-matter) in the site's [`DAR.md`](content/reference-lists/DAR.md) file, paste the contents of the file exported from Gramps.

Back at the terminal and in your site's directory, run `hugo`. This will create the file `index.json` in [public/reference-lists/dar](public/reference-lists/dar). Copy the data from this file and paste it into the file [`data/DAR.json`](data/dar.json).

## Things to know

### CSS

+ The site css currently requires a polyfill for the oklch color space it uses. If editing the site css, some extra steps will need to be taken.
    + One method is to use the tools lightning-css and Watchexec with the script in the repository's package.json file. Move to the site directory in your terminal and run `watchexec -w "./themes/beth/assets/scss/styles/" npm run build`. This bundles the .scss files into a .css file and then uses lightning-css to correct for the oklch usage.

[^1]: https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line
