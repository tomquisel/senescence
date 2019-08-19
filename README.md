## Summary

This is an exploration of genes that are related to cellular senescence. It found a [list of genes](https://docs.google.com/spreadsheets/d/1MsvinkQ6UlP7HwxD_w7Fn-wa5G6AXQQC4Uka8uhdSec/edit#gid=1148360109) that are not yet in the CellAge database but are likely to be involved in senescence. These genes are good candidates for experimental verification. A literature review showed that the top 3 candidates already have some evidence linking them to senescence.

See the [full notebook](https://nbviewer.jupyter.org/github/tomquisel/cellage/blob/master/exploration.ipynb) for details.

## Data

It uses data from the following sources:

* [CellAge](https://genomics.senescence.info/cells/): Maintains a list of genes labeled either as pro-senescence or anti-senescence. These labels are experimentally verified. At the time of analysis, it included 153 genes that promote cellular senescence and 121 genes that inhibit it.
* [Gene Ontology Database](http://geneontology.org/): Maintains a database of cellular components, biological processes, and molecular functions that genes are involved in. Genes are labeled with a list of terms.

## Analyses

### Functional Enrichment of GO terms

This is a traditional analysis that identifies Gene Ontology (GO) terms that are over-represented in genes involved in cellular senescence.

### Gene senescence classifier

This analysis trained several machine learning models that classify whether a gene is involved in cellular senescence or not based on the GO terms for the gene. An ElasticNet classifier achieved 0.82 AUC. See the [report](https://docs.google.com/spreadsheets/d/1MsvinkQ6UlP7HwxD_w7Fn-wa5G6AXQQC4Uka8uhdSec/edit#gid=1782163090).

### Promoter / inhibitor classifier

This analysis aimed to classify whether a senescence-related gene promotes or inhibits senescence, based on the GO terms for the gene. It proved a more difficult task, partially because the training dataset is small. An ElasticNet classifier achieved 0.66 AUC. See [report](https://docs.google.com/spreadsheets/d/1MsvinkQ6UlP7HwxD_w7Fn-wa5G6AXQQC4Uka8uhdSec/edit#gid=1115444922).
