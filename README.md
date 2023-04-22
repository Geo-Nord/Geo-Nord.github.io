# GeoNord.github.io

## Getting Started

- Prerequisite: install hugo (https://gohugo.io/getting-started/installing/) if
  you want to see and test the changes locally
- Clone repository and submodules:
  - (HTTPS) `git clone --recurse-submodules
    https://github.com/GeoNord/GeoNord.github.io.git`
  - (SSH) `git clone --recurse-submodules
    git@github.com:GeoNord/GeoNord.github.io.git`

## Template Architecture

The theme used is the [Syna Theme](https://syna.okkur.org/docs). The theme is a
git submodule cloned under `themes/syna`.

The file `config.toml` contains the main configurations (URL, title, favicon,
colors, menus) for the website.

The folder `content` is composed of different subfolders, each one of these
subfolders corresponds to a page of the website. A page is made up of fragments;
each fragment is defined by a Markdown file (refer to `content` for examples),
note that the `weight` attribute determines the order in which the fragments are
arranged. See the [Syna Theme
Documentation](https://about.okkur.org/syna/fragments/) for the different
fragments that are available. Fragments placed in the `_global` subfolder are
applied to every page of the website (header, footer, menu, etc.), the `_index`
subfolder corresponds to the Home page.

The folder `resources` is populated by the `hugo server -D` command when locally
building and viewing the website during development.

The folder `static` contains the favicon, images, and some custom CSS for the
website.


## Website Deployment

* Clone this repository
* Make your edits in the template files
* View your edits locally with `hugo server -D`
* Once satisfied, commit and push your edits to GitHub
* At every new commit pushed to the `main` branch on GitHub, a GitHub Action is
  triggered to rebuild and redeploy the website automatically (no need to run
  the `hugo` command yourself or create a `public` folder anymore)
