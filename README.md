# Vision_Transformer
ViT_GenderClassify
https://github.com/lucidrains/vit-pytorch/raw/main/images/vit.gif
Table of Contents
Vision Transformer - Pytorch
Install
Usage
Parameters
Simple ViT
Distillation
Deep ViT
CaiT
Token-to-Token ViT
CCT
Cross ViT
PiT
LeViT
CvT
Twins SVT
CrossFormer
RegionViT
ScalableViT
SepViT
MaxViT
NesT
MobileViT
Masked Autoencoder
Simple Masked Image Modeling
Masked Patch Prediction
Masked Position Prediction
Adaptive Token Sampling
Patch Merger
Vision Transformer for Small Datasets
3D Vit
ViVit
Parallel ViT
Learnable Memory ViT
Dino
EsViT
Accessing Attention
Research Ideas
Efficient Attention
Combining with other Transformer improvements
FAQ
Resources
Citations
Vision Transformer - Pytorch
Implementation of Vision Transformer, a simple way to achieve SOTA in vision classification with only a single transformer encoder, in Pytorch. Significance is further explained in Yannic Kilcher's video. There's really not much to code here, but may as well lay it out for everyone so we expedite the attention revolution.

For a Pytorch implementation with pretrained models, please see Ross Wightman's repository here.

The official Jax repository is here.

A tensorflow2 translation also exists here, created by research scientist Junho Kim! 🙏

Flax translation by Enrico Shippole!


Parameters
image_size: int.
Image size. If you have rectangular images, make sure your image size is the maximum of the width and height
patch_size: int.
Number of patches. image_size must be divisible by patch_size.
The number of patches is:  n = (image_size // patch_size) ** 2 and n must be greater than 16.
num_classes: int.
Number of classes to classify.
dim: int.
Last dimension of output tensor after linear transformation nn.Linear(..., dim).
depth: int.
Number of Transformer blocks.
heads: int.
Number of heads in Multi-head Attention layer.
mlp_dim: int.
Dimension of the MLP (FeedForward) layer.
channels: int, default 3.
Number of image's channels.
dropout: float between [0, 1], default 0..
Dropout rate.
emb_dropout: float between [0, 1], default 0.
Embedding dropout rate.
pool: string, either cls token pooling or mean pooling

Distillation
https://github.com/lucidrains/vit-pytorch/raw/main/images/distill.png

