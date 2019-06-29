---
layout: post
title:  "Glycoscience visibility"
# date:   2019-06-22 19:31:32 +0200
author: "Genadij Razdorov"
categories: [glycoscience, visibility]
---
{% include abbreviations.md %}

Some 10 days ago I had oral presentation titled *Glycoscience visibility* at
[*the 2nd Meeting of the Human Glycome Project*][HGP2019]. I am showing main
results from my presentation in this post.

<!--more-->
![Article set used](/assets/domains.png){:width="30%" align="left"}

We have compared a set of articles Pubmed is returning if searched for *glycan*
with a set of articles more relevant to glycoscience published in last 10
years.
Since Pubmed maps [*Glycan* to *Polysaccharide* MeSH
term](https://www.ncbi.nlm.nih.gov/mesh/?term=glycan),
[*polysaccharides*][poly] was used to denote this set, [*glyco*][glyco] to
denote more relevant set and *random* to denote randomly selected set of
articles representing articles indexed by Pubmed in general.

Venn diagram on the left is showing count and overlap of articles in this three
sets.

[Glyco][] set was constructed searching Pubmed with *glycomics, glycome, 
glycoproteomics, glycoproteome or glycan* in title only.
To make this set even more relevant we have constructed coauthorship network,
were authors are represented as nodes and coauthored articles as edges, for
glyco (on the left) and random (on the right) sets. 

![Coauthorship networks](/assets/coauthorships.png){:width="100%"}

It is evident that [glyco][] network is much more connected. Unconnected
articles in glyco set have been excluded from further analysis.

Next, using [NLP](https://en.wikipedia.org/wiki/Natural_language_processing) we
have extracted *noun phrases* from articles' abstracts per set, and counted
their frequency.
For the glyco and polysaccharides sets enrichment over random set have
been calculated as well.
Top noun phrases (by frequency or enrichment) are shown in next table.

![Top noun phrases](/assets/terms.png){:width="100%"}

It is obvious that top glyco phrases are all derived from *glyco* term, while
top phrases have only one such phrase.

From this results a number of questions about glycoscience visibility and
Pubmed indexing in glycoscience are opened.
For a discussion about this topic please check [issue
#1](https://github.com/the-human-glycome-project/visibility/issues/1).


[poly]: https://www.ncbi.nlm.nih.gov/pubmed/?term=glycan+%E2%80%9Clast+10+year%E2%80%9D%5Bdp%5D
[glyco]: https://www.ncbi.nlm.nih.gov/pubmed/?term=glycomics%5Bti%5D+OR+glycome%5Bti%5D+OR+glycoproteomics%5Bti%5D+OR+glycoproteome%5Bti%5D+OR+glycan%5Bti%5D+%E2%80%9Clast+10+year%E2%80%9D%5Bdp%5D
