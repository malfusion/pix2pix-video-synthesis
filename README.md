## Background

This project is inspired by the way humans learn to imagine the next few frames of video, when it comes to fluid motion. Just as we need to have seen a lot of occurences beforehand to imagine it with high accuracy, so does a neural network.

## Architecture
This is an implementation of the Pix2pix GAN architecture in PyTorch for Image-to-Image Translation, with a U-Net Generator and a PatchGAN Discriminator. We train the network on a specific set of video pertaining to the field that we want the network to learn (Eg: Clouds, water, waves, ink drops, etc) and task the network to predict the succeeding video frame, given a single frame as input. 

The skip connections in the U-Net Generator help the network learn a transformation on the original frame, while maintaining the details from the original image.

We train the network for 200 epochs of 2000 frames of video with a batch size of 1 to achieve the results.

**Todo:**

- Use a 70x70 PatchGAN as mentioned in the paper - "Image-to-Image Translation with Conditional Adversarial Networks" to optimise the output of the network.
- Varying the Lambda weight on the GAN loss/Pixel Loss tradeoff, to observe the difference in high and low frequence detail reproduction.

