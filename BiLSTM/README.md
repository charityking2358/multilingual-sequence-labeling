## Multilingual Bidirectional Long Short-Term Memory model 
This codebase contains a baseline bidirectional long short-term memory model for predicting part-of-speech tags on a corpus. The model contains language sequence and corresponding part-of-speech labels for 8 different languages: English (en), Afrikaans (af), Czech (cs), Spanish (es), Arabic (ar), Lithuanian (lt), Armenian (hy), and Tamil (ta). <br>
<br>
About the data: The training data used is [Universal Dependency data](https://universaldependencies.org/), a framework for consistent annotation of grammar (parts of speech, morphological features, and syntactic dependencies) across different human languages. 


## Requirements
The installation of conda is required in order to use this conda environmnet. Here are instructions for two ways to get your environment up and running. 
1. Use the Environment .yml file<br>
`conda env create -f environment.yml`

2. Create your own environment<br>
`conda create -n envir_name python=3.8`<br>
`conda activate envir_name`<br>
`conda install numpy`<br>
`conda install pytorch=1.10.1 torchtext=0.11.1 cudatoolkit -c pytorch`<br>
`conda install pandas`<br>
`conda install matplotlib`<br>
`pip install openpyxl`<br>


## Code

### Training
This codebase does not contain any trained models. For the first run, use the follow command line. 
The language codes available are {en, es, cs, ar, af, lt, hy, ta}. <br> 
`python main.py --mode train --lang <language_code>`

### Evaluating
This parameter will load an already trained and saved model, providing details on per-label accuracy. 
All model output per any configuration json will be saved to the `model_evaluation` folder. <br> 
`python main.py --mode eval --lang <language_code>`<br> 




