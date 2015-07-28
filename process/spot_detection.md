# Spot Detection
The first step in process STORM images sit to detect all spots/blink across all time-points. Spot detection is a segmentation problem. It is essentially a process of partitioning an image into foreground (i.e., objects of interest or spots) and the background. Once the image is segmented it is very easy to extract data from each of the individual segmented objects in the image.

Signal-to-noise ratio has a strong influence on segmentation. In a perfect world where there is little noise and lots of signal, simple segmentation methods like thresholding would be sufficient. However, while cameras have improved a lot, the sensitivity required to detect very few photons being emitted from each spots means results in some level of noise.

Below is a comparison of Otsu thresholding of two images with different SNR:



Note that there is not real substitute for having good images; however, there are some things we can do to work around non-optimal images. There are a number of image processing techniques that have been developed to enhance spots:
* __Simple noise filtering__
    * __Gaussian filter__
    * __Median filter__
    * Anisotropic diffusion
    * Non-local means
* __Difference of Gaussian (DoG)__
* Laplacian of Gaussian (LoG)
* Hessian of Gaussian (HoG)
* Wavelets

These image processing techniques are always somewhat of a compromise. Typically the more complex they are the better the filtering or enhancement will be, but at the cost of being computationally more expensive.

## Filtering
General image filters do not specifically enhance spots _per se_; rather they tend to reduce noise in the images, which can be strong contributor to poor segmentation results.

### Gaussian filter
Very commonly used filter in image processing. It's very simple and it's fast.
![](../assets/images/img_gfilt_plt.png)

### Median filter
Preserves the edges.
![](../assets/images/img_mfilt_plt.png)

Beyond simple filtering techniques, there are a number of image processing procedures that are specifically designed to enhance

## Difference of Gaussian
Test
![](../assets/images/img_dog_plt.png)


## Background signal
One last thing to note:

```
Noise != Background (Unspecific) Signal
```

__NONE__ of these techniques will help to remove 'background' fluorescence deriving from unspecific binding of antibodies. STORM is extremely sensitive and if your antibodies are non-specifically binding, there is nothing that can be done in terms of processing. This must be solved at the bench.
