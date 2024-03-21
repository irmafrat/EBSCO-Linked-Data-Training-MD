# Learning Turtle

-   Although JSON-LD is a common format for exchanging linked data on the web, one of the best ways to learn, write, and read RDF is through the Turtle serialization \([Terse RDF Triple Language](https://www.w3.org/TR/rdf12-turtle/), or TTL\).

-   A subset of Turtle, called [N-Triples](https://www.w3.org/TR/rdf12-n-triples/), is simply lines of triples \(which can be hard to read\).


## Prefixes

When we're writing RDF in Turtle, one of the first things we might want to do is declare some prefixes and namespaces so that we don't have to type as much.

```
@prefix bf: <http://id.loc.gov/ontologies/bibframe/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .

<https://metadatafram.es/alicia> foaf:name "Alicia" .
```

### Base

-   In addition to declaring prefixes, we can also use the `@base` keyword to declare the base URI for a Turtle file. Any relative URIs in our data will then be resolved against the base.
-   Instead of writing `<https://metadatafram.es/alicia>`, we can declare a base URI and then use relative URIs.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
                
<alicia> foaf:name "Alicia" .
```

## Semicolons

We can repeat statements about the same subject using semicolons.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .

<alicia> foaf:name "Alicia" ; foaf:nick "Al" .
```

**Note:** Notice the spacing around punctuation. \(Spacing is not required, but it makes the syntax easier to read.\)

## Commas

We can repeat objects for the same predicate using commas.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .

<alicia> foaf:name "Alicia" , "Al" .
```

## Typed Literals

-   When the object of a statement is a **literal** \(not a resource we can may statements about\), it can take a data type.
-   RDF uses the data types defined for XML, typically declared with the prefix `xsd`.
-   Data types are indicated with double carets, followed by the type name.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#date> .

<alicia> foaf:name "Alicia" ; <birthDate> "1946"^^xsd:date .
```

## Blank Nodes

In RDF, we sometimes need to say something about a resource whose identity we don't know \(or care\) about. These are called **blank nodes**.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#date> .

<alicia> foaf:name "Alicia" ; 
foaf:knows [ a foaf:Person ] ;
foaf:knows _:b1 .

_:b1 a foaf:Person .
```

**Note:** The example shows two different ways to encode a blank node: one with an identifier \(`_:b1`\) and one with square brackets. Blank node identifiers are not guaranteed to be unique across different Turtle files.

## Lists

We can also define lists, which can be [tricky in RDF](https://s.zazuko.com/zj3Rhn), but are easy to write in Turtle.

```
@base <https://metadatafram.es/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#date> .

<alicia> foaf:name "Alicia" ; 
foaf:knows (_:b1 _:b2 _:b3) .
```

## Type

-   Finally, Turtle defines a shortcut expression for the built-in RDF predicate `rdf:type`.
-   In Turtle, we can use the word `a` instead of `rdf:type`.
-   That way, it reads almost like an English sentence: `<alicia> a foaf:Person`.

**Note:** `rdf:type` is an important predicate because it allows us to say what kind of thing an entity is \(what **class** of things it belongs to\).


# Exercises with RDF and Turtle

-   This set of 10 exercises will sharpen your skills in working with RDF and the Turtle format.
-   Some exercises ask you to review a vocabulary such as [Schema.org](https://schema.org/), but most of them are hands-on and require you to edit a set of triples.
-   To validate your work, use an RDF editor such as the [Sketch editor](https://sketch.zazuko.com/), by Zazuko.


## Exercise 1

```language-ttl


<https://metadatafram.es/data/person1> <http://xmlns.com/foaf/0.1/name> "Alicia" .
<https://metadatafram.es/data/person2> <http://xmlns.com/foaf/0.1/name> "Roberto" .

                
```

1.  Add a new triple with a person3 and give them a name.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 2

```language-ttl


<https://metadatafram.es/data/person1> <http://xmlns.com/foaf/0.1/name> "Alice" .
<https://metadatafram.es/data/person1> <http://xmlns.com/foaf/0.1/knows> <https://metadatafram.es/data/person2> .

                
```

1.  Rewrite these triples using the feature of Turtle that allows us to avoid repeating a subject.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 3

```language-ttl


<https://metadatafram.es/data/person1> <http://xmlns.com/foaf/0.1/name> "Alicia" ;
<http://xmlns.com/foaf/0.1/knows> <https://metadatafram.es/data/person2> .
                    
                
```

1.  Now shorten the URIs by declaring prefixes at the top and using the qualified form.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 4

|Subject \(Domain\)|Property|Object \(Range\)|
|------------------|--------|----------------|
| | | |
| | | |
| | | |
| | | |
| | | |

1.  Explore the [Schema.org](https://schema.org/) vocabulary and see what types of entities and properties are defined there.

2.  List five possible "triple templates" in a table like the one above, using classes that can be related to each other as subject and object.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 5

```language-ttl


@prefix schema: <http://schema.org/> .

<> a schema: ;
schema:name "" ;
schema:author <> .

                
```

1.  Use the `rdf:type` predicate or the special `a` shortcut to say what kind of thing the subject of these statements is.

2.  Choose a term from [Schema.org](https://schema.org/).


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 6

|Subject \(Domain\)|Property|Object \(Range\)|
|------------------|--------|----------------|
| | | |
| | | |
| | | |
| | | |
| | | |

1.  Explore the vocabulary specification for [FOAF](http://xmlns.com/foaf/0.1/) \(Friend of a Friend\) and see what types of entities and properties are defined there.

2.  List five possible "triple templates" in a table like the one above, using classes that can be related to each other as subject and object.


## Exercise 7

```language-ttl


@prefix foaf: <http://xmlns.com/foaf/0.1/> .
                    
<> foaf:firstName "" ;
foaf:lastName "" ;
foaf:knows <> .
                   
                
```

1.  Using FOAF, choose some terms to use to begin creating a profile for yourself.

2.  How many statements can you add?


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 8

```language-ttl


@prefix dcterms: <https://purl.org/dc/terms/> .

<https://metadatafram.es/data/document1> dcterms:title "An Introduction to RDF" ;
dcterms:creator <> ;
dcterms:date "" .

                
```

1.  Explore the [Dublin Core Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/) vocabulary specification.

2.  Fill in the missing values and add further statements.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 9

```language-ttl


@base <urn:name/> .
                    
<alicia> a <Person> ; <age> 77 .
                    
                
```

1.  Are these statements valid Turtle? Why or why not?


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

## Exercise 10

```language-ttl


@prefix bf: <http://id.loc.gov/ontologies/bibframe/> .
@prefix dcterms: <https://purl.org/dc/terms/> .
@prefix schema: <http://schema.org/> .

<> a schema:Book ;
bf:title [ 
  a bf:Title ; bf:mainTitle "" ;
  dcterms:creator [] 
] .

                
```

1.  Where are the blank nodes in these statements?

2.  Rewrite the blank nodes using alternative syntax and fill in the statements.


**Related information**  


[RDF Sketch editor](https://sketch.zazuko.com/)

