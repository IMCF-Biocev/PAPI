## Exercise 0: Install & Setup 

### Instructions for creation of a new environment

1. **Open a terminal/prompt**:
   - On Windows: Miniforge3 Prompt
   - On macOS/Linux: Terminal
   - You should see (base) environment by default
    ```bash
    (base) C:\Users\Username>
    ```

2. **Create the new environment from scratch using mamba or conda**:
    ```bash
    conda create -n papi-advanced python=3.10
    ```

3. **!!! Activate created environment !!!**
    ```bash
    conda activate papi-advanced
    ```
    After activating papi-advanced, your prompt should change to:

    ```bash
    (papi-advanced) C:\Users\Username>
    ```

4. **Install necessary packages with pip**:
    ```bash
    pip install cellpose==3.1.1.1 napari[all] apoc stackview
    ```

5. **Install additional packages with mamba/conda**:
    ```bash
    conda install numpy=1.26.4 pandas=2.1.4 matplotlib seaborn scikit-image scikit-learn scipy ipywidgets jupyterlab trackpy
    ```
    Type `y` that you agree when prompted 