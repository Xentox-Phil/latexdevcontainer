# LatexDevContainer

A development container template for LaTeX projects using Docker and VSCode. This template provides a preconfigured environment for editing and compiling LaTeX documents all within a containerized setup.

## Features

- **Dockerized Environment**: Build and run LaTeX projects inside a container with all necessary dependencies preinstalled.
- **VSCode Integration**: Preconfigured for use with VSCode, including essential LaTeX and Git extensions.
- **Multiple LaTeX Compilation Tools**: Supports several LaTeX compilers like `latexmk`, `pdflatex`, `xelatex`, `lualatex`, and more.
- **Custom LaTeX Recipes**: Includes common recipes for compiling LaTeX documents and generating bibliographies and glossaries.
- **Git Integration**: Seamlessly integrates with Git for version control, supporting GitHub/GitLab workflows.
- **SSH Support**: SSH keys are mounted to the container for secure access to repositories.

## Requirements

To use this development container, you must have the following installed:

- **Docker**: A containerization platform to build and run containers.
  - Install Docker from [here](https://www.docker.com/get-started).
  
- **VSCode**: A lightweight code editor that supports the development container setup.
  - Install VSCode from [here](https://code.visualstudio.com/).

- **VSCode Remote - Containers Extension**: This extension enables VSCode to connect to and develop within a containerized environment.
  - Install the "Remote - Containers" extension from the [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers).

## Setup

1. Clone this repository to your local machine:

2. Open the project in VSCode:
    - Launch VSCode and open the cloned project folder.
    - VSCode should automatically detect the `devcontainer.json` file and prompt you to reopen the folder in a container. Click **Reopen in Container**.

3. Once inside the container, you’re ready to start working on your LaTeX documents.

### If the container doesn't open automatically

If VSCode doesn't prompt you to open the project in the container automatically, you can manually trigger the process by using the command palette:

1. Open the command palette in VSCode by pressing `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS).
2. Search for and select **Remote-Containers: Reopen in Container**.
3. VSCode will build and start the container, and you'll be inside the containerized development environment.

### Available LaTeX Compilers & Recipes

This template provides the following tools and recipes for compiling LaTeX documents:

- **Tools**:
  - `latexmk`: The default tool for compiling LaTeX projects.
  - `pdflatex`, `xelatex`, `lualatex`: Different LaTeX compilers for diverse document needs.
  - `bibtex`: For generating bibliographies.
  - `knitr`, `Weave`, and `pweave`: For compiling Rnw, Jnw, and Pnw files.
  - `tectonic`: A modern and fast LaTeX engine.
  - `makeglossaries`: For generating glossaries in LaTeX.

- **Recipes**:
  - `latexmk`: Compiles LaTeX documents using `latexmk`.
  - `pdflatex -> bibtex -> pdflatex * 2`: Common compilation sequence for documents with references.
  - `Compile Rnw files`, `Compile Jnw files`, `Compile Pnw files`: Compile R, Julia, or Python-notebook-based LaTeX documents.
  - `Build Glossary`: Compile and create glossaries from LaTeX files.
  
## Notes

- The container uses the `latest texlive` Docker image to provide a full LaTeX environment.


## Troubleshooting

- If you encounter issues with Docker or VSCode integration, try restarting the container. In order to debug issues with the LaTeX Workshop extension, you can open the terminal, navigate to the Output tab, and select LaTeX Workshop from the dropdown to view relevant logs.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
