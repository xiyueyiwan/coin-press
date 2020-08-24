# CoinPress: Practical Private Mean and Covariance Estimation
A Python implementation of [CoinPress: Practical Private Mean and Covariance Estimation](https://arxiv.org/abs/2006.06618).
CoinPress stands for COnfidence-INterval-based PRivate EStimation Strategy.

Instructions
===
We include a demo for both mean and covariance estimation, the parameters for which can be specified by either command-line arguments, or inside the python script. 

For instance to run the covariance and mean estimation demo for a synthetic dataset with 3000 10-dimensional datapoints and total privacy budget 0.5:

`python demo.py --n 3000 --d 10 --total_budget 0.5`

To see usage details one can run:

`python demo.py --h`


For more examples please see `mean_estimation.py` and `cov_estimation.py`. More complete experiment details can be found in `multivariate_covariance_experiments.ipynb` and `multivariate_mean_experiments.ipynb`, calling on core functions from `algos.py` and `utils.py`. `plot_mean.py` and `plot_cov.py` produce the plots as shown in the paper, using data included in `./results`. This data can be regenerated by running the aforementioned scripts or Jupyter notebooks. Exceptions are the files prefixed by `dfmbg` in `./results/synthetic_mean/`, which are generated using code from Du et al's [repository](https://github.com/wxindu/dp-conf-int).

To run the map of Europe experiments (included our covariance experiments notebook), files from the following are required:
* [Novembre_etal_2008_misc](https://github.com/NovembreLab/Novembre_etal_2008_misc): A repository containing data from [Genes Mirror Geography in Europe](https://www.nature.com/articles/nature07331). Extract the following three files to `./data`: 
    * `POPRES_08_24_01.EuroThinFinal.LD_0.8.exLD.out0-PCA.eigs`
    * `POPRES_08_24_01.EuroThinFinal.LD_0.8.exLD.out0-PCA.eval`
    * `POPRESID_Color.txt`

Reference
===
This repository is an implementation of our paper [CoinPress: Practical Private Mean and Covariance Estimation](https://arxiv.org/abs/2006.06618), authored by [Sourav Biswas](https://sravb.github.io/), [Yihe Dong](https://yihedong.me/), [Gautam Kamath](http://www.gautamkamath.com/), [Jonathan Ullman](http://www.ccs.neu.edu/home/jullman/).
Code contributed by all four authors. 

If you use our code or paper, we ask that you please cite:
```
@article{BiswasDKU20,
  title         = {CoinPress: Practical Private Mean and Covariance Estimation},
  author        = {Biswas, Sourav and Dong, Yihe and Kamath, Gautam and Ullman, Jonathan},
  journal       = {arXiv preprint arXiv:2006.06618},
  year          = {2020}
}
```
