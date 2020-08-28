This is the public site for the paper under submission named: "Incorporating transfer learning technique with amino acid embeddings to efficiently predict 
N_linked glycosylation sites in ion channels"

LIBRARY REQUIREMENTS
	We will need to install some basic packages to run the programs as followed:
		git version 2.15.1.windows.2
		python 3.6.5
		numpy 1.14.3
		pandas 0.23.0
		sklearn 0.20.2


INSTRUCTION:

1. Using git bash to clone all the required files in "YOUR FOLDER" folder git clone https://github.com/khucnam/NIonPred

2. python Predict.py your_fasta_file.fasta ("your_fasta_file.fasta" file contains the sequences you want to classify. Please see the "sample.fasta" as an example.)

----> Running the Predict.py script will generate the Result.csv file. In Result.csv file, there are 2 columms: first one contains the protein ID, 
the next column contaisn a probability that an amino acid is N_linked glycosylated.
