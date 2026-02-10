# Documentation Website (MkDocs + GitHub Pages)

For any academic or research project, **documenting the code is essential**. Clear documentation enables reproducibility, supports collaboration, and ensures that scientific ideas remain understandable beyond the original development phase.

This repository provides a **simple, reproducible documentation workflow** that connects local note-taking with automatic website deployment.

How to use this template
1.	Write your documentation
	- Place all documentation files inside the `docs/` directory.
	- Ensure `docs/mkdocs.yml` exists and is correctly configured.
2.	Use the provided workflow
	- The workflow file (in `.github/workflows/`) builds the site using MkDocs and deploys it to GitHub Pages on every push to main.
3.	Enable GitHub Pages
	- Go to `Settings` → `Pages` in your GitHub repository.
	- Under Source, select: `Deploy from a GitHub Actions workflow`
	- Save the settings.
4.	Deploy
	- Push changes to the main branch.
	- GitHub Actions will automatically build and publish your documentation website.

## Result

Your documentation will be available at: `https://<username>.github.io/<repository-name>/`

No manual deployment steps are required after setup.


## Writing Documentation

All documentation is written in the `docs/` folder.

- The repository is preconfigured for **Obsidian**.
- Open the repository directly in Obsidian to start writing.
- Write documentation as plain Markdown files.
- Use Obsidian for structured notes, links, and incremental writing.

## Publishing Documentation

The documentation website is built using **MkDocs** and deployed automatically to **GitHub Pages**.

When you:
- add a new chapter
- add a new lesson or page
- reorganize content

you must update `mkdocs.yml` to include the new files in the navigation. This step is required for the content to appear on the rendered website.

## Workflow Summary

- Write notes in `docs/` using Obsidian
- Commit changes to the repository
- Update `mkdocs.yml` when adding new pages
- Push to `main`
- GitHub Actions builds and publishes the documentation website automatically
