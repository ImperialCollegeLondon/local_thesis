# 📖 Thesis template for Imperial College London designed to work in VSCode

The `.devcontainer` contains the config files to run the docker image and install some helpful extensions to aid in `LaTeX` use in VSCode.

## Pre-requisites
Ensure that the `Dev Containers` extension is installed in VSCode

## Building your PDF
The normal `build` command in VSCode would now build your project into a PDF. By default, the shortcut for this is `Ctrl-Alt-B`

## View your PDF
The view shortcut is `Ctrl-Alt-V`.

## Github Actions
On commit - a GitHub Action will also compile the PDF and store it as an artifact of the compilation process.
To view the compiled PDF, go to the `Actions` tab, select the latest run and you should see an artifact of the build process called `PDF`

# Limitations
At the moment, the main entry is hardcoded into the GitHub Actions to be `main.tex`. This limitation does not exist in the local build process.