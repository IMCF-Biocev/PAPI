## Exercise 6: Set up a Virtual Environment for Napari

You can access full Napari installation guide [here](https://napari.org/stable/tutorials/fundamentals/installation.html#napari-installation). 

Follow the instructions below to create a new virtual environment. Select a different environment name if you already have this one. 

You need to be in the terminal/prompt and make sure you are in the (base) environment. If your other evironment is active, deactivate it first.

The following steps show how to create a new environment containing Python and how to install *Napari* package inside. 

(We use conda, but mamba would also work.)

```bash
conda create -y -n napari-env -c conda-forge python=3.11
conda activate napari-env
python -m pip install "napari[all]"
```


Once finished, open Napari GUI by typing `napari` in the terminal.

```bash
napari
```

*Note:*
On some platforms, particularly macOS and Windows, there may be a ~30 second delay before the viewer appears on first launch. This is expected and subsequent launches should be quick. However, anti-malware and other security software measures may further delay launches—even after the first launch.
