# GroupA-CS586-Fall2020

We performed an ontology matching between ChemOnt and RXNO, using `vocabulary.owl` from PubChem as a mediating ontology.

Files in this repository:
1. `AML_v3.1`: We've placed a copy of AML v3.1 in this repository. This version contains a copy of `vocabulary.owl` pre-loaded as a mediating ontology. The latest version of the original AML can be downloaded from their [GitHub Repository](https://github.com/AgreementMakerLight/AML-Project).
2. `chemont_owl.owl` and `rxno.obo`: Source and target ontologies.
3. `vocabulary.owl`: Mediating ontology from PubChem.
4. `chemont-rxno-vocabulary.tsv`: Mapping result from AML.
5. `chemont-rxno-vocabulary-final.tsv`: Mapping result after manual evaluation of the AML result.
6. `new_ontology.owl`: New ontology made with missed mappings from AML.

Steps to reproduce the results that we observed are given below.

1. Clone this repository:

```
git clone "https://github.com/masood/GroupA-CS586-Fall2020.git"
```

2. Navigate to the AML folder and open AML:
```
cd AML_v3.1
java -jar AgreementMakerLight.jar
```

3. Go to `File`-> `Open Ontologies`.

4. Select `chemont_owl.owl` as the source ontology and `rxno.obo` as the target ontology.

> At this point, you can obseve our matching results by going to `File`-> `Open Alignment` and opening the `.tsv` files.

5. Run the automatic match or custom match to observe varying results.

> The copy of AML included uses `vocabulary.owl` by default. In order to remove this, navigate to `AML_v3.1/store/knowledge` and remove the mediating ontology.

That's it. It's that simple! :)
