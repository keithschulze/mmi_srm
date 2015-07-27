# Post processing and Quality Control
We now have a list of localisations that were detected in each frame of the time-series. The problem is that many localisations represent single molecules that have been detected in multiple frames of the time-series:
* Each blink typically lasts several frames.
* Fluorophores cycle or blink a number of times.

The primary method for determining this currently is simply a spatial and temporal threshold. For example, if a blink occurs in the same region with 5 frames, it is considered to originate from the same fluorophore molecule. After 5 frames, a blink is considered to originate from a different molecule.

## Drift correction
No real substitute for having a stable system. Always try to minimise drift in the system rather than trying to correct for it later.

### Fiducial markers
Fluorescent markers that can be included during imaging.
Properties of a good fiducial marker:
* Must be visible across all time-points in the image series.
* Must not move.
* Must be small enough to be localised accurately.

### Cross-correlation
Fourier transform. Correlate phase images.

### Multiple emitter analysis


## Quality Control
Localisation Precision

Resolution

Fourier Ring Correlation
