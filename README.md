# Acoustics Image

A repository for creating image for acoustics work.

How to use? 

* Use the image url in a JupyterHub via url `ghcr.io/nmfs-opensci/image-acoustics:latest`
* Use via docker run (note image is Unbuntu OS), `docker run ghcr.io/nmfs-opensci/image-acoustics:latest`

## For Contributors

Basic idea is that you edit `conda/environment.yaml` and the image will update automatically. Watch the Actions tab to make sure the image build aok. If you have other changes you need to make, add files to `binder` directory. This uses [repo2docker](https://repo2docker.readthedocs.io/en/latest/config_files.html) and a GitHub Action in `.github/workflows` to build the image and push to `ghcr.io` (the GitHub image repository).

* Edit Python modules in `conda/environment.yaml`. The GitHub Action in `.github` will create the conda-lock file.
* Edit other files in `binder` directory for the image. The `repo2docker` GitHub Action in `.github` will rebuild the image. Read about other files you can add to the `binder` directory and how they will be used [here](https://repo2docker.readthedocs.io/en/latest/config_files.html).  Make sure to update the push criteria in `.github/workflows/repo2docker.yaml` if you add files to the `binder` directory.

## Using this in JupyterHub

If the JupyterHub has the **Bring your own image** feature, then you can paste in `ghcr.io/nmfs-opensci/image-acoustics:latest` to the image and a server with your image will spin up.

<img width="772" alt="image" src="https://github.com/user-attachments/assets/13f1d200-b8a6-44e1-a9db-537260b21ec4">

