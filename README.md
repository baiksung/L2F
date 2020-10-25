# L2F - Learning to Forget for Meta-Learning 
#### Sungyong Baik, Seokil Hong, Kyoung Mu Lee

Source code for CVPR 2020 paper "Learning to Forget for Meta-Learning"

[Paper](https://arxiv.org/abs/1906.05895)


## Proposed Meta-Learning

<center><img src="./figures/overall_fig.png" width="100%"></center>

## Dataset Preparation

The miniImageNet dataset can be downloaded from the [link](https://drive.google.com/file/d/1qQCoGoEJKUCQkk8roncWH7rhPN7aMfBr/view) provided in [MAML++ github page](https://github.com/AntreasAntoniou/HowToTrainYourMAMLPytorch).

Once downloaded, place it in the datasets folder.

Note: By downloading and using the miniImageNet datasets, you accept terms and conditions found in [imagenet_license.md](https://github.com/baiksung/baiksung/blob/master/imagenet_license.md)

## Results

- Note that the reported results for ResNet12 were trained with **batch size of 1** to fit into **11GB** GPU Memory.
- With more than **22GB memory**, models with ResNet12 backbone can be trained with **batch size of 2** to get higher accuracy.

| Model   | Backbone | Batch Size | 1-shot Accuracy | 5-shot Accuracy |
|---------|----------|------------|-----------------|-----------------|
|MAML     |ResNet12  |1           |   51.03±0.50%   |    68.26±0.47%  |
|MAML+L2F |ResNet12  |1           |**57.48±0.49%**  |  **74.68±0.43%**|
|MAML     |ResNet12  |2           |   58.37±0.49%   |    69.76±0.46%  |
|MAML+L2F |ResNet12  |2           | **59.71±0.49%** |  **77.04±0.42%**|


- 5-way classification results on miniImageNet 

<center><img src="./figures/fig_results.png" width="100%"></center>

## Citation

If you find this code useful for your research, please consider citing the following paper:

``` text
@inproceedings{baik2020learning,
    author = {Baik, Sungyong and Hong, Seokil and Lee, Kyoung Mu},
    title = {Learning to Forget for Meta-Learning},
    booktitle = {CVPR},
    year = {2020}
}
```

## Acknowledgement

The main structure of this code is based on [MAML++](https://github.com/AntreasAntoniou/HowToTrainYourMAMLPytorch).
We thank the authors for sharing the codes for their great works.
