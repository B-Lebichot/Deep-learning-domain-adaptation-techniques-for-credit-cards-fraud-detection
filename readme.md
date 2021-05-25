# Code of manuscript: Learning to Classify with Incremental New Class


## Code Structures
To reproduce our experiments with LC-INC, please use **main.py**.

 - `data`: Images and splits for the data sets.
 - `saves`: The pre-trained weights of LC-INC, which can be used to reproduce the experiment results.
 - `main.py`: The main guideline of the detection process.
 - `network.py`: The definition of network structure, including embedding module and structure comparison module.
 - `utils.py`: Useful functions adopted in the code.
 - `DataPrepare.py`: The code to generate strem data from YSneaker dataset.

## Prerequisites
The following packages are required to run the scripts:
- [PyTorch-1.4 and torchvision](https://pytorch.org)
- Dataset: Please download the extracted features of YSneaker via: [this page](https://drive.google.com/file/d/1UgkiBbXuvrCxVXFFaoMhs3o2b1cTYG4q/view?usp=sharing), and put it into the folder `data`.


## Arguments
The main.py takes the following command line options:

**Optimization Related Arguments**
- `initepochs`: The maximum number of initial training epochs, default to `10`
- `lr`: Learning rate for the model, default to `0.01` with pre-trained weights
- `batch`: Batchsize of training, default to `64`
- `embeddingdim`: Dimension of the projected embedding space, default to `64`
- `inputdim`: Dimension of the input dimension
- `buffersize`: The size of the buffer, default to `200`
- `chunksize`: The size of the chunk, default to `500`
- `resume`: To reproduce the results with the pre-trained models, set it to `1` and the model will resume our pre-trained models.






