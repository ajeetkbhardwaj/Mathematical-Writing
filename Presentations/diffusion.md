---
marp: true
theme: uncover
class: invert
math: mathjx
size: 16:9
footer: Ajeet Kumar Bhardwaj | ajeetskbp9843@gmail.com | [Linkedin](https://www.linkedin.com/in/ajeetkumar09)

---
# <!--fit-->Diffusion Models


---
how to use pipelines in the [Diffusers library]() to generate images.
how to use its many features, and discuss options for accessing the GPU resources needed to use the library. How to how to use its many features, and discuss options for accessing the GPU resources needed to use the library.

---
What are Diffusion Models ?
> Diffusion Models is the one of generative models in a group of the generative algorithms. A good generative model will create a diverse set of outputs that resemble the training data without being exact copies. How do diffusion models achieve this ?

---

![bg fit](https://user-images.githubusercontent.com/10695622/174349667-04e9e485-793b-429a-affe-096e8199ad5b.png)

---
how to use them: guidance scale (for varying the amount the prompt is used), negative prompts (for removing concepts from an image), image initialisation (for starting with an existing image), textual inversion (for adding your own concepts to generated images), Dreambooth (an alternative approach to textual inversion).

CLIP embeddings
The VAE (variational autoencoder)
Predicting noise with the unet
Removing noise with schedulers

---
how Stable Diffusion works, using a novel interpretation that shows an easily-understood intuition for the theory. how Stable Diffusion works, using a novel interpretation that shows an easily-understood intuition for the theory. how the derivatives of such a model can provide the score needed to provide the basis of a diffusion process that generates handwritten digits. finite differencing, analytic derivatives, autoencoders, and U-Nets. Jeremy introduces the concept of creating a model that can take a sentence and return a vector of numbers representing the image, using two models: a text encoder and an image encoder. the similarities between diffusion-based models and deep learning optimizers, suggesting new research directions.