---
####################### Banner #########################
banner:
  title : "Genestorian"
  image : "images/genes2.svg"
  content : "An Open Source web application for model organism collections"

##################### Feature ##########################
feature:
  enable : true
  title : "Organise your collection of Plasmids and Strains"
  feature_item:
    # feature item loop
    - name : "By researchers, for researchers"
      icon : "fas fa-vial"
      content : "Genestorian is developed and used in the group of Jürg Bähler at UCL"
      
    # feature item loop
    - name : "Track plasmid lineage"
      icon : "fas fa-dna"
      content : "Keep track of all cloning operations of plasmids up to their entry point into your collection"
      
    # feature item loop
    - name : "Track strain lineage"
      icon : "fas fa-bacterium"
      content : "Keep track of genetic modifications and mating of all your strains."
      


######################### Service #####################
service:
  enable : true
  service_item:
    # service item loop
    - title : "Know the origin of every sequence"
      images:
      - "images/roadmap2_newcolours.svg"
      content : "Genestorian generates the sequences of new alleles and plasmids _in silico_ from existing sequences in your local collection or sequences retrieved from genome databases."
      button:
        enable : true
        label : "See a prototype of this feature"
        link : "https://shareyourcloning.netlify.app/"
        external_url: true
        
    # service item loop
    - title : "Browse your collection "
      images:
      - "images/browse_collection.svg"
      content : "Easily find all the strains that contain a certain allele, and the resources used to create that allele. Export this information to share with others or for publication."
      button:
        enable : true
        label : "See a prototype of this feature"
        link : "https://prototype.genestorian.org/login"
        external_url: true
        
    # service item loop
    - title : "A work in progress"
      images:
      - "images/work_in_progress.svg"
      content : "Genestorian is at a very early stage of development, but you can already get involved:
      
      * If you have some ideas or feedback.
      
      * If you want to contribute.
      
      * If you want to know more."
      button:
        enable : true
        label : "See how to get involved"
        link : "/contributing/"


---
<!-- 
# What is Genestorian?

Genestorian is an Open Source web application that allows researchers to document collections of model organism strains and recombinant DNA.

# Documenting genetic engineering

Genestorian stores your collection of strains and recombinant DNA in a relational database.

It stores the genetic engineering steps followed to generate new entities from existing ones.

Genestorian generates the sequences of new entities _in silico_ from existing sequences in your local collection or sequences retrieved from genome databases.

# Sharing better records with less effort

Your cloning strategy can be exported graphically or as text.

One click to produce an unambiguous record of your cloning strategy to be used in a publication, or shared with colleagues and collaborators!

Your data can be exported to json and other formats, so you can write scripts to do virtually anything you want. Check out this [network view](/html/network/index.html) of a strain collection, or this [web interface to document a cloning strategy](/html/web_interface/index.html)

# Why Open Source?

The collection of recombinant DNA and strains is one of the most valuable assets of a laboratory.

With an Open Source solution there are no proprietary file formats, changes on privacy policy nor company shut-downs and acquisitions to worry about!

# Demo of the prototype

Genestorian is at a very early stage of development. It will initially focus on collections of recombinant DNA and yeast/fungi strains.

We will keep the design of the tool as abstract as possible, so that it can incorporate the needs of multiple model organisms in the future.

You can find a [hosted prototype](https://prototype.genestorian.org) to illustrate the use-case of Genestorian, the code is on [github](https://github.com/manulera/YeastDatabase), and you can see a video of this prototype below. If you have some ideas or feedback, please [send an email](mailto:genestorian@gmail.com).

{{< youtube 34GMuHpl7f0 >}}

 -->