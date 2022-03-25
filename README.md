# BERT_models_v1

This repository contians the code and the data for the relation extraction work. 

Running the code
========================================
The code can be run in Google Colab with GPU runtime.

 .sent and .pointer files: The .sent files contain the sentences and the corresponding locations of entities and triples.

1. Converting into BERT embeddings: Run the code helper.py. The BERT embeddings will be generated.

   Example: python3 helper.py train.sent train.pointer train_bert.sent train_bert.pointer train_bert.pos 
   
   Similarly for test and dev file.
   
2. Running the code: Run the code matbert_ptrnet_decoder.py for MatBERT. The parameters are as follows:

   python3 [Program file] [CUDA device used] [seed] [job mode (train or test)] [batch size] [number of epoch] [type of nn (bi-directional or not etc.)] [order of triples (random or not)] [update BERT]
   
   Example: python3 bert_ptrnet_decoder.py 0 1023 train 32 50 0 0 0
            python3 bert_ptrnet_decoder.py 0 1023 test 32 50 0 0 0
   
   
   
   
   


