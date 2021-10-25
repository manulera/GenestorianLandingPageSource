---
title: "Roadmap"
featured_image: "/images/roadmap.svg"
---

As a first step towards the development of Genestorian, I am developing [ShareYourCloning](https://github.com/manulera/ShareYourCloning). 

ShareYourCloning will provide a user interface to document and share cloning strategies. Sounds interesting? [Visit ShareYourCloning repository](https://github.com/manulera/ShareYourCloning).
<!--
Genestorian is a project that will involve the development of:

1. A standard file format to document genetic engineering steps
2. A web application to generate this documentation in the browser or programmatically
3. A web application with a database to store such information

None of the above software components, which will improve open reproducible science, exists as Open Source, and proprietary solutions do not cover the use-case of model organism research.

## 1. A file format for genetic engineering

Genestorian will store the genetic engineering steps followed to generate new entities from existing ones. The problem is that, as of now, no open file format exists to store this information. Developing a file format to record genetic engineering steps will set the foundations of Genestorian, but will also allow you to share your cloning strategy with others in an unambiguous way, that can also be read by computers.

The file will store the biological entities and the cloning steps in two different lists. Think about it like a family tree file, where you would store objects representing people in one list, and objects representing their relations in another list.
<details>
  <summary>Familiar with <code>.json?</code> Click here to see how the final format may look!</summary>

```
{
    "entities": [
        {
            "type": "Circular",
            "id": "pFA6a",
            "source": {...}
        },
        {...}
    ],
    "steps": [
        {
        "inputs": [{...},{...}],
        "output": {...},
        "method": {...},
        "proofs": [{...},{...}]
        },
        {...}
    ]
}
```
</details>

## 2. A web application to visualize and generate these files

That file format sounds interesting... But who wants to type all that? The next step is to build a web interface where you can generate this documentation in the browser. We will also build a web API so that you can generate this documentation programmatically with your favourite programming language.

The interface will be modular, and will allow the user to fully document the history of a DNA molecule, kind of like a family tree building tool. See an early example of the interface [here](/html/web_interface/index.html).

## 3. A web application with a database to store such information

Once the file format exists, and we have an easy way to generate this documentation, the next step is to build a database where this information can be stored, and a web application to access or enter information.

This is when strains and alleles come into play. Since existing strains are used to generate new ones by genetic engineering or sexual crossing, the same allele is present in multiple strains. The database will ensure that there is a single entry for each allele, which will contain the information of how it was generated. Additionally, it will record in which strains the allele is present, and how it was transmitted between them.

So now we have two genealogies to keep, that will be managed by two parts of the database: one for the DNA sequences (to know how they were engineered) and one for the strains (to know in which strains new alleles enter the collection, and how they are inherited). Below you can find a simplified scheme of database entities associated with biological resources and their relations.

<div class="figure_box">

{{< figure src="/images/database.svg" alt="database_image" >}}

<span class="span_biological_resource">Biological resources</span> will be mapped to entities in a relational database. Abstract entities in the database referred to as <span class="span_abstract_entity">sources</span> will store the information of the strain/plasmid generation process.  Genestorian will leverage <span class="span_bioinformatic_resource"> bioinformatic resources</span> to access genomic DNA sequences (like the Ensembl API), and to generate allele and plasmid sequences (in silico molecular biology libraries).

</div>

Here is a demo of a prototype of the web application. If you have some ideas or feedback, please [send an email](mailto:genestorian@gmail.com).

{{< youtube 34GMuHpl7f0 >}}
-->
