# Master's Thesis -- LaTeX Skeleton

Cold-Start Preference Alignment of LLMs: a Comparative Study (Nova SBE, BA).

## Build

Recommended:
```
latexmk -pdf main.tex
```

Manual:
```
pdflatex main
biber main
pdflatex main
pdflatex main
```

You need a TeX distribution with `biber`, `biblatex`, `cleveref`, `siunitx`,
`tabularx`, `microtype`, and `setspace`. TeX Live full or MacTeX full will
have all of these.

## Structure

```
thesis/
├── main.tex                    # preamble, doc skeleton, \input sections
├── references.bib              # BibLaTeX database
├── figures/                    # drop PDF/PNG figures here
└── sections/
    ├── 00_abstract.tex
    ├── 01_introduction.tex
    ├── 02_background.tex
    ├── 03_methodology.tex
    ├── 04_experimental_design.tex
    ├── 05_results.tex
    ├── 06_business_analysis.tex
    ├── 07_limitations.tex
    ├── 08_conclusion.tex
    └── 09_ai_disclosure.tex
```

## Workflow notes

- Every section starts with a comment block stating its **page budget** and
  the **points it must hit**. Don't drift from those without updating the
  budget elsewhere.
- `\todo{...}` macro renders in red so it's impossible to miss before
  submission. Search-and-replace `\todo{` to find them all.
- Figures live under `figures/` and are picked up by `graphicspath`.
  Replace the placeholder `\fbox{...}` blocks in section 5 with real
  `\includegraphics{...}` calls once the plots are ready.
- The cover page in `main.tex` is a placeholder. **Before submission**,
  swap it out for the official Nova SBE WP cover-page template from the
  WP SharePoint, with the correct title, advisor, and student ID.
- The AI Usage Disclosure appendix (`sections/09_ai_disclosure.tex`)
  exists because Nova SBE's guidelines require it. Fill it in honestly.

## Page budget

| Section                            | Target |
| ---------------------------------- | ------ |
| 1 Introduction                     | ~2.5 pp |
| 2 Background                       | ~3.0 pp |
| 3 Methodology                      | ~4.0 pp |
| 4 Experimental Design              | ~2.0 pp |
| 5 Results                          | ~4.0 pp |
| 6 Business Analysis                | ~4.5 pp |
| 7 Limitations & Future Work        | ~1.5 pp |
| 8 Conclusion                       | ~1.0 pp |
| **Body total**                     | **~22.5 pp** |

References and appendices are **after** the 25-pp body limit and don't
count against it.
