This folder contains all the input data used to identify sub-networks in E. coli iJO1366 model,i.e.,

1. Genome-scale metabolic model *i*JO1366 in *SBML* format
2. Directed Bipartite graph of *i*JO1366 generated using our implementation as ".gpickle" file. Since our implementation renames the entries in the model, we also have an additional ".pickle" file called "iJO1366_namemap.pickle". This pickle file consists of a Python dictionary which consists of the mapping between different identifiers in the model and the renamed entities.
The directed bipartite graph and the namemap can be read in python by using the following command:

	```python
	from networkx as import read_gpickle
	from cPickle import load
	G = read_gpickle("iJO1366.gpickle")
	with open("iJO1366_namemap.pickle", "r") as f:
		namemap = load(f)
	```

	Note that this requires the package [NetworkX](https://networkx.github.io/)

3. List of seed metabolites including the source and the target metabolites
4. Cutoff - 15
