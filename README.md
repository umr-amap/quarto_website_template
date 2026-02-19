# Publish Jupyter Notebooks or R Markdown to GitHub Pages

This guide walks you step-by-step through publishing a Jupyter Notebook (.ipynb)
and/or R Markdown (.Rmd) project to GitHub Pages using Quarto.

::: callout-note
To follow this guide, we assume that you already have: 1) `git` installed and set up on your computer, 2)
a github account, 3) you known how to edit jupyter notebooks, Markdown and/or RMarkdown files.
:::

## Install Quarto

[Quarto](https://quarto.org/) is an open-source scientific and technical publishing system that can render:

- [Jupyter Notebooks](https://jupyter.org/) (.ipynb)
- [R Markdown](https://rmarkdown.rstudio.com/) (.Rmd)
- [Markdown](https://www.markdownguide.org/)(.md or .qmd)

from multiple languages like Python, R or Julia into websites, PDFs, blogs, and more.

Please follow the [guidelines](https://quarto.org/docs/get-started/) to install Quarto and the extension for your text editor (not necessary but better user experience).

## Create a minmal website using this template

We will create a new project named `my_awesome_project`. Consider that this can be anything that you want to share with your colleagues, tutors, students, etc...

### Fork this repository into your github

On this repository, click on the `Fork` button on the top right corner of the page.

This will ask you to name a new project that is gonna be a fork of this one, hosted into your github account.

**Untick** the `Copy the main branch only` button, as you want to get all branches. Finaly, click on the `Create fork` button.

Great ! You now have your own quarto website project hosted on your account.

### Download this new project locally

This is the usual `git` workflow:

```bash
git clone https://github.com/YOURUSERNAME/my_awesome_project.git`
```

or use Github Desktop or VS Code or etc... to download the project.

### Enable GitHub Pages

We now need to tell `GitHub` that this project is gonna host a website.

Inside your new project <https://github.com/YOURUSERNAME/my_awesome_project.git> :

- Click on `Settings`
- Click on `Pages` on the left sidebar
- Under Build and deployment:
  - Source: Deploy from a branch
  - Branch: `gh-pages` branch
- Click `Save`

Congrats, you now have a website hosted on `GitHub` pages. Wait 2-3 minutes and check at `https://YOURUSERNAME.github.io/my_awesome_project/`

## Publish your changes

Detailed instructions on how to render the website can be found [here](https://quarto.org/docs/publishing/github-pages.html).

You now have a new project:

- hosted on your github account
- already configured to generate a quarto website
- `github pages` is already configured to host the website that quarto will build on the `gh-pages` branch.

You can now add new content and organize it the way you want.

You now have 2 magic commands that you need to know:

To render the website on your computer, you need to run:

```bash
quarto render
```

::: callout-note
Please note that the `Jupyter_example.ipnb` will fail to render as the python kernel selected will not exist on your local environment. Just change it's value to standard `python3` if youhave `numpy` and `matplotlib` already installed.
:::

To publish your website, you need to run:

```bash
quarto publish gh-pages
```

You IDE also probably has some shortcuts for these commands.

and "voilà", your website is now ready at : `https://YOURUSERNAME.github.io/my_awesome_project/`
