# Publishing this reconstruction to GitHub

**Suggested repository name:** `australian-wage-growth-vs-inflation`

**Short description:** `Reproducible Australian CPI vs WPI analysis using original ABS data, Python and quarterly real-wage index comparisons.`

This project is a **reconstructed and independently rerun Python analysis**, not a recovered copy of the author's earlier RMIT R assignment or RPubs publication. Keep that distinction in the repository description and on your CV.

## Upload using the GitHub website

1. Go to https://github.com/new, sign in, set the repository name shown above and select **Public** if you want a portfolio project.
2. **Do not** select “Add a README”, “Add .gitignore”, or “Choose a licence”; all required documentation and `.gitignore` are already in this package. The ABS data have their own attribution/licensing terms, so a blanket repository licence was not added.
3. Create repository. On its next page, choose **uploading an existing file**.
4. Extract the ZIP first. Open the `australia-wage-vs-inflation` folder, then upload its **contents** (not the enclosing folder) so `README.md` appears at the repo root. GitHub's web upload supports file drag-and-drop. If the browser will not preserve your nested directories, use the command-line alternative below.
5. Enter commit message: `Publish independently verified ABS CPI vs WPI analysis` and commit to `main`.
6. Confirm the README renders the figure, the notebooks open, and the source citations/attribution are visible.

## Reliable command-line alternative

Create an **empty** repository on GitHub first; then open a terminal from inside the extracted `australia-wage-vs-inflation` folder:

```bash
git init
git add .
git commit -m "Publish independently verified ABS CPI vs WPI analysis"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/australian-wage-growth-vs-inflation.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your real GitHub username and authenticate when prompted. Never put a personal access token into source code or this package.

## Quality and attribution checklist

- [ ] README says the notebook is a **reconstruction**, not the original RMIT R project.
- [ ] `data/` contains the unchanged uploaded ABS files; `data/SHA256.txt` matches both.
- [ ] ABS sources and reuse conditions are credited in `data/SOURCE.txt`.
- [ ] `notebooks/analysis_EXECUTED.ipynb` displays executed results.
- [ ] Run `pip install -r requirements.txt`, install Jupyter, open notebook from `notebooks/`, then **Restart & Run All** when your environment is ready.
- [ ] Don't interpret the WPI/CPI ratio as take-home pay or an individual household's real income.
- [ ] Avoid claiming the historical RPubs project had these exact figures.

## Suggested CV wording

**Australian Wage Growth vs Inflation (Independent Python Reconstruction)** — Recovered analysis logic from a prior notebook-development record and reproduced quarterly Australian CPI/WPI comparisons using original ABS workbooks; documented source series, indexed comparison and validation checks, with reproducible notebooks and exports.
