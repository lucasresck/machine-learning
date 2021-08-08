# machine-learning

Problem sets and implementations for [Machine Learning](https://emap.fgv.br/disciplina/graduacao/aprendizado-de-maquinas) (2021, FGV).
Professor: [Rodrigo Targino](https://emap.fgv.br/corpo-docente/rodrigo-santos-targino).

## Separability of legal documents according to precedent citations

It was the main evaluated assignment from this course. Bellow, you can watch a YouTube video summarizing the work.

[![](https://img.youtube.com/vi/W8gp3DzQgg0/0.jpg)](https://www.youtube.com/watch?v=W8gp3DzQgg0)

The Brazilian Supreme Court (STF) frequently cites what is called a "Súmula Vinculante," or Binding Precedent (BP), in their decisions, which is a precedent that has mandatory application. 58 BPs have already been created until today. It seems trivial that documents that cite the same precedents have the same subjects, and documents that cite different precedents have different subjects. In this work, we explore if this is also trivial for machine learning models, i.e., if traditional machine learning models can learn to "separate" these documents according to precedent citations, particularly Binding Precedents. The main result is the fact that the documents are very separable, even linearly separable, according to the BP citations.

Consider, for example, a dimensionality reduction of the (TF-IDF) vectors extracted from the documents:

<img src="https://github.com/lucasresck/machine-learning/blob/main/images/svd_1.png?raw=true" width="480">

We see that the documents are very separable, according to the BP citation.

This was the result when we fitted many supervised models, trying to predict which precedent was being cited:

<img src="https://github.com/lucasresck/machine-learning/blob/main/images/accuracies.png?raw=true" width="480">

We achieved high performance classification metrics, indicating the high separability of the documents.

More details can be found at the [assignment file](https://github.com/lucasresck/machine-learning/blob/main/a2_assignment/main.pdf).
