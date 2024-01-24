# The Hidden Language of Diffusion Models [ICLR'24]

<p align="center">
<img src="docs/part1.gif" width="800px"/> 

<a href="https://hila-chefer.github.io/Conceptor/"><img src="https://img.shields.io/static/v1?label=Project&message=Website&color=red" height=20.5></a> 
 <a href="https://arxiv.org/abs/2306.00966"><img src="https://img.shields.io/badge/arXiv-2306.00966-b31b1b.svg" height=20.5></a>

> Text-to-image diffusion models have demonstrated an unparalleled ability to generate high-quality, diverse images from a textual prompt. However, the internal representations learned by these models remain an enigma. In this work, we present Conceptor, a novel method to interpret the internal representation of a textual concept by a diffusion model. This interpretation is obtained by decomposing the concept into a small set of human-interpretable textual elements. Applied over the state-of-the-art Stable Diffusion model, Conceptor reveals non-trivial structures in the representations of concepts. For example, we find surprising visual connections between concepts, that transcend their textual semantics. We additionally discover concepts that rely on mixtures of exemplars, biases, renowned artistic styles, or a simultaneous fusion of multiple meanings of the concept. Through a large battery of experiments, we demonstrate Conceptor's ability to provide meaningful, robust, and faithful decompositions for a wide variety of abstract, concrete, and complex textual concepts, while allowing to naturally connect each decomposition element to its corresponding visual impact on the generated images. 

### NEW! code is published under the [google research repo](https://github.com/google-research/google-research/tree/a2a0ec853e8fae38532c727799863e9d639aa0f2/conceptor)

## Description  
Official implementation of the paper The Hidden Language of Diffusion Models. The paper proposes a method dubbed <i>Conceptor</i> to produce explanations for text-to-image diffusion models.
 <br>

## Concept Explanation with Conceptor
<p align="center">
<img src="docs/part2.jpg" width="800px"/>  
<br>
Given a concept of interest (e.g., a president) and a text-to-image model, we generate a set of images to visually represent the concept. Conceptor then learns to decompose the concept into a small set of interpretable tokens, with the objective of reconstructing the generated images. The decomposition reveals interesting behaviors such as reliance on exemplars (e.g., "Obama", "Biden").
</p>

## Single-image Decomposition with Conceptor
<p align="center">
<img src="docs/part3.jpg" width="800px"/>  
<br>
 Given a single image from the concept, our method extracts the tokens in the decomposition that caused the generation of the image. For example, a snail is decomposed into a combination of ladybug and winding due to the structure of its body, and the texture of its shell.
</p>

## Concept Manipulation with Conceptor
<p align="center">
<img src="docs/manipulation.jpg" width="600px"/>  
<br>
 Our method enables fine-grained concept manipulation by modifying the coefficient corresponding to a token of interest. For example, by manipulating the coefficient corresponding to the token abstract in the decomposition of the concept sculpture, we can make an input sculpture more or less abstract.
</p>

## Citing our paper
If you make use of our work, please cite our paper:
```
@article{chefer2023hidden,
        title={The Hidden Language of Diffusion Models},
        author={Chefer, Hila and Lang, Oran and Geva, Mor and Polosukhin, Volodymyr and Shocher, Assaf and Irani, Michal and Mosseri, Inbar and Wolf, Lior},
        journal={arXiv preprint arXiv:2306.00966},
        year={2023}
}
```
