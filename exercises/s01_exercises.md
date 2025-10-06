# Python for Image Analysis – Introductory session



## Exercises

1. [Running Your First Python Script](#exercise1)
2. [Your First Jupyter Notebook](../materials/session_1/E02_first_notebook.ipynb)
3. [Python foundations 01](../materials/session_1/E03_python_foundations_1.ipynb)
4. [Python foundations 02](../materials/session_1/E04_python_foundations_2.ipynb)
5. [Working with Images](../materials/session_1/E05_image_analysis.ipynb)
6. [Set up a virtual environment for Napari](#exercise6)

---



Click on exercises below to show the instructions.

<a id="exercise0"></a>
<details>
<summary><h3>Exercise 0: Install & Setup Environment</h3></summary>

### Instructions

Before starting Exercise 1, make sure you have all necessary tools installed.

1. **Download and install Miniforge** (Python package manager):
   - [Miniforge installer](https://github.com/conda-forge/miniforge#miniforge3)
   - Follow platform-specific instructions.

2. **Download and install your preferred IDE (code editor) - recommended: VS Code** :
   - [VS Code download](https://code.visualstudio.com/Download)
   - Install with default options.

3. **Open a terminal**:
   - On Windows: miniforge3 Prompt or VS Code integrated terminal  
   - On macOS/Linux: Terminal or VS Code integrated terminal
   - You should see (base) environment by default
    ```bash
    (base) C:\Users\Username>
    ```

4. **Navigate to the PAPI setup folder**:
    ```bash
    cd path/to/PAPI/setup/intro
    ```

5. **Create the environment from the YAML file using mamba or conda**:
    ```bash
    mamba env create -f environment.yml
    ```

6. **Activate created environment**:
    ```bash
    conda activate papi_intro
    ```
    After activating papi_intro, your prompt should change to:

    ```bash
    (papi_intro) C:\Users\Username>
    ```
7. **Verify installation with**:
    ```bash
    conda list
    ```

</details>


<br><br>
---

<a id="exercise1"></a>
<details> 
<summary><h3>Exercise 1: Running Your First Python Script</h2></summary>


### Instructions

- Open a plain text editor (like Notepad) or create a new text file in your IDE (e.g., VS Code).  
- Type or copy-paste the **code** below into the new text file. 
    ```python
    # --- EXERCISE CODE ---

    # 1. Create a variable to hold a string of text
    message = "Hello from our first Python script!"

    # 2. Use the print() function to display the message in the terminal
    print(message)

    # 3. A simple calculation
    a = 10
    b = 20
    print("The sum of a and b is:", a + b)
    ```

- Save the file as `my_script.py`.  
    - *Note:* the Python interpreter can run any plain text file (`python my_script.txt` will work if it contains valid code).  
      However, `.py` is the standard extension and enables syntax highlighting, debugging, etc., in most editors.
- Open your terminal (Anaconda Prompt or integrated terminal in VS Code).  
   - In VS Code it is under: `Terminal > New Terminal`.
    - *in terminal*: Activate the environment **papi_intro**
    ```bash
    conda activate papi_intro
    ```
    - *in terminal*: Navigate to the folder with `my_script.py` file. 
        - For most systems, the command is: `cd path\to\folder`
    - *in terminal*: Run the script by typing the following and pressing Enter: 
    ```bash
    python my_script.py
    ```  
- You should see the output printed directly in your terminal.  
    Output you should see:
    ```
    Hello from our first Python script!
    The sum of a and b is: 30
    ```


</details>


<br><br>
---
<a id="exercise6"></a>
<details>
<summary><h3>Exercise 6: Set up a Virtual Environment for Napari</h2></summary>

## Set up a virtual environment for Napari

You can access full Napari installation guide [here](https://napari.org/stable/tutorials/fundamentals/installation.html#napari-installation). 

Follow the instructions below to crate new virtual environment. Select a different environment name if you already have this one. 

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

</details>