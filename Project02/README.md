# Project 02 - Dataset

This project uses `data/train/train_images.npy`, `data/train/train_labels.npy`, `data/test/test_images.npy`, `data/test/test_labels.npy`, `data/test/clean_images.npy` and `data/test/clean_labels.npy`, derived from **MNIST-C** (a corrupted version of MNIST). The training split contains only corrupted digits; the test split provides both corrupted and clean (uncorrupted) images for evaluating distribution shift, as prepared by the course staff for this assignment.

**Official download (static archive):** https://zenodo.org/records/3239543 (`mnist_c.zip`)

**Corruption code:** https://github.com/google-research/mnist-c

## License

- The MNIST-C dataset (Zenodo record) is distributed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**: reuse and redistribution are allowed for any purpose, provided appropriate credit is given.
- The corruption-generation code in the `google-research/mnist-c` repository is licensed under **Apache License 2.0**.

## Attribution / citation

> Mu, N., & Gilmer, J. (2019). MNIST-C: A Robustness Benchmark for Computer Vision. *arXiv preprint arXiv:1906.02337*.
>
> LeCun, Y., Cortes, C. THE MNIST DATABASE of handwritten digits. (original dataset, CC BY-SA 3.0)
