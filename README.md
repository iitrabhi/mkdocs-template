# Building the Website with MkDocs for GitHub Pages

When using MkDocs to build a website, especially for hosting on GitHub Pages, it's important to understand the directory structure and how to configure the output correctly. This section explains the process and provides a command to automate the setup.

## Directory Structure
- **Source Files:** By default, MkDocs uses a directory named `docs` for documentation source files.
- **Build Output:** The generated static site files are usually placed in a directory named `site`.

However, for GitHub Pages, there's a specific requirement:
- **GitHub Pages Requirement:** GitHub Pages needs a `docs` folder at the repository's root to serve the website.

To accommodate this, our MkDocs content is stored in a separate `mkdocs` folder, and we use a special command to restructure the output to meet GitHub Pages' requirements.

### Automated Build Command
The following command is designed to streamline the build process and ensure compatibility with GitHub Pages:

```bash
rm -rf ../docs && mkdocs build && mv site ../docs
```

Here's what each part of the command does:

1. `rm -rf ../docs`: Removes the existing `docs` directory at the parent path to clear any previous build outputs.
2. `mkdocs build`: Builds the static site, outputting the files into the `site` directory.
3. `mv site ../docs`: Moves the newly generated `site` directory to replace the deleted `docs` directory at the parent path.

This process is crucial for GitHub Pages deployments, ensuring that the `docs` folder containing the site content is correctly placed at the repository's root. This setup is particularly useful when your Markdown documentation is maintained in a separate `mkdocs` folder.

## Handling Images (Logo and Favicon)
MkDocs expects certain assets like the logo and favicon to be located in a specific directory:

- **Location:** These files should be placed under the `img` folder within the `docs` directory.

Ensure that your logo and favicon are correctly placed in this directory for MkDocs to reference them properly on your website.
