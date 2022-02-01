# Siamese network sprint

This repo contains notebooks and instructions to try out using a siamese network on our epigenetics dataset.

## Run in the cloud

The `siamese_contrastive.ipynb` notebook is originally from the [Keras](https://keras.io/examples/vision/siamese_contrastive/) project.
Their version can be [run in the cloud on Google Colab](https://colab.research.google.com/github/keras-team/keras-io/blob/master/examples/vision/ipynb/siamese_contrastive.ipynb).

Our own copy of the notebook and other notebooks we may create in this repo can also be [run in the cloud on Binder](https://mybinder.org/v2/gh/epigenetic-ml/siamese-sprint/HEAD).
Click on one of the notebook files in the left-hand panel to open it.

## Local setup

To run and modify the notebooks from your own machine, we need to:

1. clone the repo;
2. setup a Python environment with Jupyter and other dependencies;
3. start the Jupyter server and run your notebooks.

### Clone the repo

Assuming you connect to GitHub using an SSH key (see the [documentation to setup SSH key login](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) if you don't; the main advantage is that you won't have to type your username and password every time you want to commit something to the repo), you can clone with the SSH URL:

```console
git clone git@github.com:epigenetic-ml/siamese-sprint.git
```

Otherwise (if you don't login using an SSH key) use the HTTPS URL:

```console
git clone https://github.com/epigenetic-ml/siamese-sprint.git
```

### Setup Python environment

We will assume you have installed Miniconda ([download a Miniconda installer here](https://docs.conda.io/en/latest/miniconda.html)).
Create a basic Python environment for the project called `epi-siamese` with:

```console
conda create -n epi-siamese python -c conda-forge
```

This installs the latest Python version in the environment, which is 3.10.2 at the moment of writing.
Note that we use the `conda-forge` channel, which is optional, but has more packages.

Next, activate the environment in your current shell:

```console
conda activate epi-siamese
```

Finally, we install the dependencies needed for running locally using `pip`:

```console
pip install -r requirements.txt
```

### Start Jupyter and run your notebook(s)

In the dependencies file `requirements.txt` we listed the `notebook` package, which installs the Jupyter notebook server.
We can start the server now, from the repo folder:

```console
jupyter notebook
```

This will open up a tab in your browser pointing to the server's webinterface (typically at address `http://localhost:8888`).
You will see the notebook files in a list on the webinterface.
Just click the one you want to work on and it will open in its own tab.
Now you can run and change things interactively.
When you do so, the notebook will typically autosave every now and then.
Note that this changes the notebook file on disk.

As an alternative to the notebook server, there's also Jupyter Lab, which has a more extensive UI with multiple panels.
Binder (see the [Run in the cloud](#Run-in-the-cloud) section) also uses Jupyter Lab.
To install it, run `pip install jupyterlab` in your environment and run it with `jupyter lab`.