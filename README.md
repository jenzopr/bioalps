genomics alps
=============

This repository contains a proposal for ALPS profiles in the genome science domain. Profiles are drafts and will very likely change in the next few weeks.

The domain: Genome science (genomics)
=====================================

## Key concept

We use four entities to share our understanding of the genomics domain:

- Objects/entities: A bioobject or bioentity represents one of the key components in genomics, e.g. a chromosome, a gene, a CDS, a protein and the like. Semantically, it is described by a sequence (i.e. a concatenation of letters from an arbitrary alphabet) and its length (i.e. the number of letters concatenated). Additionally to that, bioobjects are described by properties (e.g. GO-Terms) and associated with features or events (e.g. protein domains, SNVs or splice events). 
- Assemblies: Genome, transcriptome or proteome assemblies are aggregations bioobjects (i.e. nucleotide or protein sequences), nowadays mostly from data generated by high-throughput experiments followed by computational approaches. Assemblies are semantically described by a title and a version number. Additionally, properties (see below) can be assigned to annotate the assembly, for example how the data was generated and how it has been processed.
- Experiments: Our understanding of a biological experiment is based on the MINSEQE draft proposal (http://www.mged.org/minseqe/). Semantically, it is described by a title, a short summary, one or more references, the underlying biological system, experimental factors and additional properties (see below). Samples that were taken within the experiment, as well as contrasts that can be used to contrast experimental variables or factors are described below.
- Samples: Samples are taken within experiments and are semantically described by a title and a list of additional properties assigned to the sample. Furthermore, a list of measurements for a biological object, measured values (e.g. from gene expression experiments), associations (e.g. from protein interaction experiments) as well as a features (e.g. from epigenomic studies) can be given.

Furthermore, three helpful terms are defined:

- Properties: A property is a term-value pair that annotates its context. For example, a GO-Term (term) assigned to a gene (context) might be a property. 
- Features: Features have a start and end position along the bioobject's sequence they are attached to. They may have a strand, a type and a description or a reference to another describing entity. Features can be used to encode concepts like protein-domains, SNPs, methylathed regions and many more.
- Contrasts: Attached to an experiment, a contrast enables comparison of samples with different flavours of an experimental factor. They are semantically described by a title, the experimental factor or variable used and additional filters on other experimental factors.

## general profile description

- All collections provide several hypermedia controls, like search, create and update.
- Profiles do not include explicit accession numbers as semantic descriptors, since the URL can be used as accession and defines the resource.
- Since some key entities may have multiple accessions, a canonical link may be provided.
- Some profiles enable the inclusion of safe state transitions (links). This enables interconnection between key entities and to other web resources and allows for hierarchical models.
- Base descriptors are free floating (non-containered) because of the highly varying understanding in the field.
- Although properties, features and contrast may not be independent resources, they have profiles for easier inclusion into other collections.

## Open questions

- Since hypermedia control is only available as search, edit-form and create-form relations, I'm asking myself if hypermedia control needs seperate profiles?
- Currently, there is a mixture of related and up relations. I somehow need to model hierarchy between different representations - maybe there is a better way to do so.

Contribution and contact
========================

## How to contribute?

Feel free to fork this repository, add your changes and send me a pull request.

## Contributors
Jens Preussner
Mike Amundsen

## Contact

Feel free to contact me via e-mail (jens.preussner@mpi-bn.mpg.de)
