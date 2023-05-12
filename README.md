# Image-Transformation-Techniques

## Basic GAN Implementations for Image Synthesis:
Generative Adversarial Networks, known as GANs, are a sophisticated subset of deep learning algorithms specializing in generating data. Operating with a pair of contesting neural networks, these models have a broad range of applications such as artistic styling, image merging, and direct image translations. Our objective in this project is to employ GANs for synthesizing believable pizza images from two datasets - one with genuine pizza images and another with computer-generated pizza imitations.

Insights Gained:
In the initial stage of this project, we focused on creating artificial images through the power of GANs. Separate GANs were trained for authentic and computer-generated pizzas, resulting in the former producing images that were convincingly realistic. Optimizations such as reducing the batch size and increasing the training duration were identified as potential means to enhance the performance. The project demonstrated promising results with 85 epochs of training, suggesting that extending to 100-150 epochs with additional data augmentation techniques such as blurring, image rotation, and jitter introduction could yield even better outcomes. Future work could also explore refining the model architecture for enhanced results.

## Supervised Image Conversion Using Pix2Pix:
Image-to-image conversion is pivotal in applications like transforming grayscale images to color, artistic style transition, and altering seasonal representations in images. This process uses a supervised method where each source image is paired with a corresponding target image, creating a direct mapping that the model learns. We utilize the Pix2Pix framework, an advanced Conditional GAN model, allowing us to dictate the output class of the generated image. In our study, we applied this architecture to the Dayton dataset consisting of diverse street and aerial views. The model's efficacy was measured using established metrics such as the Frechet Inception Distance (FID) and the Inception Score (IS).

Concluding Observations:
During this phase, we explored the complex task of paired image translation, which necessitates specialized models for each unique translation challenge. By implementing the Pix2Pix GAN, we tailored the loss function to combine L1 Distance and Adversarial Loss, alongside innovations in the Generator and Discriminator designs. This enabled the generation of images that were not only authentic to the content of the target domain but also accurately translated from the source imagery. Our replication of the Pix2Pix model yielded metrics-aligned results, with qualitative assessments matching the quantitative FID and IS scores. Observations indicated a decrease in FID and an increase in IS with more training epochs. Prospective studies could look into training unpaired networks with smaller batch sizes and investigating learning schedules to optimize runtime.

## Unsupervised Conversion with CycleGAN:
In the realm of unsupervised learning, CycleGAN stands out for its impressive ability to translate images between domains using cycle consistency. This concept ensures that an image translated from its source domain to the target domain and then back again should result in the original image. Our work implemented CycleGAN to facilitate translations between Live Pizza images and those from Synthetic or Pre-Recorded domains.

## Advancements in CycleGAN Methodology:
Despite its effectiveness, the CycleGAN framework sometimes produces artifacts due to its pixel-level constraints. To address this, we proposed a new loss function that combines VGG Perceptual loss (feature-level loss) with pixel-level consistency loss. This enhanced CycleGAN architecture was subjected to both qualitative and quantitative evaluations, using the same metrics of FID and IS to assess the quality of the image translations produced.
