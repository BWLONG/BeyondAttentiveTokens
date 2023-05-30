# BAT

> **Beyond Attentive Tokens: Incorporating Token Importance and Diversity for Efficient Vision Transformers**

This work propose a simple yet effective decoupling and merging method that can simultaneously preserve the most attentive local tokens and diverse global semantics without imposing extra parameters.
To the best of our knowledge, this work is the first to emphasize the token diversity for pruning ViT. We also demonstrate its cruciality through numerical and empirical analysis. 

![intro](imgs/method.png)

# Preparation

Download and extract ImageNet train and val images from http://image-net.org/. The directory structure is the standard layout for the torchvision datasets.ImageFolder, and the training and validation data is expected to be in the train folder and val folder respectively.

```
/path/to/imagenet/
  train/
    class1/
      img1.jpeg
    class2/
      img2.jpeg
  val/
    class1/
      img3.jpeg
    class/2
      img4.jpeg
```

Install the requirements by running:

```
pip3 install -r requirements.txt
```

# Model Zoo

We provide our models pretrained on ImageNet 2012.

| Name | Keep rate | Acc@1 | MACs (G) | #Params | log |
| --- | --- | --- | --- | --- | --- |
| DEiT-S-Ours | 0.7 | 79.6 | 3.0 | 22.1M | [Ours-0.7](./log/Ours-0.7.log) |
| DEiT-S-Ours | 0.6 | 79.3 | 2.6 | 22.1M | [Ours-0.6](./log/Ours-0.6.log) |
| DEiT-S-Ours | 0.5 | 79.0 | 2.3 | 22.1M | [Ours-0.5](./log/Ours-0.5.log) |
| DEiT-S-Ours | 0.4 | 78.6 | 2.0 | 22.1M | [Ours-0.4](./log/Ours-0.4.log) |
| DEiT-S-Ours | 0.3 | 77.8 | 1.8 | 22.1M | [Ours-0.3](./log/Ours-0.3.log) |
| DEiT-S-Ours | 0.2 | 76.4 | 1.6 | 22.1M | [Ours-0.2](./log/Ours-0.2.log) |

## Visualization
The visualization code is modified from [EViT]( https://github.com/youweiliang/evit).

![intro](imgs/result.png)

# License
This repository is released under the Apache 2.0 license as found in the [LICENSE](LICENSE) file.

# Acknowledgement
We would like to thank the authors of  [EViT]( https://github.com/youweiliang/evit) and [Evo-ViT](https://github.com/YifanXu74/Evo-ViT), based on which this codebase was built.

