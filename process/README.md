# STORM Processing and Reconstruction
The aim of this section is to improve your understanding of how STORM images are processed and reconstructed into super-resolution images. We will go into quite a low level of detail, but please don't feel overwhelmed. This is probably a level of detail you won't have to deal with; however, it is valuable to get a sense of what the various STORM processing software packages are doing, so that you can make informed decisions about the parameters you are setting and how they might affect the data you get out.

The examples covered in this section are not exhaustive and are not necessarily state-of-art in terms of the STORM processing. Nevertheless, many software packages still employ these techniques. A recent publication in _Nature Methods_ has done a very comprehensive evaluation and comparison of many freely available software packages for single-molecule localisation microscopy:

Sage, D., Kirshner, H., Pengo, T., Stuurman, N., Min, J., Manley, S., & Unser, M. (2015). Quantitative evaluation of software packages for single-molecule localization microscopy. _Nature Methods_. [http://doi.org/10.1038/nmeth.3442](http://doi.org/10.1038/nmeth.3442)

As you work through the different steps in this section, I encourage you all to take a look at the paper above and see if you can recognise some of the methods that are given as examples here, as well as going further to find out a little more about some of the advancements that have been made recent years. In particular, you will notice that many of the best performing packages in the tend to use more advanced methods (e.g., Maximum Likelihood Estimation, MLE) for sub-pixel localisation than are described here.


## Basic STORM Processing Outline
From the paper mentioned above you can see that there are a myriad of different STORM processing package, but all follow a fairly sequence of steps:
1. Spot enhancement and detection
2. Sub-pixel localisation
3. Post-processing and quality control
4. Reconstruction

We'll break these down with some examples in the next few chapters to see what sort of approaches are typically used at each of these steps. Hopefully this will give you a broad idea of what sort of things can affect the output of analysis.
