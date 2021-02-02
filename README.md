# Steam StyleGAN2-ADA (PyTorch)

The goal of this repository is to capture the distribution of Steam banners with a StyleGAN2-ADA model (PyTorch).

![Target A][target-A]![Projection A][projection-A]
![Target B][target-B]![Projection B][projection-B]
<sub>
Progression videos of the projection of Steam banners ([*Dog Trainer*][store-link-A] and [*My UnReal pet*][store-link-B]) with a network pre-trained by Nvidia on the `LSUN DOG` dataset.
</sub>

## Data

The [`Steam-OneFace`][steam-oneface] dataset,
obtained with the `retinaface` face detection module:
-   consists of 2.5k Steam banners (256x256 resolution) which should all feature exactly one face,
-   can be downloaded (74 MB) with the following commands:
```bash
!gdown --id 1-0Nk7H6Cn3Nt60EdHG_NWSA8ohi2oBqr
!tar xf steam-oneface-lr_with_retinaface.tar.gz
```

## Usage

-   Run [`training.ipynb`][colab-notebook-training] to train a model from scratch,
[![Open In Colab][colab-badge]][colab-notebook-training]
-   Run [`image_sampling.ipynb`][colab-notebook-sampling] to generate images with a trained model,
[![Open In Colab][colab-badge]][colab-notebook-sampling]
-   To automatically resume training from the latest checkpoint, use [my fork][stylegan2-ada-pytorch-fork] of StyleGAN2-ADA (PyTorch).

## References

-   [Karras, Tero, et al. *Training generative adversarial networks with limited data*. NeurIPS 2020][stylegan2-ada-paper],
-   [Official implementation (PyTorch)][stylegan2-ada-pytorch-repository],
-   Application to Steam banners using the [TensorFlow implementation][stylegan2-ada-applied-to-steam-banners].

<!-- Definitions -->

[target-A]: <https://github.com/woctezuma/steam-stylegan2-ada-pytorch/wiki/img/1113080_target.jpg>
[projection-A]: <https://github.com/woctezuma/steam-stylegan2-ada-pytorch/wiki/img/1113080_crop.gif>
[store-link-A]: <https://store.steampowered.com/app/1113080/>

[target-B]: <https://github.com/woctezuma/steam-stylegan2-ada-pytorch/wiki/img/1315040_target.jpg>
[projection-B]: <https://github.com/woctezuma/steam-stylegan2-ada-pytorch/wiki/img/1315040_crop.gif>
[store-link-B]: <https://store.steampowered.com/app/1315040/>

[steam-oneface]: <https://github.com/woctezuma/steam-filtered-image-data#steam-oneface-dataset>

[colab-notebook-training]: <https://colab.research.google.com/github/woctezuma/steam-stylegan2-ada-pytorch/blob/main/training.ipynb>
[colab-notebook-sampling]: <https://colab.research.google.com/github/woctezuma/steam-stylegan2-ada-pytorch/blob/main/image_sampling.ipynb>
[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>
[stylegan2-ada-pytorch-fork]: <https://github.com/woctezuma/stylegan2-ada-pytorch/tree/google-colab>

[stylegan2-ada-paper]: <https://arxiv.org/abs/2006.06676>
[stylegan2-ada-pytorch-repository]: <https://github.com/NVlabs/stylegan2-ada-pytorch>
[stylegan2-ada-applied-to-steam-banners]: <https://github.com/woctezuma/steam-stylegan2-ada>

