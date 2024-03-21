# What Is an Ontology?

-   In computer science, an ontology is defined as:

    > *A formal definition of types, properties, and relationships between entities that actually or fundamentally exist within a particular domain of discourse.*\([Wikipedia](https://es.wikipedia.org/wiki/Ontolog%C3%ADa_(inform%C3%A1tica))\)

-   An ontology is a **model of reality** expressed as a formal specification of **classes**, **properties**, and **individuals**.
-   An ontology is a **semantic schema** that documents the meaning of our data.


# Ontology Design

-   One of the first steps toward creating an ontology is to develop a set of **competency questions**.

-   These are questions that serve to define the scope of an ontology and test its usefulness later on.

-   Based on these questions, we can begin to construct a data model, defining classes, properties, and individuals.


# Ontology Design

-   For example, in an ontology about food and wine, we could ask competency questions like these:

    -   Which wine characteristics should I consider when choosing a wine?

    -   Is Bordeaux a red or white wine?

    -   Does Cabernet Sauvignon go well with seafood?

    -   What is the best choice of wine for grilled meat?

    -   Which characteristics of a wine affect its appropriateness for a dish?

    -   Does a bouquet or body of a specific wine change with vintage year?

    -   What were good vintages for Napa Zinfandel? \([Ontology 101](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf)\)


# From Spreadsheets to Schemas

![Excel spreadsheet showing a list of twenty fictional workshop participants (data was generated by ChatGPT 4.0). The spreadsheet has five columns: ID, Name, User, Inst, and Loc. It is annotated with three call-out boxes at the top, with arrows pointing to different parts of the spreadsheet. The first call-out points to the spreadsheet as a whole and asks the following questions: What's the context for this spreadsheet? Is it related to a system? The second call-out points to the Inst column and asks the following questions: Institution? What is the relationship between Person and Institution? Finally, the third call-out points to the Loc column and asks the following questions: Does Loc mean Location? Is it the location of the Institution or the Person?](../../submaps/../img/ontology/participants.svg "From Spreadsheets to Triples")


## Summary

-   Tabular data, such as what we find in spreadsheets, is not self-documenting.
-   We can guess about the meaning of columns and fields, but without a **semantic** schema, we can't be sure that our interpretation is correct. [1](#fntarg_1)

[1](#fnsrc_1) Example inspired by the book [*Linked Data: Structured Data on the Web \(Wood et al., 2013\)*](https://www.manning.com/books/linked-data).



# Activity: Competency Questions

1.  Imagine you are a library user doing research for a literature course.

2.  Think about the different information retrieval tasks you would like to perform using the library catalog.

3.  What kinds of questions about you like to ask?

4.  Develop a set of competency questions for a domain ontology about library information resources.

5.  Write each question on a Post-it note.
