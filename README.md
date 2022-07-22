
# Project Template

![Last
updated](https://img.shields.io/github/last-commit/mavrxlab/project-template)

<!-- Only edit README.Rmd, never README.md! Knitting README.Rmd will produce README.md -->

## Overview

Edit this section by replacing the (items in parens) below. This acts as
a *de facto* pre-registration and can be used in your OSF project.

1.  **Title and author(s).** (Be specific. Even if you’re unsure about
    the idea at this point; you can always update after consultation. If
    there are multiple contributors, consider specifying the
    [CRediT](https://casrai.org/credit/) taxonomy, as well.)
2.  **Summary of research questions or hypothesis.** (What are you
    wanting to discover? If you’re exploring, what are you exploring?
    What do you expect to happen or to find?)
3.  **Motivation.** (Provide some context for the previous statement.
    Why do you want to know? Be specific.)
4.  **Data.** (How are you going to answer your question or explore your
    hypothesis? Are you using a dataset? If so, link to it here. Are you
    doing a literature review? State your criteria for selection. Are
    you exploring an experience or concept? State how you’ll take notes
    and gather information, for example your own actions or the
    observation/interviewing of others?)
    1.  **Have you begun gathering data?** (Yes or No.)
    2.  **If yes, have you looked at the gathered data?** (Yes or No.)
5.  **Methods.** (On the heels of the previous item, what will your
    research method be? You may need to work with your faculty sponsor
    and/or the lab director on this.)
6.  **Plan.** (Using the project timelines provided in the lab manual,
    describe your proposed process and plan to accomplish your project.
    Try to list the steps of your plan using SMART goals.)
7.  **Leveraging the lab.** (How, specifically do you want to leverage
    the resources provided by the lab? Do you need time with some
    equipment, access to the space, research support from the lab
    personnel? If you need something specific, list this here.)

## Template Information

Based on the template made by [Ryan
Straight](https://github.com/ryanstraight) with [APCV
302](https://uaappcomp.github.io/apcv302/) in mind, specifically, as the
focus is on using R for data analysis, this template is simple enough to
fit most needs and has the media structure necessary for projects within
the lab.

If you’d rather not use the R-based ecosystem for writing that’s present
in the template, that’s fine. The folder structure will still serve you
well.

The actual report document being produced is an APA 6th edition document
using the [`papaja`](https://github.com/crsh/papaja) package, and uses
[`rfordatascience/tidytuesday`](https://github.com/rfordatascience/tidytuesday)
code. You should also install `tinytex`, of course, as per the `papaja`
instructions. Some demo code had been added to the script files and
dummy text to the `draft.Rmd` to produce an example PDF. The
`Bee Colony losses` dataset is loaded as an example. You’ll notice heavy
use of the `here` package, as well.

**Important**: each time you knit `draft.Rmd`, you will query GitHub.
There is a limit on how often you can do this. Manually downloading the
data into the `/data/raw` folder and loading from there will get around
this.

An example of how to do this is to remove the `tidytuesdayR` data
loading line from `munge.R`. Instead, simply run this in the console:

``` r
download.file('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2022/2022-01-11/colony.csv', here("3-Study", "2-Content", "1-Data", "raw", "colony.csv"))
```

Then, your data load in `munge.R` would be as such and you needn’t worry
about loading from GitHub:

`colony <- readr::read_csv(here("3-Study", "2-Content", "1-Data", "raw", "colony.csv'))`

## Authors

1.  Make your copy of the [contributor’s
    template](https://docs.google.com/spreadsheets/d/1Gl0cwqN_nTsdFH9yhSvi9NypBfDCEhViGq4A3MnBrG8/copy)
    and complete as needed. Ensure your spreadsheet’s permissions are
    set to `Anyone with the link can view`.
2.  Place that URL in step 2 of the
    [tenzing](https://rollercoaster.shinyapps.io/tenzing/) Shiny app.
    (You can use [this
    spreadsheet](https://docs.google.com/spreadsheets/d/1-WmAfoW3HoHGfmeahcOrSTGxXwZpScUBajoHHrQ0Qy8/edit#gid=0)
    as a demonstration if you like.)
3.  Choose `Show papaja YAML` in Step 3.
4.  Replace the `author` and `affiliation` frontmatter in the
    `draft.Rmd` file with this new YAML.

## Report

The resultant publications from this project go in
`4-Dissemination/2-Publications/` in subfolders for each individual
publication. The `papaja` document, `draft.Rmd`, has a variety of
comments and instructions within as comments. These are general
suggestions that follow a generic research paper structure.

## Folder and file structure

This is the default structure for a project. It’s very basic and you
should feel welcome to alter it to your liking. There is another README
in the `3-Study/2-Content/2-Media/` folder that explains the extensive
structure there. This structure is not meant to be in chronological
order, just organized.

1.  Project Management
    1.  Proposals
    2.  Finance (notes on seeking funding, so on; copies of grant
        proposal)
    3.  Reports (not papers; project-related reports like status)
    4.  Administration (CRediT author list, publication checklist, )
2.  Ethics Governance
    1.  Ethics Approval (IRB, CITI certification)
    2.  Forms (**blank** consent, waiver, etc forms; completed forms
        should be stored securely)
3.  Study
    1.  Input (files/docs used in the experiment itself; survey
        instrument, anything)
    2.  Content
        1.  Data (raw and tidied data)
        2.  Media (video recordings, audio, screencasts, so on)
    3.  Data Analysis (eda, munging scripts, transformation, etc)
    4.  Outputs (tables, figures, etc)
4.  Dissemination
    1.  Presentations (archived)
    2.  Publications (archived)
    3.  Publicity (archived)

Note that the Dissemination folder is for *archiving* content.
