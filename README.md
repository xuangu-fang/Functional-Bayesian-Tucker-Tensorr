# Functional-Bayesian-Tucker-Tensor

This authors' official PyTorch implementation for paper:"**Functional Bayesian Tucker Decomposition for Continuous-indexed Tensor Data**"[[OpenReview]](https://openreview.net/forum?id=ZWyZeqE928&referrer=%5BAuthor%20Console%5D(%2Fgroup%3Fid%3DICLR.cc%2F2024%2FConference%2FAuthors%23your-submissions))[[Arxiv](https://arxiv.org/abs/2311.04829)] (ICLR 2024).

---
#### Key Idea:  Decompose Continuous-indexed Tensor Data as mode-wise latent functions in Tucker format


<div align=center> <img src="figs/FunBat-illustration.PNG" width = 100%/> </div>


Each function is modeled as a group of State-Space Gaussian Processes(SSGPs): 
<div align=center> <img src="./figs/funbat-eq1.PNG" width = 100%/> </div>

---




Example of latent functions of spatial and temporal modes learned from real-world data.
<div align=center> <img src="./figs/FunBat.PNG" width = 100%/> </div>
<div align=center> <img src="./figs/FunBat-time.PNG" width = 50%/> </div>

## Requirements:
The project is mainly built with **pytorch 1.13.1** under **python 3.10**. Besides that, make sure to install [tqdm](https://tqdm.github.io/) and [tensorly==0.70](http://tensorly.org/stable/index.html) before running the project. The detailed package info can be found in requirement.txt.

## Instructions:
1. Clone this repository.
2. To play with the model quickly, we offer several notebooks at `notebook`(on synthetic & real data)
3. To run the real-world datasets with scripts, see `script_Funbat.sh` and `script_Funbat_CP.sh` for example.
4. To tune the (hyper)parametrs of model, modify the `.yaml` files in `config` folder
5. To apply the model on your own dataset, please follow the [process_script](https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/process_script). or [generating-synthetic-data](data/synthetic/simu_data_generate_CP_r1.ipynb) to process the raw data into appropriate format.
6. GPU choice: the models are run on CPU by default, but you can change the device to GPU by modifying the `device` as `gpu` of `.yaml` files in the `config` folder.


## Data

We offer the [raw data](https://drive.google.com/drive/folders/1DQJFZ9IkKw9pzr_vBSCLnrzqn4dp4kBd?usp=drive_link), [processed scripts](https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/process_script), and processed data([Beijing](https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/beijing),[US-TEMP](https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/US-Temp)) for all four datasets used in paper. The code for generating the synthetic data is also provided in the [data]( https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/synthetic) folder.


If you wanna customize your own data to play the model, please follow the [process_script](https://github.com/xuangu-fang/Functional-Bayesian-Tucker-Decomposition/tree/master/data/process_script).


## Citation


Please cite our work if you would like it
```
@article{fang2023functional,
  title={Functional Bayesian Tucker Decomposition for Continuous-indexed Tensor Data},
  author={Fang, Shikai and Yu, Xin and Wang, Zheng and Li, Shibo and Kirby, Mike and Zhe, Shandian},
  journal={arXiv preprint arXiv:2311.04829},
  year={2023}
}
```

```
TBD

