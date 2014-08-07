bioalps
=======

This repo contains a proposal for ALPS profiles in the genome/bioscience domain. Profiles are drafts and will very likely change in the next few weeks.

The genome/bioscience domain
============================

- Assemblies: Genome and/or transcriptome assemblies are aggregations of in-silico created nucleotide sequences, nowadays mostly from high-throughput sequencing. A representation of an assembly is (semantically) described in its current draft by a URL (its accession), a title and a version number. Additionally, properties (later described in the bioproperties profile) can be assigned to annotate the assembly, as well as safe transitions to sequence representations. Assembly collections provide several hypermedia controls, like search, create and update. 

bioassembly profile
===================

## Description

- Base descriptors are free floating (non-containered) because of the highly varying understanding in the field.
- A semantic descriptor points to the (later described) bioproperties profile.
- A safe transition allows fetching representations of sequences (later described as bioobjects).
- Hypermedia controls return assemblies itself.

## Open questions

- Although base descriptors are free floating, I added a container that is returned by the state transitions. I'm not sure if this is neccessary or if returning an "item" is sufficient.
- There might be a clash between the assemblies item descriptor and the bioobjects item descriptor. I'm still looking for a good way to include a safe transition to another representation (Basically its about modelling the hierarchical nature of the problem space)
- Maybe I even don't need the descriptors inside the transitions?

