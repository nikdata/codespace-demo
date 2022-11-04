# GitHub Codespaces & RStudio

## Introduction

The goal of this repo is to document a minimum viable example of how to leverage RStudio within GitHub Codespaces. I was inspired to make this repo based on a similar [repo](https://github.com/revodavid/devcontainers-rstudio) by [David Smith](https://github.com/revodavid) from Microsoft. In David's repo, the example he provides is quite detailed and my aim with this repo is to provide a more simpler example.

Note that GitHub Codespaces is only available to the following groups:
- Enterprise customers (GitHub Enterprise)
- Teams (GitHub Teams)
- Individuals with invites

I am fortunate enough to have acces to GitHub Codespaces.

## Background

In order to make use of GitHub Codespaces, you'll want to familiarize yourself with the concept of [development containers](https://code.visualstudio.com/docs/devcontainers/containers). Succinctly, development containers are basically Docker containers/images. Perhaps the noticeable differnce is the need to have a `.devcontainer` folder. This folder would typically contain the Dockerfile and another file called `devcontainer.json` which describes some of the settings, extensions, etc. that can be used by VSCode. With that said, to *effectively* use GitHub Codespaces, you'll want to have VSCode installed on your local machine (or be familiar with it if using in a browser interface).

## ELI5 of How It Works

The easiest way for me to explain how all this works:

- Define a Dockerfile (you can use the one found in this repo)
- create the `.devcontainer` folder and the `devcontainer.json` file
  - you can copy the bare minmimum I have
- Commit and push to your repo and launch codespaces using the big GREEN button that says CODE.

If your codespace builds successfully, then you should see a VSCode interface through your browser. If you're using the same example I have, then you'll see at least 1 active port under the PORTS tab. Within this tab, you should RStudio listed and you can click on the globe icon to launch it.

One thing to keep in mind is that this approach doesn't always work with great success (as noted in David's repo). I suspect that as GitHub Codespaces continues to mature, the 'quirks' will be identified and resolved.