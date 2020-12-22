To train the Pfam_EMB:
	+ Download pfam_ft_emb file from https://drive.google.com/file/d/1ZSgAUXjO-K0qXkqggcuG8oQK805aQ59t/view?u…
	+ Unzip and move to pfam_ft_emb folder. Then run the command to train a model with vector size of dim_size:
		python app.py --dim <dim_size> --output <path_to_output_directory>
	
	Example: running the command "python app.py --dim 8 --output D:\>Glycosite_Pfam" will generate
	D:\Glycosite_Pfam\emb_8.bin which is an amino acid embedding generator or model. The embedding vectors created by
	emb_8.bin have a size of 8
	
Next, the trained Pfam_EMB model can be used for querying. For example:

	+ To load a trained model, which was saved on disk as a binary file:
		import fasttext
		model = fasttext.load_model("D:\Glycosite_Pfam\emb_8.bin")
		
	+ To print our all words in the vocabulary (amino acid), sorted by decreasing frequency of a model, execute:
		model.words
		
	+ To get an embedding vector for an amino acid A:
		model.get_word_vector("A")
		
For more information about how to train and use a language model with fastText, please refer to 
https://fasttext.cc/docs/en/unsupervised-tutorial.html
		
	
	