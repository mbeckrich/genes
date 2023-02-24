# Genes

### A personal website for family history and stories

###### Rough draft t_t

# How it works

# How it's made

- The site is made using [Hugo](gohugo.io/), [Volta](https://volta.sh/) (to
  install Node and NPM), [Stylelint](stylelint.io/) (refer to package.json for
  custom rules and extends), [Watchexec](https://github.com/watchexec/watchexec)
  and [lightningcss](https://github.com/parcel-bundler/lightningcss)
- To replicate the development environment:

1) From the terminal[^1] (e.g., Windows Terminal, Kitty, macOS's Terminal),
   confirm a recent version of git is installed (`git -v`). Refer
   to [git-scm](git-scm.com/) for additional git setup info, if necessary. If
   git is not installed, refer to to git-scm
   or [Github's install directions](https://github.com/git-guides/install-git).
2) Use a package manager such as [homebrew](https://brew.sh/)
   or [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)
2) With the terminal and a package manager, install Hugo, Volta, and Watchexec
3) Clone the repository. Change directory to the cloned repository: (
   e.g.,`cd genes`).
4) Run `volta install node` and `volta install npm`. Then, run `npm install` to
   install dependencies.

# Things to know

### CSS

- The site css currently requires a polyfill for the oklch color space it uses.
  If editing the site css, some extra steps will need to be taken.
    - One method is to use the tools lightning-css and Watchexec with the script
      in the repository's package.json file. In a terminal,
      run `watchexec -w "./themes/beth/assets/scss/styles/" npm run build`. This
      bundles the .scss files into a .css file and then uses lightning-css to
      correct for the oklch usage.

[^1]: https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line
