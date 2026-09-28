# NESTOR Clinical Validation Guidelines

Open-access guidelines, protocols and standard operating procedures for the validation and translation of data-driven innovative methods into clinical practice within the NESTOR research domains.

**Status: Draft — pending review.** D3.3 is scheduled for submission on **30 September 2026**, with **UM** as lead beneficiary. Authors and reviewers remain pending. This version covers embryo analysis and does not establish clinical readiness.

## Project context

This repository develops NESTOR **D3.3** in the revised deliverable list, originally **D3.4** in the proposal: “Protocols and standard operating procedures on practical recommendations covering the data driven innovative method validation into the clinical practice”, under WP3 and task T3.1. **UM is the lead beneficiary.** The revised identifier was confirmed by the project contributor. The separate interoperability report is now D3.2 in the supplied report draft (originally D3.3 in the proposal).

The scope covers personalised reproductive medicine, assisted reproductive technologies, non-invasive prenatal testing, uterine health, and AI/data-driven solutions for ART.

The separate `embryo-vision` repository contains the research implementation. This site documents a short practical workflow and a draft worked example, distinguishing verified local records from missing original training/evaluation evidence. Private data and model weights are not copied here.

## Local development

Run these commands from this repository's root with Python installed:

```console
python -m venv .venv
```

Activate the environment in Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

In Windows Command Prompt, use `.venv\Scripts\activate.bat`; on macOS/Linux, use `source .venv/bin/activate`.

```console
python -m pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000>. Stop the server with Ctrl+C.

If PowerShell activation is unavailable, invoke the environment directly:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs serve
```

Check the static site before sharing changes:

```console
mkdocs build --strict
```

Generated output is written to `site/` and ignored by Git, as is `.venv/`. MkDocs Material is the only direct dependency; it installs MkDocs and its required dependencies.

## Content organisation

- [About the guidelines](docs/index.md): purpose, proposal references and current scope.
- [Practical workflow](docs/practical-workflow.md): concise steps and a draft transferred-model checking procedure.
- [Embryo image-analysis example](docs/embryo-image-analysis.md): documented work and missing evidence.

Earlier [introduction](docs/introduction.md), [framework](docs/validation-framework/index.md), [protocol catalogue](docs/protocols/index.md), [templates](docs/templates/index.md) and [references](docs/references.md) are retained as inactive drafts. They are excluded from the built website and search index through `exclude_docs`; their content may be outdated and is not the current site structure. References for active content appear on its own pages.

Edit Markdown in `docs/`; maintain navigation in [mkdocs.yml](mkdocs.yml). Keep unknown scientific content as explicit TODOs until sourced and reviewed. Split overview pages only when sufficient content exists to justify separate pages.

## Publication and releases

Markdown is the source for the intended living, open-access website. The [Pages workflow](.github/workflows/pages.yml) builds the site with `mkdocs build --strict` and deploys only the generated `site/` directory on pushes to `main`. It can also be started manually from GitHub Actions. Inactive drafts remain excluded from the website and search index, although they remain in the repository source.

To enable publication after approval:

1. In the repository's **Settings → Pages → Build and deployment**, select **GitHub Actions** as the source.
2. Push the documentation and workflow to `main`.
3. Check the **Deploy documentation to GitHub Pages** run in the Actions tab. The deployment job provides the published URL.

Expected address: <https://georgekazakis.github.io/nestor-sops/>. Adding the workflow locally does not itself publish the site. GitHub Pages must be available for the repository's visibility and account plan. No custom domain or additional deployment secret is configured.

A reviewed deliverable release may later be archived as a fixed snapshot, including a PDF. Before that release, confirm authorship, reviewers, approval, source references and project acknowledgement details. Publishing the website does not establish formal deliverable approval.

## License

The original guidelines and documentation in this repository are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/); see [LICENSE](LICENSE). Identify NESTOR Clinical Validation Guidelines and the credited contributors when reusing material, retain attribution, link the license and indicate changes. Third-party material retains its own terms. No separate software license is introduced at this stage.
