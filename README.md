bioalps
=======

This repository contains a proposal for ALPS profiles in the genome/bioscience domain. Profiles are drafts and will very likely change in the next few weeks.

The genome/bioscience domain
============================

- Objects/entities: A representation of a bioobject or bioentity is semantically described by a sequence (i.e. a concatenation of letters from an arbitrary alphabet) and by its length (i.e. the number of letters concatenated). Several term-value pairs describe additional properties of bioobjects. Furthermore, features provide description of associated parts of the sequence. Safe state transitions link to other resources, like experiments, parent resources or search, edit and create forms.
- Properties: Representations provide term-value pairs for annotation. 
- Features: Representations describe start and end positions, the strand and type of a biological feature. Start and end positions are meant to be on a bioobject#sequence. Additionally, a description can be provided, as well as a safe state transition to another resource describing the feature in greater detail. 
- Experiments: A representation of a biologicl experiment is described by the experiments title, a short summary, one or more references, the underlying biological system, experimental factors and bioproperties (see above). Safe state transitions link to samples that were taken within the experiment, as well as contrasts that can be used to contrast experimental variables or factors. Furthermore, state transitions to the author(s), a search, create and update form can be included.
- Samples: Representations are described by the samples title and a list of bioproperties assigned to the sample. Furthermore, a list of measurements for a biological entity or object as well as the measured value can be given. Since samples are attached to experiments, a safe state transition refers to the experiment. Sample collections also provide state transitions to search, edit and create forms.
- Contrasts: Used in experiments, a representation of a contrast can include a title, the experimental factor or variable used and additional filters. Safe state transitions can refer to the experiment(s) the contrast is used in and to search, edit and create forms.
- Assemblies: Genome and/or transcriptome assemblies are aggregations of in-silico created nucleotide sequences, nowadays mostly from high-throughput sequencing. A representation of an assembly is (semantically) described in its current draft by a URL (its accession), a title and a version number. Additionally, properties (see above) can be assigned to annotate the assembly, as well as safe transitions to sequence representations. Assembly collections provide several hypermedia controls, like search, create and update. 

## general profile description

- Profiles do not include explicit accession numbers, since the URL can be used as accession and defines the resource. 
- Since some bioobjects may have multiple accessions, a canonical link may be provided.
- Base descriptors are free floating (non-containered) because of the highly varying understanding in the field.
- Hypermedia controls are not fully implemented, but transitions to search, edit and create forms are possible.

## Open questions

- Since hypermedia control is only available as search, edit-form and create-form relations, I'm asking myself if they need seperate profiles?
- Currently, there is a mixture of related and up relations. I somehow need to model hierarchy between different representations - maybe there is a better way to do so.
