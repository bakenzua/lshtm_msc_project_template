# lshtm_msc_project_template

The goal of lshtm_msc_project_template is to provide a template [Quarto](https://quarto.org) book for a MSc project at [LSHTM](lshtm.ac.uk)

It provides a title page, with all the required components configurable through `_quarto.yml`, and a framework for writing up various sections of a project.


## Install

Either clone this git repository:

```         
git clone https://github.com/bakenzua/lshtm_msc_project_template.git
```

or download the [zip file](https://github.com/bakenzua/lshtm_msc_project_template/archive/refs/heads/master.zip) and extract somewhere appropriate on your pc.

## Configure

Configuration of the title page can be made by editing the metadata in `_quarto.yml`

Editable options are indicated via comments.

``` yaml
################################################
#   Title page metadata - edit accordingly     #
################################################
candidate-number: "007"
msc-course: "Medical Statistics"
academic-year: "2023-24"
page-count: "0"
project-length: "Standard" # Extended (MSc IID only)
################################################
```

#### Output file

Extra care should be taken with the `output-file` option as this does not compile from the other options:

``` yaml
# edit line below...
  output-file: "[Candidate Number]_[MSc]_[Year of Submission]_Project.pdf"
```

Replacing

-   `[Candidate Number]` with the candidate number, e.g. 1234

-   `[MSc]` with MSc title, e.g. MedSats

-   `[Year of Submission]` with year of submission, e.g. 2023

Will produce an output file: `1234_MedStats_2023_Project.pdf` as required

## Use

The project includes the following quarto files that are applicable for different sections of a project.

-   index.qmd

    -   Title page

    -   Table of contents

    -   Abstract

    -   Acknowledgements

-   intro.qmd

    -   Introduction

    -   Aims and Objectives

-   methods.qmd

-   results.qmd

-   discussion.qmd

-   references.qmd

-   appendices.qmd

## Citations and References

The `references.bib` file is a bibliography file as [described in Quarto documentation](https://quarto.org/docs/manuscripts/authoring/rstudio.html#citations). This can be exported from a reference manager, e.g. [Zotero](https://www.zotero.org/). To cite an article from the bibliography in your text, you use @ followed by the citation identifier. An example is given in `intro.qmd`. Cited articles will then automatically be compiled to the references page.

The `the-lance.csl` file is a [citation style](https://citationstyles.org/) definition which uses the styling required by The Lancet. Alternative citation and reference styles can be downloaded from [https://github.com/citation-style-language/styles](https://github.com/citation-style-language/styles). The `csl: the-lancet.csl` field of `_quarto.yml` should be amended accordingly.
