# BIBFRAME in the Metadata Landscape

![Network diagram showing the relationship between BIBFRAME and other metadata standards. The diagram depicts a graph that starts with a square node labeled BIBFRAME on the left, with edges depicting relationships to OWL, RDA, MARC 21, RDF, AACR2, and IFLA LRM. The relationships are as follows: BIBFRAME uses RDF, uses in part OWL, codifies RDA, replaces and translates MARC 21, and is inspired by IFLA LRM. Other nodes also have relationships: OWL formalizes RDF; RDA uses in part RDF, replaces AACR2, and implements IFLA LRM.](../../../submaps/../img/bibframe_etc/bf_landscape.svg "BIBFRAME Landscape")


# A Brief History of BIBFRAME

-   **May 2011**: the launch of the BIBFRAME Initiative was announced

-   **March 2013**: BIBFRAME 1.0 was released

-   **2015**: the model was reviewed by invited experts, who recommended:

    -   Reuse of other vocabularies

    -   Links to things, not strings

    -   Rethinking the model for administrative metadata

-   **April 2016**: BIBFRAME 2.0 was launched

-   **2018**: the Library of Congress BIBFRAME pilot project was launched

-   **2021**: the "BIBFRAME 100" project was launched

-   **June 2021**: BIBFRAME 2.1 was released


# What Is the BIBFRAME Model?

BIBFRAME 1.0 model

![Network diagram showing a high-level overview of the BIBFRAME 1.0 model, divided between Work and Instance.](../../../submaps/../img/bibframe_etc/bibframe1.png "BIBFRAME 1.0")

# What Is the BIBFRAME Model?

BIBFRAME 2.0 model

![Network diagram showing a high-level overview of the BIBFRAME 2.0 model, divided among Work, Instance, and Item.](../../../submaps/../img/bibframe_etc/bibframe2.jpg "BIBFRAME 2.0")


# BIBFRAME Patterns: Work, Instance, Item

BIBFRAME 2.0 model

![Network diagram showing an example BIBFRAME model for the work Their Eyes Were Watching God, by Zora Neale Hurston. The diagram shows the relationships among Work, Expression, Manifestation (Instance in BIBFRAME) and Item.](../../../submaps/../img/bibframe_etc/bf_graph.svg "BIBFRAME Patterns: Work, Instance, Item")


# BIBFRAME Patterns: Contribution

BIBFRAME 2.0 model

![Network diagram showing an example BIBFRAME model for contributors to an inscription. The Inscription class comes from the ARM ontology. One contribution is defined with role giver and agent Zora Neale Hurston (Person), and another is defined with role receiver and agent Carl Van Vechten (Person).](../../../submaps/../img/bibframe_etc/arm_inscription_bf_contributions.svg "BIBFRAME Patterns: Contribution")


# BIBFRAME Patterns: Title

BIBFRAME 2.0 model

![Network diagram showing an example BIBFRAME model for a Title. The diagram shows a BIBFRAME Instance URI with a title relation to a Title node that, for its part, has values for main title and subtitle.](../../../submaps/../img/bibframe_etc/bf_title.svg "BIBFRAME Patterns: Title")


# BIBFRAME Patterns: Provision Activity \(Publication\)

BIBFRAME 2.0 model

![Network diagram showing an example BIBFRAME model for a Provision Activity (subclass Publication). The diagram shows a place relation to a URI representing Italy, as well as three BFLC extension properties for the simple string values extracted from the MARC source data.](../../../submaps/../img/bibframe_etc/bf_provision.svg "BIBFRAME Patterns: Provision (Publication)")


## Summary

-   BIBFRAME 2.0 defines a pattern for grouping information about the provision of a resource, such as the publication of an Instance.
-   This pattern allows data to be both recorded as both linked data \(notice the URI for Italy\) and string literals.
-   Terms from the [Library of Congress Extension Vocabulary for BIBFRAME](https://id.loc.gov/ontologies/bflc.html) \(BFLC\) are used to record "simple" place, agent, and date values.



# From MARC 21 to BIBFRAME

BIBFRAME 2.0 model

![Diagram showing the BIBFRAME 2.0 model on the left and slivers of MARC 21 bibliographic fields on the right (fields 130, 245, 260, and 300). Arrows extend from the fields to the BIBFRAME 2.0 entities to which they correspond: 130 maps to Work; 245 maps to Work and Instance; 260 maps to Instance; 300 maps to Instance and Item.](../../../submaps/../img/bibframe_etc/marc_to_bibframe.png "From MARC 21 to BIBFRAME")


## Summary

A single MARC 21 bibliographic record contains fields \(and subfields\) that map to different entities in the BIBFRAME model.


# The BIBFRAME Ecosystem

-   Other standards in the BIBFRAME ecosystem:

    -   [MADS/RDF](https://www.loc.gov/standards/mads/rdf/) \(Metadata Authority Description Schema\)

    -   Library of Congress Vocabularies like the [Name Authority File](https://id.loc.gov/authorities/names.html)

    -   Domain extension ontologies for [Art and Rare Materials](https://github.com/Art-and-Rare-Materials-BF-Ext/arm) \(ARM\), Performed Music, and others

    -   Library of Congress [tools](https://bibframe.org/)

    -   [BIBFRAME en español](https://docs.google.com/spreadsheets/d/1KgpWmMSyAEVVkfQgBPB0tdf6jk9cJ81z8S_Z9k4mH-8/edit?usp=sharing)


# Cataloging with BIBFRAME

-   First, let's review the [BIBFRAME model](https://id.loc.gov/ontologies/bibframe.html).

-   Try to match your categories against the terms in BIBFRAME

-   Now, let's use the hosted version of the Library of Congress [Marva Editor](https://bibframe.org/marva/editor/) to gain some hands-on experience with BIBFRAME.

-   Choose one of the PDF files with scanned images of a book to catalog:

    -   *Reading with Clarice Lispector*
    -   *The Versatility of Bamboo*
-   Work in groups. Half the group should work on the **Instance** description and half on the **Work** description.

-   If time allows, switch roles after finishing.


**Related information**  


[Reading with Clarice Lispector](../../../resources/activities/cataloging_activity/Reading_with_Clarice_Lispector.pdf)

[The Versatility of Bamboo](../../../resources/activities/cataloging_activity/Versatility_of_Bamboo.pdf)

