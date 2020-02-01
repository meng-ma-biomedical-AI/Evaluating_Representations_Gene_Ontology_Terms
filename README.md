
# Encode Gene Ontology terms using their definitions or positions on the GO tree.

## The methods applied are: 

* **Defintion encoder**
  1. BiLSTM 
  2. ELMo
  3. Transformer based on BERT strategy. 
  
* **Position encoder**
  1. GCN
  2. Onto2vec

## The key objective is to capture the relatedness of GO terms by encoding them into similar vectors. 

Consider the example below. We would expect child-parent terms to have similar vector embeddings; whereas, two unrelated terms should have different embeddings. 

![GoTermExampl](Figure/GoTermExample.png)

### Libraries needed

[pytorch](https://pytorch.org/)

[pytorch-pretrained-bert](https://pypi.org/project/pytorch-pretrained-bert/)

[pytorch-geometric](https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html)


### Defintion encoder 

We embed the [definition](https://www.ebi.ac.uk/QuickGO/term/GO:0075295) of a term. The key is that child-parent terms often have simlar defintions, so that we can embed them into comparable vectors. 

All models are already trained, and ready to be used. **[You can download the embeddings here.](https://drive.google.com/drive/folders/129UObLlhnp0RK6MQAS7waUF-k4SuGV-u?usp=sharing)** 

Alternatively, you can also train your own embedding. You only need to prepare your code into the [same format here](https://drive.google.com/drive/folders/1DITbTYg_49lpDu_RmHzY5WVTG7Acp_7B?usp=sharing)


