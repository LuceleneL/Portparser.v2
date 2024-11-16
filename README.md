# Portparser.v2

Second version of Portparser, a parsing model to perform the annotation following the Universal Dependencies (UD) framework for Portuguese language. texts.

In this repository you have access to the model that can be employed using the latinpipe (https://github.com/ufal/evalatin2024-latinpipe)

# The Available Model
This model is available here and it is composed by the contents of the directory [Portparser_v2_model]().
To use this model with Latin Pipe you need to:
- install Latin Pipe in your machine - see the requirements and instructions at [Latin Pipe page](https://github.com/ufal/evalatin2024-latinpipe);
- copy the directory `Portparser_v2_model` to the same location of your Latin Pipe code file (`latinpipe_evalatin24.py`);
- run Latin Pipe over your CoNLL-U file, for instance `my_file.conllu` (Latin Pipe does not perform tokenization) with the command:
    - `python3.11 latinpipe_evalatin24.py --load Portparser_v2_model/model.weights.h5 --exp annotation --test my_file.conllu`

Latin Pipe requires the absence of errors in the input `.conllu` file, so it is safer to have the input `.conllu` file with only the first two and last columns filled (token ID, FORM, and MISC) and all other columns empty (LEMMA, UPOS, XPOS, FEATS, HEAD, DEPREL, and DEPS).

# Annotation of Textual files
If you do not have a CoNLL-U file of your text to be annotated, you can use the following programs to:
- perform the segmentation of your textual files:
    - https://github.com/LuceleneL/portSentencer
- perform the tokenization of segmented sentences file:
    - https://github.com/LuceleneL/portTokenizer



## File Structure
The files are stored in the following directories:
- `Portparser_v2_model` - the proposed model to be used with Latin Pipe;
- `myFile.conllu` - an example of input (a CoNLL-U file with five sentences in Portuguese).

# Acknowledgments
This work was carried out at the Center for Artificial Intelligence of the University of São Paulo (C4AI - [http://c4ai.inova.usp.br/](http://c4ai.inova.usp.br/)), with support by the São Paulo Research Foundation (FAPESP grant #2019/07665-4) and by the IBM Corporation. The project was also supported by the Ministry of Science, Technology and Innovation, with resources of Law N. 8.248, of October 23, 1991, within the scope of PPI-SOFTEX, coordinated by Softex and published as Residence in TIC 13, DOU 01245.010222/2022-44.

