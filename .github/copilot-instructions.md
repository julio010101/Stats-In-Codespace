# AI Coding Agent Instructions

> Objective: Support educational statistical/data science workflows (Python + R + Jupyter) in a devcontainer/Codespaces setup. Optimize for adding chapter notebooks/scripts and dataset-driven exploration without breaking existing learning materials.

## Repository Essence
- Primary assets: Jupyter notebooks (`*.ipynb`), chapter Python/R scripts, SQL scripts, Clickhouse DB, small CSV + `.RData` datasets per chapter.
- Chapter organization under `Aula1/CapX-Favero/` and similar folders; each chapter contains: script(s) (`SCRIPT - Capítulo NN.py/.R/.ipynb`) and datasets (CSV + `.RData`).
- Environment provisioning via `.devcontainer/devcontainer.json` + `setup.sh` (installs Python, R, IRkernel, tidyverse, scientific Python stack).
- No automated test suite; validation is through successful notebook cell execution.

## Environment & Tools
- Python dependencies pinned loosely in `requirements.txt` (includes `numpy`, `pandas`, `polars`, `seaborn`, `statsmodels`, `stemgraphic`). Use existing libs—do not introduce heavy frameworks.
- R packages preinstalled (ggplot2, dplyr, tidyr, etc.)—avoid redundant install logic unless missing.
- If adding Python packages: append to `requirements.txt`; if adding R packages: modify `.devcontainer/setup.sh` or instruct install inline in notebook.

## Conventions
- Language: Comments, headings, variable names frequently in Portuguese—preserve style (e.g., `df_cotacoes`, headers with `##############################################################################`).
- Data access: Use relative paths to local CSV within the chapter folder (`pd.read_csv('Cotações.csv')`). Do not centralize datasets unless a cross-chapter reuse need is explicit.
- Keep educational clarity: Prefer explicit intermediate variables over dense chained expressions.
- Avoid refactoring header banners in existing scripts; they serve didactic structure.

## Adding New Chapter / Content
1. Create folder `AulaN/CapM-Favero/` (match existing casing/spaces/hyphen pattern).
2. Place datasets (`.csv`, optional `.RData`) directly inside folder.
3. Add script variants as needed: `SCRIPT - Capítulo MM.py`, `.R`, optionally a notebook version.
4. Start Python scripts with import block + banner; load data with `pd.read_csv('dataset.csv')`.
5. For notebooks: First cell should import libraries; second cell loads data; include Markdown explanation cells mirroring pattern in examples.

## Notebook & Script Patterns
- Python examples show: imports → data load → exploratory display (`df`, `df.info()`, `.describe()`) → statistical summaries → plots (Seaborn/Matplotlib) → specialized visuals (`stemgraphic`).
- R notebooks: tidyverse style; mimic structure when adding new R examples.
- Use separate cells for major steps (loading, EDA, visualization, modeling) to aid incremental teaching.

## Data Handling
- Large binary files (`*.RData`) already tracked—do not convert/rewrite unless necessary; prefer adding new sources as CSV for transparency.
- If dataset size grows significantly, consider Git LFS (there is a `git-lfs.ipynb` indicating awareness). Mention but do not auto-configure unless asked.

## ClickHouse Integration
- A `clickhouse` binary/file exists plus notebooks under `Aula1/julio/` & `Aula2/julio/` referencing ClickHouse usage and backup. Treat ClickHouse as the core topic.
- If adding ClickHouse examples: create isolated notebook (`clickhouse-<topic>.ipynb`) with connection setup cell and clearly marked prerequisites.

## Safe Changes
- Do NOT rename existing educational files; references may exist externally (lesson plans).
- Avoid silent dependency additions—surface rationale in PR description.
- Preserve relative paths; avoid absolute filesystem assumptions inside notebooks.

## Validation Workflow
- After modifying a script/notebook: run all cells top-to-bottom; ensure no errors and plots render.
- For new libs: import in a scratch notebook first to confirm availability in container.
- For environment changes: ensure `.devcontainer/setup.sh` remains idempotent (re-runs without failure).

## Git & PR Guidance for Agents
- Commit scope: one conceptual addition (new chapter, new dataset, ClickHouse example) per PR.
- Commit message style may follow `feat:` / `docs:` etc. (see `CONTRIBUTING.md`). Use Portuguese when modifying Portuguese files; English acceptable for infra.

## When Unsure
- Ask whether content targets Python, R, or both before generating cross-language examples.
- Clarify if a dataset should be shared across chapters before centralizing.

## Quick Reference Paths
- Devcontainer: `.devcontainer/devcontainer.json`, `.devcontainer/setup.sh`
- Python deps: `requirements.txt`
- Examples: `exemplo_estatistica.ipynb`, `exemplo_python.ipynb`
- Chapter scripts: `Aula1/Cap2-Favero/SCRIPT - Capítulo 02.py` (illustrative structure)

> Operate as a careful editor: enhance educational clarity, avoid architectural overreach.
