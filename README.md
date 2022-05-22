# Extending-Source-Code-Summarization-using-transformers

Final Project for Course 533 natural Language Processing Rutgers University.

Source code summarization can be explained as generating a readable summary that describes the functionality of a program. to solve this problem, it is critical to understand code rep- resentation by modeling the pairwise link be- tween code tokens in order to reflect their long- term dependence. We have explored the transformer model approach to generate summary based on the self-attention mechanism. Previous works have shown that this approach works better than the state-of-the-art techniques by a significant margin. To improve on it, we used the CuBERT tokenizer to generate tokens from the dataset. We were able to achieve better results than that of the previous work. We also experimented by adding the Diverse Beam Search for inference, instead of the Beam Search used before.


## Installing C2NL

You may consider installing the C2NL package. C2NL requires Linux and Python 3.6 or higher. It also requires installing PyTorch version 1.3. Its other dependencies are listed in requirements.txt. CUDA is strongly recommended for speed, but not necessary.

git clone this repository

Run the following commands to clone the repository and install C2NL:

cd NeuralCodeSum; pip install -r requirements.txt; python setup.py develop

## For Python Data generation

Use the CuBERT token generator file for gernerating the tokens and replace it with the original tokens.

For the token generation use the following repository:

## https://github.com/Sahilraut17/CubertImplementation.git

Then:

$ cd data/python and run the script get_data.sh

## Training/Testing Models

We provide a RNN-based sequence-to-sequence (Seq2Seq) model implementation along with our Transformer model. To perform training and evaluation, first go the scripts directory associated with the target dataset.

$ cd  scripts/DATASET_NAME

Where, choices for DATASET_NAME are ["java", "python"].

To train/evaluate a model, run:

$ bash script_name.sh GPU_ID MODEL_NAME

For example, to train/evaluate the transformer model, run:

$ bash transformer.sh 0,1 code2jdoc


## Acknowledgement
 
We borrowed and modified code from  Github wasiahmad /
NeuralCodeSum . We would like to expresse our gratitdue for the authors of these repositeries and paper.
Citation

@inproceedings{ahmad2020summarization,
 author = {Ahmad, Wasi Uddin and Chakraborty, Saikat and Ray, Baishakhi and Chang, Kai-Wei},
 booktitle = {Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics (ACL)},
 title = {A Transformer-based Approach for Source Code Summarization},
 year = {2020}
}

