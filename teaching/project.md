---
layout: teaching
title: "Class Project"
---

### In short

The bulk of the evaluation arises from the course project that students have to hand in. This is a computing project to be realized by groups of 2 persons. The content is free, but will have to include:

- The use of several datasets that will be merged and cleaned (can be collected from the web — scraping, API — or downloaded from existing databases)
- Descriptive statistics with meaningful visualisation
- Modelling (ML and/or NLP) with interpretation of the results

Students are invited to propose themes that they care about.

The project has to use Git and should be made available on GitHub.

### Project expectations

The project is a problem to which you want to find an answer, using data.

The first step is therefore to look for a problematization and contextualization. You should investigate a subject that appeals to you, so that you can motivate the reader to become involved in your approach.

There are three dimensions to the project. For each of these parts, you can go more or less far. But you should deepen at least one of the three dimensions (i.e. the "advanced" bullet points below).

**1. Data management**

The data can be directly available in the form of .txt, .csv files, etc. or come from websites (scraping, API).

You are likely to get data that is not 'clean': set up cleaning protocols to get a reliable and robust dataset(s) at the end of this stage to conduct your analysis. This is also the time to create variables that are more understandable, better identified, etc.

**2. Descriptive analysis and graphical representations**

With descriptive statistics, you seek to have an overall view of the major trends in your data: the link with the problem, how it allows you to answer it, what the first elements of the answer are... Each result must be interpreted (what does it show, how does it validate/contradict your argument?). In terms of graphical representations, several levels are possible. You can simply represent your data using `matplotlib`, go further with `seaborn` or `scikit-plot`. The basis of a good visualization is to find the right type of graph for what you want to show and to make it visible: a legend that makes sense, axes with names, etc.

**3. Modelling**

Last, you will propose a modelling approach to complete / reinforce the descriptive analysis. The model does not matter (linear regression, random forest or other): it must be appropriate (meet your problem) and justified. You can also compare several models that do not have the same purpose. The results must be interpreted as well.

#### Minimal expectation by part

1. **Data retrieval**
   - Standard: use several data sources, data cleaning
   - Advanced: data collection with webscraping, merge several datasets
2. **Data visualisation**
   - Standard: propose at least 4 exhibits (graphs or tables)
   - Advanced: one or more elaborated figures, such as maps, or unsupervised learning representations
3. **Data modelling**
   - Standard: supervised ML approach comparing at least 2 models, or NLP
   - Advanced: both a ML model and some NLP (for example)

### Organisation

#### Hand-in requirement [due date: TBD]

- A report taking the form of a **Jupyter Notebook**
  - Exception: if you want to develop an application (`Dash` or `Streamlit`)
  - Make sure your notebook is "correctly compiled" (i.e. cells named `[1]-[N]`)
  - You might need other Python or notebook files in the upstream analysis
- Everything should be hosted on a **GitHub repository**: data, code, notebook, slides
  - Project folder should have a well-defined structure
  - Code should be clean (e.g. functions instead of copy-paste)
  - You must have a `README.md` in the main directory with instructions on how to run the project and what it does, clearly indicating which file corresponds to the report

#### In-class project discussion

We will discuss your proposed project so that the instructors can evaluate whether it is doable within the time frame.

#### Project pitch

During this session, you present your project idea to the rest of the class, based on slides. The time allocated to each group will depend on the number of groups. Your presentation should contain:

- Project idea and motivation
- Question you are trying to answer
- The data used
- The methodological approach

#### Final presentation [23/11/2026]

You have to hand in the project and present it to the instructors (see the [course schedule](/teaching/data-management)).

The oral should be based on a beamer presentation, presenting the question you aim at answering, the underlying data, the descriptive and the modelling steps. You will be asked questions regarding the choice of the different visualisation and modelling approaches.

While the overall grade of the course project is at the group level, the presentation includes an individual dimension.

#### Submission format

Invite your instructors to collaborate on your GitHub repository by the due date.

### Some ideas for projects

- A platform inspired by [bxl-malade](https://bxl-malade.medor.coop/) for Liège using [opendata Liège](https://opendata.liege.be/) and [WalStat](https://walstat.iweps.be/walstat-open-data.php)
- A map of Belgium with communal level information from [WalStat](https://walstat.iweps.be/walstat-open-data.php) for Wallonia, [IBSA](https://ibsa.brussels/) for Bruxelles, and [statistics-flanders](https://www.vlaanderen.be/en/statistics-flanders)
- From past years: corporate performance and employee sentiment, modelling hotel prices in Paris using data from Booking, visualisation of the real estate landscape in the Province of Liège using data from Immoweb

[Back to Data Management](/teaching/data-management)
