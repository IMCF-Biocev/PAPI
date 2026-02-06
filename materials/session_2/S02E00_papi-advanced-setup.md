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
4. **Install necessary packages with mamba/conda**:
    ```bash
    conda install numpy=1.26.4 pandas=2.1.4 matplotlib seaborn scikit-image scikit-learn scipy ipywidgets jupyterlab trackpy ipykernel=6.30.1
    ```


5. **Install additional packages with pip**:
    ```bash
    pip install cellpose==3.1.1.1 napari[all] apoc stackview
    ```

    Type `y` that you agree when prompted 

<br>

--- 

6. **Verify installation**:
- Create new jupyter notebook
- Connect kernel to papi-advanced
- Inside first cell type & run
    ```python
    import napari   
    v = napari.Viewer()
    ```
    Check if Napari window pops up and is not frozen (you can access menus)

- Inside second cell type & run
    ```python
    from cellpose import models 
    m = models.Cellpose(model_type='nuclei')
    ```
    - **If the kernel is crashing**:
        1. Close jupyter notebook 
        2. Go back to prompt/terminal
        3. Execute following commands: 
            ```bash
            pip uninstall -y torch
            ```
            ```bash
            conda install pytorch
            ```
        - Verify cellpose functionality in jupyter notebook again

