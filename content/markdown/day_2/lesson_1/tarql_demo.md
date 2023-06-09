---
author: [EBSCO Information Services, Timothy A. Thompson \| @timathom\[@indieweb.social\], timothy.thompson@yale.edu]
---

# Tarql Demo: From Spreadsheets to Triples

Debugging

![Excel spreadsheet showing a list of twenty fictional workshop participants (data was generated by ChatGPT 4.0). The spreadsheet has five columns: ID, Name, User, Inst, and Loc. It is annotated with three call-out boxes at the top, with arrows pointing to different parts of the spreadsheet. The first call-out points to the spreadsheet as a whole and asks the following questions: What's the context for this spreadsheet? Is it related to a system? The second call-out points to the Inst column and asks the following questions: Institution? What is the relationship between Person and Institution? Finally, the third call-out points to the Loc column and asks the following questions: Does Loc mean Location? Is it the location of the Institution or the Person? For highlighting purposes, three black boxes have been overlaid on the spreadsheet: one is drawn around the Inst header, one around a value in the ID column, and one around a value in the Inst column. Finally, a large text box overlay covers the bottom part of the spreadsheet and shows two triples: person worksFor organization and organization name Universidade de Chile.](../../submaps/../img/tools/from_spreadsheets_to_triples.svg "From Spreadsheets to Triples")

**Previous topic:**[Showcase of Tools](../../day_2/lesson_1/showcase_of_tools.md)

**Next topic:**[LUX: Yale Collections Discovery](../../day_2/lesson_2/lux_yale_collections_discovery.md)

## Summary

Using a command-line tool such as Tarql, we can easily convert from tabular data and spreadsheets to RDF triples that conform to a semantic schema or ontology.

## Tarql Demo: Input and Output

-   After downloaded Tarql, we run it from the command line like this: `sh bin/tarql -v participants_mapping.rq participants_fictional.csv > participants_mapped.ttl`
-   We need to specify a SPARQL query to map our data \(`participants_mapping.rq`\), an input CSV file \(`participants_fictional.csv`\) and a Turtle file for saving our output \(`participants_fictional_mapped.ttl`\).
-   The Turtle file can then be loaded into a triple store for querying.
-   You can see examples below under Related Links.

**Related information**  


[SPARQL Mapping Query](../../resources/code/participants_mapping.rq)

[CSV input data](../../resources/data/participants_fictional.csv)

[Turtle output data](../../resources/data/participants_fictional_mapped.ttl)
