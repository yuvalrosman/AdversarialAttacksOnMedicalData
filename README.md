# AdversarialAttacksOnMedicalData
<img src='/images/models.png'>

This repository contains the implementation of adversarial attack methods targeting MedShapeNet's 3D meshes. The code is designed to manipulate and perturb the mesh data in a way that degrades the performance of machine learning models trained on this dataset, specifically reducing their classification accuracy. The generated adversarial examples can be used for further research into the robustness and security of mesh-based neural networks, aiding in the development of more resilient models.

## SIGGRAPH ASIA 2020 [[Paper]](https://arxiv.org/abs/2006.05353)
Created by [Yuval Rosman](mailto:yuvalrosman6@gmail.com) and [Ben Volovelsky](mailto:benvolovel@gmail.com).

This repository contains the implementation of [MeshWalker](https://arxiv.org/abs/2006.05353) and [Random-Walks-for-Adversarial-Meshes](https://github.com/amirbelder/Random-Walks-for-Adversarial-Meshes).

## Data
Note for this README: replace `<dataset>` with `medshapenet`.


### Raw datasets
To get the raw datasets go to the relevant website, 
and put it under `MeshWalker/datasets_raw/medshapenet`. 
- [MedShapeNet](https://medshapenet-ikim.streamlit.app).


### Processed
To prepare the data, run `python dataset_prepare.py medshapenet`.

Or request the data directly from us. 

Make sure to put the processed dataset in `MeshWalker/datasets_processed/medshapenet`. 
Processing will rearrange dataset in `npz` files, labels included, vertex neighbors added.


## Training
python train_val.py medshapenet


You will find the results at: `MeshWalker\runs\???`

Use tensorboard to show training results: `tensorboard <trained-model-folder>`

Note that "accuracy" tab is a fast accuracy calculated while training, 
it is not the final accuracy we get using averaging.
To get the final accuracy results, please refer to the "full_accuracy" tab at tensorboard, 
or run evaluation scripts.

