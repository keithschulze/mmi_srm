# STORM Processing and Reconstruction
We are going to get into specifics about how STORM raw image sequences are processed and reconstructed into super-resolution images. Please don't feel overwhelmed, this is a level of detail you won't have to deal with; however, it is valuable to get a sense of what STORM processing software is doing so that you can make informed decisions about the parameters you are setting and how they might affect the data you get out.

## Overview
Basically all STORM processing software follows a similar sequence of steps:
1. Spot enhancement and detection
2. Sub-pixel localisation
3. Post-processing and quality control
4. Reconstruction

Let's break these down to see what sort of approaches are typically used at each of these steps. Hopefully this will give you a broad idea of what sort of things can affect the output of analysis.
