# AGENTS.md

## Cursor Cloud specific instructions

This is a LaTeX CV/Resume project based on the [Awesome-CV](https://github.com/posquit0/Awesome-CV) template. There are no application servers, databases, or package managers — only LaTeX compilation.

### Building documents

Compile any `.tex` file with `lualatex` (preferred per README) or `xelatex`:

```bash
lualatex -interaction=nonstopmode resume.tex
lualatex -interaction=nonstopmode cv.tex
lualatex -interaction=nonstopmode coverletter.tex
```

The `fonts/` directory ships Roboto and FontAwesome TTFs used by `awesome-cv.cls`. FontAwesome icon glyphs may produce "Missing character" warnings — this is cosmetic and does not prevent PDF generation.

### Linting

```bash
chktex resume.tex
chktex cv.tex
chktex coverletter.tex
```

`chktex` returns exit code 2 for warnings (no errors). All current warnings are stylistic (dash lengths, command spacing) and expected for this template.

### Key files

| File | Purpose |
|---|---|
| `resume.tex` | Main résumé (letter paper) — references `resume/*.tex` sections |
| `cv.tex` | Full CV (A4 paper) — references `cv/*.tex` sections |
| `coverletter.tex` | Cover letter template |
| `awesome-cv.cls` | Document class defining layout/styling |
| `fontawesome.sty` | FontAwesome icon support |
| `fonts/` | Bundled Roboto and FontAwesome font files |
