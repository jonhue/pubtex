---
layout: pubtex
title: PubTeX
---

# PubTeX

This is a template for publicly hosting LaTeX files with GitHub actions.

It roughly works as follows:

1. You write your latex files as you would normally
2. Whenever you push your changes to `main`, your files are compiled and pushed to the `gh-pages` branch.
3. You can now download them directly or publish the branch with GitHub Pages

You also get this nice front page for free :)

### Some examples

* [Paper](https://jonhue.github.io/pubtex/paper.pdf)
* [Slides](https://jonhue.github.io/pubtex/slides.pdf)
* [Handout](https://jonhue.github.io/pubtex/slides_handout.pdf)

### Usage

1. [Use this template](https://github.com/jonhue/pubtex/generate) (you only need to include the `main` branch)
2. List all `.tex` files you want to compile in `.github/workflows/publish.yml` under the `files` option
3. If you want to generate handouts for some Beamer slides, list those files under the `handouts` option
4. [Create SSH deploy key](https://github.com/peaceiris/actions-gh-pages#%EF%B8%8F-create-ssh-deploy-key)
5. (optional) Enable GitHub Pages for the `gh-pages` branch

### Options

| Name          | Description                                                                | Default     |
| ------------- | -------------------------------------------------------------------------- | ----------- |
| `deploy_key`  | Deploy key used to deploy to GitHub Pages                                  |             |
| `files`       | Space-separated list of files that should be compiled                      |             |
| `handouts`    | Space-separated list of Beamer files that handouts should be generated for |             |
| `publish_dir` | The directory that should be published with GitHub Pages                   | `dist`      |
| `index_page`  | Path to the Markdown file that should be the main page                     | `README.md` |
