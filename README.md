# NESTOR Clinical Validation Guidelines

Open-access guidelines, protocols and standard operating procedures for the validation and translation of data-driven innovative methods into clinical practice within the NESTOR research domains.

Based on the supplied D3.3 report, with **UM** as lead beneficiary. The public site covers the general validation workflow, legal and ethical guidance, multi-site harmonisation and an embryo image-analysis example. It presents practical guidance without website version labels or drafting history.

## Project context

This repository develops NESTOR **D3.3** in the revised deliverable list, originally **D3.4** in the proposal: “Protocols and standard operating procedures on practical recommendations covering the data driven innovative method validation into the clinical practice”, under WP3 and task T3.1. **UM is the lead beneficiary.** The revised identifier was confirmed by the project contributor. The separate interoperability report is now D3.2 in the supplied report draft (originally D3.3 in the proposal).

The scope covers personalised reproductive medicine, assisted reproductive technologies, non-invasive prenatal testing, uterine health, and AI/data-driven solutions for ART.

The separate `embryo-vision` repository contains the research implementation. This site presents the practical guidance from D3.3 v3, with explicit evidence limits and next steps for the exploratory embryo study. Private data and model weights are not copied here.

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

- [About the guidelines](docs/index.md): purpose, audience, scope and starting points.
- [From research to clinical use](docs/clinical-translation.md): Chapter 2, including the evidence stages in Table 2.
- [Practical workflow](docs/practical-workflow.md): Chapter 5 and Table 6, linked to checklist items and the worked example.
- [Legal, regulatory and ethical guidance](docs/regulatory-guidance.md): Chapter 3, Tables 3–4 and dated official implementation sources.
- [Harmonisation across sites](docs/harmonisation.md): Chapter 4 and the minimum practices in Table 5.
- [Validation checklist](docs/validation-checklist.md): all 30 Annex A items, with accessible checkboxes and print support. Selections are not stored; download the editable Word copy to maintain a study record.
- [Embryo image-analysis example](docs/embryo-image-analysis.md): Chapter 6, including current evidence and further validation needs in Table 7.
- [Limitations and next steps](docs/limitations.md): Chapters 8–9 and Table 8.
- [References and downloads](docs/references.md): source-numbered bibliography, original v3 report and an editable Annex A checklist.
- [Abbreviations](docs/abbreviations.md): the report's glossary.

Earlier [introduction](docs/introduction.md), [framework](docs/validation-framework/index.md), [protocol catalogue](docs/protocols/index.md) and [templates](docs/templates/index.md) are retained as inactive drafts. They are excluded from the built website and search index through `exclude_docs`; their content may be outdated and is not the current site structure. The references page is now active and follows the v3 report.

Edit Markdown in `docs/`; maintain navigation in [mkdocs.yml](mkdocs.yml). The report section and table anchors are stable cross-references and should be retained when editing headings. Record substantive differences from the source report in the repository history. Do not invent missing measurements, approvals, numerical cutoffs or governance assignments.

Refresh the source report download only when a new source version is supplied. Keep all checklist items and the `(M)` / `(C)` scope labels aligned between the source annex, web page and editable download. The downloadable v3 report is an unchanged copy of the supplied public deliverable.

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
