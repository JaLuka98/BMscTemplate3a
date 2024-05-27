# BMscTemplate3a

Welcome to the BMscTemplate3a, a LaTeX thesis template designed for BSc and MSc theses. This template is based on the work by Marcel Rieger: [Marcel Rieger's Thesis Template](https://gitlab.cern.ch/aachen-3a-cms/thesis-template). This README will guide you through the setup, usage, and customization of the template.

## Features

- Pre-configured structure for a thesis
- Includes templates for various sections: introduction, theory, conclusions, ... They are placed in the `content/` directory
- Supports bibliographies, citations, and references.
- Main document: thesis.tex where the other content files are referenced

## Getting Started

To use this template, follow these steps:

1. **Clone the repository:**
   ```
   git clone https://github.com/JaLuka98/BMscTemplate3a.git
   cd BMscTemplate3a
   ```

2. **Customise:**

Apply your changes. 

Note that at the moment, it is needed to download the Eidesstattliche Versicherung first as described in `documents/`. You should fill it out, print it, sign it and then include it into the directory. If you want to skip this part, you can exclude it in `thesis.tex` for the beginning.

3. **Compile the thesis:**

  The compilation can be done as follows:
  ```
  lualatex thesis.tex
  bibtex thesis
  lualatex thesis.tex
  lualatex thesis.tex
  ```

## Comments on the customization
### Binding Correction
In the thesis.tex file, you can set the binding correction with the following command:

`\newcommand{\bindcorrection}{no}`

Set this to yes if you need extra space for binding when printing. For PDF documents just viewed on a computer, it is usually preferred not to use a binding correction.

### References
You can get many references directly from [inspire](https://inspirehep.net/):
Export the citation in BibTeX format and add it to your .bib files.

Including the DOI in your references is optional. You can mark it with an "x" if you choose not to include it.

### Page Shift and New Page

In `content/index.tex`, use `\newpage` to start a new page for each section, or `\pageshift` to ensure new sections start on the desired page (even or odd). 



## ToDo:
- Indent everything correctly with spaces instead of tabs

- Check if "website" and "software" can be cited correctly
