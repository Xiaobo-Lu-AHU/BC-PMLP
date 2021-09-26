BC-PMLP
=======
The source code of transfer learning for recommendation system.

Environment Settings
---------------------
The general environment of the experiment is given as follows： 

- Python 3.5
- torch 1.4.0
- some necessary packages.
	
Interpretation and description
------------------------------
For each file in this folder, including code and data, we will give the following explanation:

    - Folder BC-PMLP: 
	    Folder data: Store the feature vectors trained by BC and derived from SVD++ in the form of dictionary;
	    Code BC_PMLP.py: Store the construction code of PMLP (called REG) and the prediction code of BC (called CLA);
	    Code Dataset.py: Some data preprocessing functions. If you run this code directly, this function file will not work;
	    Code run.py: There is a main function inside。
		
    - Folder Data: One test data and one training data are stored in it. We do not provide the original data in the whole folder, but only the encoded and segmented processed data.
    - Folder SVD++: 
	    Folder data: Representation vectors of all users and items trained from SVD++ algorithm are stored, which are also the input of BC-PMLP;
	    Code SVD++.py: The source code of SVD++ algorithm, most of which comes from the Internet.

More details about the code are given in the form of comments in the code file.

Examples of running codes
-------------------------
In the context of appropriate configuration requirements, you can successfully run a set of experimental results with the following instructions：
```
python run.py
```
The parameter values required for program operation can be modified in the source code. The best empirical values of parameters are given in our paper.

We provide the vector file `SVD++_emb_file` trained by SVD++ algorithm to help you directly transfer. If you want to complete the training process of SVD++, you can execute the following code:
```
python SVD++.py
```
Later, the program will generate the same file based on the training data.
