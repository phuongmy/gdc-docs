# Gene and Mutation Summary Pages

Many parts of the GDC website contain links to Gene and Mutation summary pages.  These pages display information about specific genes and mutations, along with visualizations and data regarding their interactions between themselves and the projects and cases within the GDC.

## Gene Summary Page

The Gene Summary Page describes each gene with mutation data featured at the GDC and provides results related to the analyses that are performed on these genes.  

### Summary

The summary section of the gene page contains the following information:

[![Gene Summary](images/GDC-Gene-Summary.png)](images/GDC-Gene-Summary.png "Click to see the full image.")

* __Symbol:__ The gene symbol
* __Name:__ Full name of the gene
* __Synonyms:__ Synonyms of the gene name or symbol, if available
* __Type:__ A broad classification of the gene
* __Location:__ The chromosome on which the gene is located and its coordinates
* __Strand:__ If the gene is located on the forward (+) or reverse (-) strand
* __Description:__ A description of gene function and downstream consequences of gene alteration
- __Annotation:__ A notation/link that states whether the gene is part of [The Cancer Gene Census](http://cancer.sanger.ac.uk/census/)

### External References

A list with links that lead to external databases with additional information about each gene is displayed here. These external databases include: [Entrez](https://www.ncbi.nlm.nih.gov/gquery/), [Hugo Gene Nomenclature Committee](http://www.genenames.org/), [Online Mendelian Inheritance in Man](https://www.omim.org/), and [Uniprotkb SwissProt](http://www.uniprot.org/).

### Cancer Distribution

[![Cancer Distribution](images/GDC-Gene-CancerDist.png)](images/GDC-Gene-CancerDist.png "Click to see the full image.")

A table and bar graph displayed that shows how many cases are affected by mutations within the gene as a ratio and percentage. Each row/bar represents the number of cases for each project.

### Protein Viewer

[![Protein Plot](images/GDC-Gene-ProteinGraph.png)](images/GDC-Gene-ProteinGraph.png "Click to see the full image.")

Mutations and their frequency across cases are mapped to a graphical visualization of protein-coding regions with a lollipop plot. Pfam domains are highlighted along the x-axis to assign functionality to specific protein-coding regions. The bottom track represents a view of the full gene length. Different transcripts can be selected by using the drop-down menu above the plot.  

The panel to the right of the plot allows the plot to be filtered by mutation consequences or impact.  The plot will dynamically change as filters are applied.  Mutation consequence and impact is denoted in the plot by color.

The plot can be viewed at different zoom levels by clicking and dragging across the x-axis, clicking and dragging across the bottom track, or double clicking the pfam domain IDs. The `Reset` button can be used to bring the zoom level back to its original position. The plot can also be exported as a PNG image, SVG image or as JSON formatted text by choosing the `Download` button above the plot.

### Most Frequent Mutations

The 20 most frequent mutations in the gene are displayed as a bar graph that indicates the number of cases that share each mutation.  

[![Gene MFM](images/GDC-Gene-MFM.png)](images/GDC-Gene-MFM.png "Click to see the full image.")

A table is displayed below that lists information about each mutation including:

* __ID:__ A UUID Code for the mutation assigned by the GDC, when clicked will bring a user to the Mutation Summary Page
* __DNA Change:__ The chromosome and starting coordinates of the mutation are displayed along with the nucleotide differences between the reference and tumor allele
* __Type:__ A general classification of the mutation
* __Consequences:__ The effects the mutation has on the gene coding for a protein (i.e. synonymous, missense, non-coding transcript)
* __# Affected Cases in Gene:__ The number of affected cases, expressed as number across all mutations within the Gene.
* __# Affected Cases Across GDC:__ The number of affected cases, expressed as number across all projects. Choosing the arrow next to the percentage will expand the selection with a breakdown of each affected project
* __Impact:__ A subjective classification of the severity of the variant consequence. The categories are:
  - __HIGH__: The variant is assumed to have high (disruptive) impact in the protein, probably causing protein truncation, loss of function or triggering nonsense mediated decay
  - __MODERATE__: A non-disruptive variant that might change protein effectiveness
  - __LOW__: Assumed to be mostly harmless or unlikely to change protein behavior

## Mutation Summary Page

  The Mutation Summary Page contains information about one somatic mutation and how it affects the associated gene. Each mutation is identified by its chromosomal position and nucleotide-level change.

### Summary

  [![Mutation Summary](images/GDC-Mutation-Summary.png)](images/GDC-Mutation-Summary.png "Click to see the full image.")

  - __ID:__ A unique identifier (UUID) for this mutation
  - __DNA Change:__ Denotes the chromosome number, position, and nucleotide change of the mutation
  - __Type:__ A broad categorization of the mutation
  - __Reference Genome Assembly:__ The reference genome in which the chromosomal position refers to
  - __Allele in the Reference Assembly:__ The nucleotide(s) that compose the site in the reference assembly
  - __Functional Impact:__ A subjective classification of the severity of the variant consequence. The categories are:
    - __HIGH__: The variant is assumed to have high (disruptive) impact in the protein, probably causing protein truncation, loss of function or triggering nonsense mediated decay
    - __MODERATE__: A non-disruptive variant that might change protein effectiveness
    - __LOW__: Assumed to be mostly harmless or unlikely to change protein behavior

#### External References

  A separate panel contains links to databases that contain information about the specific mutation. These include [dbSNP](https://www.ncbi.nlm.nih.gov/projects/SNP/) and [COSMIC](http://cancer.sanger.ac.uk/cosmic).

### Consequences

  [![Mutation Consequences](images/GDC-Mutation-Consequences.png)](images/GDC-Mutation-Consequences.png "Click to see the full image.")

  The consequences of the mutation are displayed in a table. The fields that detail each mutation are listed below:

  * __Gene:__ The symbol for the affected gene
  * __AA Change:__ Details on the amino acid change, including compounds and position, if applicable
  * __Consequence:__ The biological consequence of each mutation
  * __Coding DNA Change:__ The specific nucleotide change and position of the mutation within the gene
  * __Strand:__ If the gene is located on the forward (+) or reverse (-) strand
  * __Transcript(s):__ The transcript(s) affected by the mutation. Each contains a link to the [Ensembl](https://www.ensembl.org) entry for the transcript   

### Cancer Distribution

  [![Mutation Distribution](images/GDC-Mutation-CancerDist.png)](images/GDC-Mutation-CancerDist.png "Click to see the full image.")

  The Cancer Distribution table contains information about how the mutation affects each project, which can be exported as a JSON object. The table contains the following fields:

  * __Project ID__: The ID for a specific project
  * __Disease Type__: The disease associated with the project
  * __Site__: The anatomical site affected by the disease
  * __# Affected Cases__: The number of affected cases and total number of cases displayed as a fraction and percentage

### Protein Viewer

  [![Mutation Protein Graph](images/GDC-Mutation-ProteinGraph.png)](images/GDC-Mutation-ProteinGraph.png "Click to see the full image.")

  The protein viewer displays a plot representing the position of mutations along the polypeptide chain associated with the mutation. The y-axis represents the number of cases that exhibit each mutation, whereas the x-axis represents the polypeptide chain sequence. [Pfam domains](http://pfam.xfam.org/) that were identified along the polypeptide chain are identified with colored rectangles labeled with pfam IDs. See the Gene Summary Page for additional details about the protein viewer.