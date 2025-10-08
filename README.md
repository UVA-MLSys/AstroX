# AstroX

Project Description: 

Leveraging unsupervised and multimodal learning, we
aim to advance foundation models for a scalable and
better representation of large astronomy data for
insights. AstroX is a foundation model designed to
learn representations by aligning galaxy images and
spectra.This in-progress work focuses primarily on the
multimodal training phase, building upon and expanding
the capabilities of the state-of-the-art AstroCLIP model.
It paves the Way for Agentic AI and Autonomy in
Cosmology research for Astronomers.


Dataset:

Pre-training Dataset: Unlabeled dataset with metadata
The model uses galaxy images from the DESI Legacy Survey (DR9) and
spectra from DESI early data release (DR3).
The DESI LS contains 20TB of 76.4 million images in three optical bands (g,
r, and z). The spectra (flux over wavelength) includes 0.5TB of 1M+
samples. The image dataset is hosted on ORNL due to resource constraints.
Others are on Rivanna.
The cross-matched dataset between image and spectra to perform
multimodal alignment includes 160GB of 197.6k samples.
Downstream Tasks (Use Cases): with labels for benchmarking: (1) Redshift esti-
mation, (2) Galaxy property estimation, (3) Galaxy morphology classification, (4)
Searching similar galaxies, (5) Galaxy image segmentation.


Model:

Vision Transformer (DINOv2 from META, 315M parameter) uses
self-supervised Learning on the unlabeled image data.
Transformer-based spectrum encoder (55M parameter) for 1D
spectroscopic data. Learns self-supervised on the cross-matched spectra.
Contrastive learning on the cross-matched data aligns image and spectrum
in a shared embedding space.
Pretrained weights and supervised models (ResNet, CONV+Att) for result
comparison.
We improve the CLIP mechanism by adding Cyclic-CLIP for better
representation.
