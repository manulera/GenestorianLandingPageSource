---
title: "Internships"
---

If you are here, you might be interested in doing an internship working on Genestorian.

You might not know know much biology, but don't worry! An internship with us can also be an opportunity for you to learn about the fascinating world of genetics and genetic engineering. Here are some basics to understand the use-case we are trying to address.

{{< table_of_contents >}}

## A video summary

In this video, the use case is explained for the general public in ~3 mins.

{{< youtube dh8XevL1Fbo >}}

## Key concepts in Genetics for research

### Genetics: why?
**Genes** are sequences of DNA that encode information to produce important biological molecules: RNA and proteins ([read more](https://en.wikipedia.org/wiki/Central_dogma_of_molecular_biology)). These molecules are involved in cellular functions like generating energy, duplicating the genetic material, or moving cells and their components. Virtually all cellular processes involve a protein or RNA encoded by a gene.

**Genetics** is a branch of biology that uses a series of techniques to modify the DNA sequence of organisms (**genetic engineering**) in order to study **gene functions**. A classic genetic experiment is to remove the entire sequence of a gene from an organism and study the consequences of the absence of this gene. Processes that are perturbed when a gene is missing point to its **gene function**: the function of the RNA or protein encoded by the missing gene. Other gene modifications are possible. For example, DNA fragments can be removed from a gene to understand the function of the specific part of a protein encoded by that fragment. Another example is adding a marker DNA sequence to a gene so that the encoded protein becomes visible in a microscope. Such genetic modifications produce new **gene variants, known as alleles**.

Certain species are frequently used in research, and are known as **model organisms**. Popular examples are the bacteria *E. coli* and the baker's yeast *S. cerevisiae*.  For a certain model organism, several genetic variants exist, known as **strains**. An important concept in genetics is the concept of **wild-type strain**, a “normal” genetic variant of that organism for which the sequences of all genes are known. When a genetic modification is made in the wild-type strain, the resulting new strain is characterised by its **genotype**, which lists the non-wild-type **alleles** present in that new strain. For example, if we remove the gene named ase1 in a yeast wild-type strain, the genotype of the resulting new strain will be "ase1Δ" ("Δ" means that the gene has been removed).

### Genetics: how?

That's all great, but how do you edit the DNA of an organism? For this, we use **recombinant DNA**, molecules of DNA that exist outside of cells and can be manipulated in the lab. There are multiple techniques that allow us to generate a desired DNA sequence, but they tipycally eiher combine pieces of existing recombinant DNA molecules or add small modifications. So every molecule of DNA always comes from another one. We could, for example combine two pieces of existing **plasmids** (circular DNA) to generate a new plasmid (see below). A way to this is by "cutting and pasting" the pieces of interest using **restriction enzymes** (scissors in the figure), molecules that cut the DNA at specific sequences.

{{< figure src="/images/plasmid_combination.svg" alt="plasmid_combination" width="300px" margin="auto">}}

Once we have our desired sequence, we can insert it or replace a fragment in the genome of an organism using **genetic engineering** methods.

## The problem we are solving

We want to develop a web application for researchers to be able to track the **ancestry** of their plasmids and strains. Let's start with a practical example, depicted in the figure below.

{{< figure src="/images/genealogies.svg" alt="genealogies" width="250px" margin="auto">}}

First, we take a plasmid, and we replace a fragment of the 1st chromosome in the wild-type strain by a fragment from the plasmid. We have then generated:

1. A new sequence / allele.
2. A new strain.

{{< figure src="/images/genealogies_1.svg" alt="genealogies_1" width="250px" margin="auto">}}

Then, we take this newly generated strain, and we cross it sexually with a strain from our collection that has a non-wild-type allele in chromosome 3. Among the offspring, we will find all combinations of the parent alleles, and we select a cell that has both alleles in chrosome 1 and 3 to stablish a new strain. This time we have generated only:

1. A new strain.

{{< figure src="/images/genealogies_2.svg" alt="genealogies_2" width="250px" margin="auto">}}

So, when we say ancestry we actually mean two things:

* The ancestry of sequences: How new sequences (in alleles or recombinant DNA) were generated from existing ones.

* The ancestry of strains: What alleles exist in a given strain, and how they were acquired.

At this point, you are probably thinking: 🤔 Well, I am sure there is already an Open Standard to encode this information given that these operations are routinely done in **hundreds of laboratories** using cutting-edge technology, working on different model organisms, storing **millions of strains** used to study embryonic development, cancer, ageing, and other biological processes.

<div class="alert alert-danger text-center mx-auto" role="alert" style="width:fit-content"><strong>🚨Spoiler alert🚨</strong><br>That is not the case</div>

The inventories of strain collections are typically kept as plain text in spreadsheets or similar tables. This is prone to errors and inconsistency because genotypes are input manually as plain text.

### How we want to solve it

We want to extend the [Synthetic Biology Open Language (SBOL)](https://sbolstandard.org/), an open standard for the representation of DNA. SBOL currently has abstract functionality for linking entities to their ancestors through an experimental step, but no specific implementations of concrete experimental procedures that combine existing sequences exist. Basically, we can represent that `A` comes from `B`, but no software tools are available to systematically generate `B` from `A` by reading experimental information nor verify that `B` comes from `A` if the experimental information is provided. We want to implement this functionality, and make a web application where researchers can document the generation of strains and recombinant DNA. 

### What you can do during your internship

An important challenge for the project is to migrate data from spreadsheets to the database. You will develop a first version of a tool to perform the data refinement required to migrate from spreadsheet to the database. The task will require:

* From a table where the genotypes of strains are represented as strings, identify the allele names.
* See if those alleles correspond to known alleles for that organism (from lists that are available online).
* Extract the information of in which strains a new allele was generated, and the relationships parent-child between strains. How this information is recorded in the spreadsheet (if it is recorded at all) will very likely vary.
* Score the predictions depending on certainty.
* Format those predictions os that they can be imported into the database.
* (Optional) develop a system for users to validate or change the predictions.
* (Optional) develop a web interface for users to input their data, browse through the predictions, and validate or change them there.

Questions? Comments? [Send an email!](mailto:genestorian@gmail.com)

If you are planning to apply for a Google Summer of Code internship, please have a look at [this repo](https://github.com/manulera/genestorian_data_refinement) where you will find useful details for your application, and questions by other prospective applicants. You can follow or star the repository to see if further info is added.
