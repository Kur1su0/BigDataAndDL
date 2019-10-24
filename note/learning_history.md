# Unsupervised Learning

## PCA



# NN

## CNN

How big is the output volume? The depth is equal to the number of filters -- every filter produces an activation map. The weight and height depend on a number of factors, which we can summarize in the following equations:

$$W_o = (W_i - F + 2 P) / S + 1$$
$$H_o = (H_i - F + 2 P) / S + 1$$

Where $(W_i, H_i)$ is the input size, $F$ is the width/height of the filter (which we assume is square), $P$ is the amount of __zero padding__, and $S$ is the __stride__. Zero padding refers to adding a border of zeros around the input image, and the stride refers to how far the kernel steps when it slides across the input. We almost always use $F = 2 P + 1$ and $S = 1$, which makes these equations simpler (just a little bit):

$$W_o = W_i$$
$$H_o = W_i$$

In other words, we leave the stride set to 1 (just like the convolution examples from before) and we fix the filter size and zero padding so that the output volume always has the same width and height as the input -- if we use 3x3 kernels then we'll add one layer of zeros, if we use 5x5 kernels then we'll add two layers of zeros, and so on. It's just simpler that way.