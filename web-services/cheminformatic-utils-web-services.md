# Cheminformatic Utils Web Services

ChEMBL Chemoinformatic Utils (aka **'ChEMBL Beaker'**) is a set of useful utility web service tools that provide RESTful access to commonly used cheminformatic methods. Many of them utilise the [RDKit cheminformatics library](http://www.rdkit.org/). The ChEMBL Beaker tools can be tested interactively at [https://www.ebi.ac.uk/chembl/api/utils/docs](https://www.ebi.ac.uk/chembl/api/utils/docs). They include:

* Chemical structure standardisation tools (e.g. check, getParent, standardize; see [Bento et al.](https://github.com/chembl/ChEMBL\_Structure\_Pipeline))
* Physico-chemical property calculation (e.g. molecular weight, heavy atom count, number of hydrogen bond donors / acceptors, number of aromatic rings, etc)
* Chemical structure format converters (e.g. molfile to SMILES, InChI to InChIKey, etc)
* Other tools for structural alerts, molecule similarity and molecule display\


## Chemical Structure Standardisation

| check       | Checks a molecule for issues using ChEMBL Structure Pipeline functionality. The input (CTAB) is either a single molfile or an SDF file. |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| exclude     | Checks if the structure will be excluded from ChEMBL. The input (CTAB) is either a single molfile or an SDF file.                       |
| getParent   | Removes salt/solvates using ChEMBL Structure Pipeline functionality.  The input (CTAB) is either a single molfile or an SDF file.       |
| standardize | Standardises a molecule using ChEMBL Structure Pipeline functionality. The input (CTAB) is either single a molfile or an SDF file.      |

\


## Physico-chemical property calculation

| chemblDescriptors | Returns selected physico-chemical descriptors that are available in ChEMBL (except the pKa related ones). The input (CTAB) is either a single molfile or an SDF file. |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| descriptors       | Returns all physico-chemical descriptors calculated by RDKit for a compound. The input (CTAB) is either a single molfile or an SDF file.                              |

\


## Chemical structure format converters

| canonicalizeSmiles | Converts SMILES to canonical SMILES. This method accepts single or multiple SMILES or \*.smi file.                                                                                 |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ctab22D            | Generates 2D coordinates for a molecule using Schrodinger's coordgen. The input (CTAB) is either a single molfile or an SDF file.                                                  |
| ctab2inchi         | Converts CTAB to an InChI. The input (CTAB) is either a single molfile or an SDF file.                                                                                             |
| ctab2inchikey      | Converts CTAB to an InChIKey. The input (CTAB) is either a single molfile or an SDF file.                                                                                          |
| ctab2smarts        | Converts CTAB to SMARTS format. The input (CTAB) is either a single molfile or an SDF file.                                                                                        |
| ctab2smiles        | Converts CTAB to SMILES format. The input (CTAB) is either a single molfile or an SDF file.                                                                                        |
| ctab2svg           | Converts CTAB to a SVG vector graphic. The input (CTAB) is either a single molfile or an SDF file. Size is the optional size of image in pixels (default value is 300 px).         |
| inchi2ctab         | Converts InChI to CTAB. This method accepts one or multiple InChIs.                                                                                                                |
| inchi2inchikey     | Converts InChIs to InChIKeys. This method accepts one or multiple InChis.                                                                                                          |
| inchi2svg          | Converts InChI to a SVG vector graphic. This method accepts single or multiple InChIs. Size is the optional size of image in pixels (default value is 300 px).                     |
| molExport          | Implements Marvin 4 js MolConvert web service. Converts a compound from one format to another, including Marvin's \*.mrv.                                                          |
| smarts2Ctab        | Converts SMARTS to CTAB. This method accepts single or multiple SMARTS.                                                                                                            |
| smiles22D          | Generate 2D coordinates from SMILES using Schrodinger's coordgen. The input (CTAB) is either a single molfile or an SDF file.                                                      |
| smiles2ctab        | Converts SMILES to CTAB. This method accepts single or multiple SMILES or an \*.smi file.                                                                                          |
| smiles2inchi       | Converts SMILES to InChI. This method accepts single or multiple SMILES or an \*.smi file.                                                                                         |
| smiles2inchikey    | Converts SMILES to InChIKey. This method accepts single or multiple SMILES or an \*.smi file.                                                                                      |
| smiles2svg         | Converts SMILES to a SVG vector graphic. This method accepts single or multiple SMILES or an \*.smi file. Size is the optional size of image in pixels (default value is 300 px).  |

\


## Substructure & similarity & molecule display

| cipStereoInfo              | Implements Marvin 4 js Stereo Info web service. Marks possible stereocenters, R/S chirality for atoms and cistrans bonds.                                                                                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| clean                      | Implements Marvin 4 js clean2D/3D web service. Recomputes 2D/3D coordinates of given compound. The compound is in Marvin's \*.mrv format. Dim is an optional parameter specifying if 2D or 3D coordinates should be computed.                                                  |
| highlightCtabFragmentSvg   | Converts SMILES to a SVG vector graphic with a highlighted fragment described as SMARTS. SMARTS describes the fragment to be highlighted. The input (CTAB) is either a single molfile or an SDF file. Size is the optional size of image in pixels (default value is 300 px).  |
| highlightSmilesFragmentSvg | Converts SMILES to a SVG vector graphic with a highlighted fragment described as SMARTS. This method accepts SMARTS and single or multiple SMILES or an \*.smi file. Size is the optional size of image in pixels (default value is 300 px).                                   |
| hydrogenize                | Implements Marvin 4 js Hydrogenize web service. Adds or removes hydrogen atoms. The compound is in Marvin's \*.mrv format. Dim is an optional parameter specifying if 2D or 3D coordinates should be computed                                                                  |
| Is3D                       | Checks if a molecule has any 3D coordinates. The input (CTAB) is either a single molfile or an SDF file.                                                                                                                                                                       |
| mcs                        | Returns the Maximum Common Substructure of a set of compounds. This method accepts compounds in SDF format.                                                                                                                                                                    |
| removeHs                   | Removes any hydrogens from the graph of a molecule. The input (CTAB) is either a single molfile or an SDF file.                                                                                                                                                                |
| sdf2SimilarityMapSvg       | Generates a similarity map, which is a way to visualise the atomic contributions to the similarity between molecules. This method requires an SDF file containing exactly two molecules.                                                                                       |
| smiles2SimilarityMapSvg    | Generates a similarity map, which is a way to visualise the atomic contributions to the similarity between molecules. This method requires exactly two SMILES strings                                                                                                          |
| structuralAlerts           | Get structural alerts for a compound. The input (CTAB) is either a single molfile or an SDF file.                                                                                                                                                                              |

## ChEMBL Beaker Status

| status | Provides information about the status of Beaker web services. A response code of 200 means that it is up and running. Returns the ChEMBL Beaker version information. |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

