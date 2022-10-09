# HUMBI-Human-Rendering-Challenge

The task is to synthetize human body via HUMBI dataset. 
Baseline model is VUnet that was developed by Esser et al. and combines both a variational autoencoder and a U-Net to disentangle appearance and pose for image generation. Specifically, a conditional U-Net is used to generate images in the target pose and a variational autoencoder to generate the corresponding textures.
Limitations of the model: some appearance misalignment, low detail especially in facial features and hands as well as clothes with dense patterns, blue tint on generated images.
Given the limitation that the baseline model provides, I hope to improve the quality of the data sample outputted from the generator in the vunet model. In what follows, I propose the approach to combine the reconstruction error with the properties of images learned from the discriminator. The GAN component of the model is implemented so as to take advantage of its high-quality generative model with encoder that map input data to latent space.   
![Picture1](https://user-images.githubusercontent.com/47673347/194770300-d91f0804-a589-41fc-ad02-70bca9dc8d5a.png)
