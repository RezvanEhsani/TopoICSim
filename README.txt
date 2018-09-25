TopoICSim

Description:

The semantic similarity between two genes and gene lists based on their Gene Ontology Annotations (GOA) 
have become an important part for many of bioinformatics analysis and tools.TopoICSim is a software written 
in R for semantic similarity computation between genes and gene groups.


Prerequisites:

R version >= 3.3.3
GOSemSim >= 2.0.4
graph >= 1.52.0
RBGL >=1.50.0
igraph >= 1.1.2
Rgraphviz >= 2.18.0
GO.db >= 3.4.0


Running the software:

TopoICSim <- function(GeneList1, GeneList2, ont="MF", organism="human", drop=NULL){

Use main function "TopoICSim" where inputs and outputs are as following:

* Input:  
   1.GeneList1; a list of Entrez Gene ID.
   2.GeneList2; a list of Entrez Gene ID.
   3.ont; Ontology type (MF or BP).
   4.organism; options:"human", "fly", "mouse", "rat", "yeast", "zebrafish", "worm", "arabidopsis", "ecolik12",
                       "bovine", "canine", "anopheles", "ecsakai", "chicken", "chimp", "malaria", "rhesus", 
			"pig", "xenopus"
   5.drop; options:"IEA", "IEP", "IGC", "IGI", "IMP", "IPI", "ISA", "ISM", "ISO", "ISS", "NAS", "ND", "RCA", "TAS", NULL

* Output:
   1.a numeric value between 0,1 thatis semantic similarity between GeneList1 and GeneList2.


For example, to measure semantic similarity by TopoICSim for two human genes 218 and 501, 
you should use the following command:
>TopoICSim("218", "501", ont="MF", organism="human", drop=NULL)

Please cite the following article when using TopoICSim:
Ehsani R and Drabløs F:TopoICSim: A new semantic similarity measure based on gene ontology. BMC Bioinformatics 2016, 17:296.




