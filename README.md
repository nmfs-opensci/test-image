# Acoustics Image

A repository for creating image for acoustics work.

How to use? 

* Use the image url in a JupyterHub via url `ghcr.io/nmfs-opensci/image-acoustics:latest`
* Use via docker run (note image is Unbuntu OS), `docker run ghcr.io/nmfs-opensci/image-acoustics:latest`

## For Contributors

This uses [repo2docker](https://repo2docker.readthedocs.io/en/latest/config_files.html) and a GitHub Action in `.github/workflows` to build the image and push to `ghcr.io` (the GitHub image repository).

* Edit Python modules in `conda/environment.yaml`. The GitHub Action in `.github` will create the conda-lock file.
* Edit other files in `binder` directory for the image. The `repo2docker` GitHub Action in `.github` will rebuild the image. Read about other files you can add to the `binder` directory and how they will be used [here](https://repo2docker.readthedocs.io/en/latest/config_files.html).
