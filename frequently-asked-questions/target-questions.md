# Target Questions

### **Where can I find more details on the target prediction?**

More details can be found in this [Blog post](https://chembl.blogspot.com/2020/01/new-chembl-ligand-based-target.html). Target predictions can be found on the interface and predictions can be run using this [Docker image](https://hub.docker.com/repository/docker/chembl/mcp).&#x20;

### What are the main target types in ChEMBL?

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### **How can I find the binding site of my compound?**

We annotate binding site information in two different ways:

1\) For drugs and clinical candidates, where the target is a protein complex and we know which subunit(s) the drug binds to, we indicate this by including a site\_id in the drug\_mechanism table. This information can be viewed on the ChEMBL interface through the Drug Mechanisms view where the data is found in the Binding\_site\_name and Binding\_site\_comment fields.

2\) For assay/bioactivity data, we have an algorithm that attempts to predict the most likely binding-domain of the protein target (based on the domain structure of the protein and a list of all curated known small molecule binding domains). This algorithm is only applied to a subset of the > 15 million bioactivity records - binding or functional assays with a single protein or protein complex targets and dose-response measurements - and is not able to make an unambiguous prediction in all cases. There are around 650 K activity measurements with a predicted domain in the predicted\_binding\_domains table.&#x20;

### **How can I find the Pfam domains for my target?**

Pfam-A domains can be found in the domains table and can be viewed in the Domain Cross References section of the target report card on the ChEMBL interface.

### **What does the target relationship\_type flag mean?**

The relationship\_type flag provides the relation between the reported target in the source document and the assigned target.\
\
D          Direct protein target assigned\
H          Homologous protein target assigned\
M         Molecular target other than protein assigned\
N          Non-molecular target assigned\
S          Subcellular target assigned\
U          Default value - Target has yet to be curated

### **How can I find Entrez\_IDs for my ChEMBL targets?**

UniProt accessions are the main identifier for protein targets. These can be mapped to Entrez IDs using the [UniProt mapping tool](https://www.uniprot.org/uploadlists/).  ChEMBL protein targets may be a single protein (with a single accession) or a protein complex, protein family (with more than one associated accession).
