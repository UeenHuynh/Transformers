# Pytorch-Transformers-Classification


This repository is based on the [Pytorch-Transformers](https://github.com/huggingface/pytorch-transformers) library by HuggingFace. It is intended as a starting point for anyone who wishes to use Transformer models in text classification tasks.

Check out the new library [simpletransformers](https://github.com/ThilinaRajapakse/simpletransformers) for one line training and evaluating!

Table of contents
=================

<!--ts-->
   * [Setup](#Setup)
      * [With Conda](#with-conda)
   * [Usage](#usage)
      * [Yelp Demo](#yelp-demo)
      * [Evaluation Metrics](#evaluation-metrics)
   * [Acknowledgements](#acknowledgements)
<!--te-->

### With Conda

1. Install Anaconda or Miniconda Package Manager from [here](https://www.anaconda.com/distribution/)
2. Create a new virtual environment and install packages.  
`conda create -n transformers python=3.11.11`  
`conda activate transformers`  
If using cuda:  
  `conda install pytorch cudatoolkit=10.0 -c pytorch`  
else:  
  `conda install pytorch cpuonly -c pytorch`  
`conda install -r requirements`  
3. Clone repo.
`https://github.com/UeenHuynh/Transformers.git`

## Usage

### Yelp Demo

This demonstration uses the Yelp Reviews dataset.

Linux users can execute [data_download.sh](data_download.sh) to download and set up the data files.

If you are doing it manually;

1. Download [Yelp Reviews Dataset](https://s3.amazonaws.com/fast-ai-nlp/yelp_review_polarity_csv.tgz).
2. Extract `train.csv` and `test.csv` and place them in the directory `data/`.

Once the download is complete, you can run the [data_prep.ipynb](data_prep.ipynb) notebook to get the data ready for training.

Finally, you can run the [run_model.ipynb](run_model.ipynb) notebook to fine-tune a Transformer model on the Yelp Dataset and evaluate the results.

### Evaluation Metrics

The evaluation process in the [run_model.ipynb](run_model.ipynb) notebook outputs the confusion matrix, and the Matthews correlation coefficient. If you wish to add any more evaluation metrics, simply edit the `get_eval_reports()` function in the notebook. This function takes the predictions and the ground truth labels as parameters, therefore you can add any custom metrics calculations to the function as required.

## Acknowledgements

None of this would have been possible without the hard work by the HuggingFace team in developing the [Pytorch-Transformers](https://github.com/huggingface/pytorch-transformers) library.
