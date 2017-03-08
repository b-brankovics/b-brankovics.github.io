---
layout: project
title: Return of the Mitochondrial DNA
date:   2016-11-18 15:29:36 +0100
permalink: /projects/return_of_the_mitochondrial_dna/
---

> This is a project associated with a [poster](https://b-brankovics.github.io/files/Return_of_the_mitochondrial_DNA.pdf) presented at the
> 29th Fungal Genetics Conference (14-19 March 2017, Pacific Grove,
> CA, USA). It contains more information on the methods used than the
> poster itself. You can also find a downloadable copy of the poster
> here and links to related information (entry on ResearchGate and
> GitHub repositories).

In the 1990s, the barcoding of life project was started, aiming to use
a single sequence to identify animals, fungi and plants to the species
level. The first marker that was proposed was a mitochondrial marker:
the mitochondrially encoded cytochrome oxidase I (_cox1_ in
filamentous fungi). 

However, amplifying the _cox1_ sequence proved problematic in many
fungal groups, because the frequent insertions of introns into the
region made universal primer design difficult. Hence, the
mitochondrial marker was abandoned and the barcoding community chose
the ITS region as official barcode for fungi.
Unfortunately, the ITS barcode proved to have insufficient resolution
in many closely related species. Thus, multi-locus analysis became the
new standard, most of which included at least one mitochondrial
marker. There has been no consensus on which mitochondrial loci to
include.


With next generation sequencing and new assembly tools it is possible
to assemble the complete mitochondrial genome of isolates, which
provide all the benefits that are associated with using mitochondrial markers.
In addition, using the complete mitochondrial genome offers better
resolution for phylogenetic analyses and with sufficient sampling it can be
placed in the context of previous works done on mitochondrial barcoding markers.

[Download the poster](http://localhost:4000/files/Return_of_the_mitochondrial_DNA.pdf)

## Take home message

- Mitochondrial genomes can be efficiently assembled from NGS data
- It is feasible to analyze the mitogenome of a large number of
strains
- Complete miotgenomes offer sufficient information to delineate even
closely related species
- A detailed analysis of the mitogenomes may offer new insights into
the biology of the organism
- Complete mitochondrial genomes should be added to whole genome
  sequencing projects

## Methods

All the different regions used for the analysis was assembled using
[**GRAbB**](#external-links). GRAbB is a program designed to assemble
selected regions of the genome or transcriptome using reference
sequences and NGS data.

Phylogenetic species were identified using the programmatic
implementation of the genealogical concordance phylogenetic species
recognition ([**GCPSR**](#external-links)).

_More details are coming after the publication of the research
article. Until then, if you wish to know more about the methods, feel
free to contact me via ResearchGate, LinkedIn or GitHub._


## Reference
> The article that was used as reference is not yet published.
> So the citation information below is temporary and will be updated
> when the work is published.

Brankovics, Balázs, van Dam, Peter, Rep, Martijn, de Hoog, G. Sybren,
van der Lee, Theo A. J., Waalwijk, Cees and van Diepeningen, Anne D.
Mitochondrial genomes reveal recombination in the presumed asexual
_Fusarium oxysporum_ species complex. (Under review)

## External links
* [The poster on ResearchGate](https://researchgate.net)
* [GRAbB on GitHub](https://github.com/b-brankovics/grabb)
* [The article describing GRAbB](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004753)
* [Automated GCPSR on GitHub](https://github.com/b-brankovics/GCPSR)
* [The fasta\_tools package on GitHub](https://github.com/b-brankovics/fasta_tools)
* [LinkedIn profile](https://nl.linkedin.com/in/balazs-brankovics)
