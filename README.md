## Preface
Several template has been used yet.
### Setup
1. If latex coding environment is based on **VScode** and **texlive**, first install an add-on named "Latex Workshop"
2. add this content below to your `setting.json`:
```json
 "latex-workshop.latex.recipe.default": "lastUsed",
  "latex-workshop.latex.autoBuild.run": "onSave",
  "latex-workshop.latex.tools": [
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOCFILE%"
      ]
    },
    {
      "name": "latexmk",
      "command": "latexmk",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "-xelatex",
        "-outdir=%OUTDIR%",
        "-cd",
        "%DOCFILE%"
      ],
      "env": {}
    },
    {
      "name": "xelatex",
      "command": "xelatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOCFILE%"
      ],
      "env": {}
    },
    {
      "name": "bibtex",
      "command": "bibtex",
      "args": [
        "%DOCFILE%"
      ]
    },
    {
      "name": "biber",
      "command": "biber",
      "args": [
        "%DOCFILE%"
      ],
      "env": {}
    }
  ],
  "latex-workshop.latex.recipes": [
    {
      "name": "latexmk",
      "tools": [
        "latexmk"
      ]
    },
    {
      "name": "zh-ref:xe->biber->xe->xe",
      "tools": [
        "xelatex",
        "biber",
        "xelatex",
        "xelatex"
      ]
    },
    {
      "name": "en-ref:xe->bib->xe->xe",
      "tools": [
        "xelatex",
        "bibtex",
        "xelatex",
        "xelatex"
      ]
    },
    {
      "name": "xelatex",
      "tools": [
        "xelatex"
      ]
    },
    {
      "name": "pdflatex",
      "tools": [
        "pdflatex"
      ]
    },
    {
      "name": "pdf->bib->pdf->pdf",
      "tools": [
        "pdflatex",
        "bibtex",
        "pdflatex",
        "pdflatex"
      ]
    }
  ],
  "latex-workshop.latex.clean.fileTypes": [
    "*.aux",
    "*.bbl",
    "*.blg",
    "*.idx",
    "*.ind",
    "*.lof",
    "*.lot",
    "*.out",
    "*.toc",
    "*.acn",
    "*.acr",
    "*.alg",
    "*.glg",
    "*.glo",
    "*.gls",
    "*.ist",
    "*.fls",
    "*.log",
    "*.fdb_latexmk",
    "*.xdv",
    "*.xml",
    "*.bcf",
    "*.synctex.gz"
  ],
  "latex-workshop.latex.clean.command": "latexmk",
```
Then turn to which template is and button `ctrl S`, a formatted pdf file can be made in few seconds.
### Beihang University Report template
This kind of template is stored in `./bh_report` folder, for whom want to form a report in latex coding.

### Certain Math Modeling Report Paper Template
The 20th Huawei Cup postgraduate Math Modeling Competition report paper template.