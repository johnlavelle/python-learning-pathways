<!---
Note for converting to HTML

Create scrollable chat-like window in the presentation where there is too much text to fit in the slide by:

1. Using a div container with specific CSS properties:
   ```html
   <div style="background-color: #f9f9f9; border: 1px solid #ddd; 
               padding: 20px; height: 70vh; overflow-y: auto;">
   ```

2. The key properties that enable scrolling are:
   - `height: 70vh` - Makes it take up 70% of the screen height
   - `overflow-y: auto` - Creates a scrollbar when content exceeds this height

3. The styling (background color, border, padding) gives it a distinct chat window appearance within the slide.

This approach keeps all LLM content in a single slide while allowing the audience to scroll through it.
--->

## Pathways to Learn Python for Scientific Software Development

### A Guide for Researchers at DMI

* **Presenter:** [Your Name/Department]
* **Date:** May 8, 2025


Note: This talk outlines practical learning paths, resources, tools, and best practices for researchers at DMI looking to start or improve their skills in scientific software development using Python.

---

# Overview

## Getting Started
* What is Python? // Keep this brief
* Integrated Development Environments (IDEs) // Show an image of each with a brief description. I will talk about the merits of each 
  * Visual Studio Code
  * Spyder
  * PyCharm
  * Jupyter Lab
* How to get started writing Python code
  * The official Python tutorial
  * Learning Python, 6th Edition (Mark Lutz)

## Scientific Development

* Important libraries for scientific development // An image for each
  * Numpy
  * Pandas
  * Xarray
  * Cartopy
* Resources for scientific development 
  * Python for Data Analysis, 3rd Edition (Wes McKinney) // For learning Numpy, Pandas
  * Python library documentation // E.g. for Xarray, as there are few books on this
* Got yas in coming from another language
  * Pythonic Code with numpy // Give an example contrastinng using for loops to do a computation vs a vector operation with numpy

## Using LLMs (AL) to learn Python

* Prompts // An example prompt and outout for each
  * To give a tutorial on a specific topic
  * Translate code to Python
  * Debug my code
  * Improve code quality
  * Write code 
* LLM options // An image for each.
  * ChatGPT
  * Gemmini
  * Claude
  * Minstral
  * Local with Ollama

## Advanced Level
    
* Why code quality is important
* How and why to improve code quality
  * technical debt 
  * code smells
  * Coding standards: PEP-8

* Books to become a better scientific software developer:
  * Fluent Python: Clear, Concise, and Effective Programming (Luciano Ramalho) 
  * Clean Code: A Handbook of Agile Software Craftsmanship (Robert C. Martin)
  * Clean Code in Python: Develop maintainable and efficient code, 2nd Editiom (Mariano Anaya)
  * Pragmatic Programmer, The: Your journey to mastery
* Online resources:
  * Kaggle
* YouTube
  * https://www.youtube.com/@ArjanCodes/videos
* Possible future topics


---

Python is a *dynamic* language, meaning you can open it in the terminal and use it interactively.

![python terminal](../assets/images/open_python_in_terminal.png)

... as opposed to a *compiled* language like Fortran.

---

## Development Environments

You can develop using your favourite text editor, VIM, etc., but there are benefits in using an IDE:

* **Code Completion**: Suggests function names, parameters, and imports as you type
* **Integrated Debugging**: Set breakpoints, inspect variables, and step through code execution
* **Version Control Integration**: Git support built directly into your development environment
* **Virtual Environment Management**: Create and manage Python environments with ease
* **Scientific Tooling**: Built-in support for Jupyter notebooks, data visualization, and scientific libraries
* **Code Inspection**: Automated detection of style issues, errors, and potential bugs

---

## Visual Studio Code

![VS code](../assets/images/vscode.png)

Very popular, but requires some setup: [https://code.visualstudio.com/docs/languages/python](https://code.visualstudio.com/docs/languages/python)

---

## Spyder

![Spyder IDE](../assets/images/ide_spyder.png)

Matlab like interface, but more limited.

---

## PyCharm

![PyCharm IDE](../assets/images/ide_pycharm.png)

Sophisticated, Python orientated IDE. Requires a subscription.

---

## Jupyter Lab

![Jupyter Lab Interface](../assets/images/ide_jupyterlab.png)

For interactive code development. Not suitable for large code bases.

---

## Learn the basic syntax: tutorial

[The official Python tutorial](https://docs.python.org/3/tutorial/index.html)


---

https://www.pythoncheatsheet.org/

---

## Key Python Libraries for Scientific Software: Numpy

# NumPy: The Foundation of Scientific Computing in Python

## What is NumPy?
NumPy (Numerical Python) is a fundamental package for scientific computing in Python that provides:
- Fast, efficient multi-dimensional array objects
- **Performance:** 10-100x faster than Python lists

## Key Features
- N-dimensional arrays (ndarray)
- Broadcasting functions
- Linear algebra operations
- Fourier transforms
- 
## Simple Example
```python
import numpy as np

# Create array
arr = np.array([1, 2, 3, 4, 5])

# Perform operations
print(arr * 2)          # [2 4 6 8 10]
print(np.sum(arr))      # 15
print(np.mean(arr))     # 3.0
```

---

<!-- Note to LLM: Please embed this text in separate page the window -->

Prompt: I have a time series of 3D air pressure measurements. Please demonstrate how I can effeciently anlyse the data using xarray.

Response:

I'd be happy to demonstrate how to efficiently analyze 3D air pressure measurements using xarray, which is an excellent library for working with labeled multi-dimensional arrays, particularly for atmospheric data.

Let me create a comprehensive example showing how to work with your 3D air pressure data using xarray:

# Analyzing 3D Air Pressure Data with xarray

Xarray is an excellent tool for working with multi-dimensional labeled arrays, particularly atmospheric data like your 3D air pressure measurements. Here's how you can efficiently analyze such data:

## Key Benefits of Using xarray

1. **Labeled dimensions** - xarray uses named dimensions and coordinates, making data access intuitive
2. **NetCDF compatibility** - seamless reading/writing of NetCDF files (standard format for climate data)
3. **Built-in operations** - powerful aggregation, selection, and computation methods
4. **Integration with other tools** - works well with pandas, numpy, dask, and visualization libraries

## Typical Workflow

### 1. Data Loading and Inspection

```python
import xarray as xr
import numpy as np
import matplotlib.pyplot as plt

# Load data from a NetCDF file
ds = xr.open_dataset('pressure_data.nc')

# Examine dataset structure
print(ds)
print(ds.info())

# Check for missing values
print(ds.isnull().sum())
```

### 2. Selection and Subsetting

```python
# Select a specific time
time_slice = ds.sel(time='2023-01-10')

# Select a pressure level
level_500 = ds.sel(level=500)  # 500 hPa

# Select a geographic region
region = ds.sel(lat=slice(30, 60), lon=slice(280, 360))
```

### 3. Aggregation and Analysis

```python
# Temporal means
monthly_mean = ds.pressure.resample(time='M').mean()

# Spatial means
zonal_mean = ds.pressure.mean(dim='lon')  # Average along longitude
meridional_mean = ds.pressure.mean(dim='lat')  # Average along latitude

# Vertical profile
vertical_profile = ds.pressure.mean(dim=['lat', 'lon'])

# Calculate anomalies
climatology = ds.pressure.mean(dim='time')
anomalies = ds.pressure - climatology
```

### 4. Visualization

```python
# Plot a horizontal slice
level_500.pressure.isel(time=0).plot(
    figsize=(12, 8),
    cmap='viridis'
)

# Plot a vertical cross-section
ds.pressure.isel(time=0).sel(lat=0).plot(
    y='level',
    figsize=(12, 6)
)

# Create a time series for a point
ds.pressure.sel(lat=45, lon=280, level=500, method='nearest').plot()
```

### 5. Advanced Analysis

```python
# Calculating gradients
pressure_gradient_x = ds.pressure.differentiate(coord='lon')
pressure_gradient_y = ds.pressure.differentiate(coord='lat')

# Coarsen data (reduce resolution)
coarse_data = ds.coarsen(lat=2, lon=2).mean()

# Apply computation across multiple dimensions
result = xr.apply_ufunc(
    your_function,
    ds.pressure,
    input_core_dims=[['time', 'level', 'lat', 'lon']],
    output_core_dims=[['lat', 'lon']],
    vectorize=True
)
```

The artifact I've provided includes a comprehensive example that:
1. Creates a synthetic dataset (or shows how to load a real one)
2. Performs basic data exploration
3. Demonstrates various selection, aggregation, and analysis techniques
4. Creates multiple visualizations (horizontal slices, vertical cross-sections, time series)
5. Shows advanced analysis methods (EOF analysis, trend analysis, seasonal patterns)
6. Demonstrates data export options

Would you like me to explain any particular aspect of the code in more detail?

---

*NumPy is the foundation for data analysis and scientific computing in Python ecosystems like pandas, SciPy, matplotlib, and scikit-learn.*

## Key Python Libraries for Scientific Software:Domain-Specific Libraries

* **[Cartopy](https://scitools.org.uk/cartopy/docs/latest/getting_started/index.html)** - Geospatial data processing
* **[scikit-learn](https://scikit-learn.org/stable/index.html)** - Machine learning
* **[PyTorch](https://pytorch.org/)** - Deep learning

### Scientific Computing
* **Dask** - Parallel computing
* **xarray / zarr** 
* **Numba** - JIT compiler for accelerating code
* **JAX** - High-performance numerical computing

---

## Use a LLM: Convert from Matlab to Python

![llm_matlab_to_python.png](../assets/images/llm_matlab_to_python.png)
An example using Claude

---

## Clean Code Principles

1. Readable - clear and intuitive
2. Simple - does one thing well
3. Consistent - follows uniform patterns
4. DRY - avoids duplication
5. Self-explanatory - requires minimal comments
6. Modular - easily testable and maintainable
7. Well-structured - follows logical organization
8. Focused on clarity over cleverness

---

# Ask an LLM

## Is this *clean code*?

Give your code to a LLM (Large Language Model). 
It will evaluate the code and show you how to improve it.

---


## Best Practices in Scientific Software Development
### Quality & Reproducibility

* **Testing**:
  * pytest for unit and integration tests
  * Test early, test often
  * Continuous Integration (GitHub Actions, GitLab CI)

* **Environment Management**:
  * Virtual environments (venv, conda)
  * Requirements tracking (requirements.txt, environment.yml)
  * Container solutions (Docker)

* **Code Review**:
  * Peer review before merging
  * Automated quality checks

---

Advanced Python

---

![book_fluent_python.jpeg](../assets/images/book_fluent_python.jpeg)

---

 *"The Pragmatic Programmer"* by David Thomas & Andrew Hunt 

---

```mermaid
flowchart TD
    Start[Start Here] --> BasicSyntax
    
    subgraph Fundamentals
        BasicSyntax[Basic Python Syntax]
        BasicSyntax --> OfficialTutorial[Official Python Tutorial]
        BasicSyntax --> KaggleCourses[Kaggle Python Courses]
        BasicSyntax --> CheatSheets[Python Cheatsheets]
    end
    
    Fundamentals --> DevEnvironments
    
    subgraph DevEnvironments[Development Environments]
        VSCode[Visual Studio Code]
        PyCharm[PyCharm]
        Spyder[Spyder - Matlab-like]
        JupyterLab[Jupyter Lab - Interactive]
    end
    
    DevEnvironments --> ScientificLibraries
    
    subgraph ScientificLibraries[Scientific Libraries]
        CoreLibs[Core Libraries<br>NumPy, Pandas, Matplotlib]
        DomainSpecific[Domain Specific<br>Cartopy, scikit-learn, PyTorch]
        HPComputing[High Performance<br>Dask, xarray, Numba, JAX]
    end
    
    ScientificLibraries --> CleanCode
    
    subgraph CleanCode[Clean Code Practices]
        PEP8[PEP 8 Style Guide]
        Naming[Descriptive Naming]
        ComprehensionPatterns[List Comprehensions]
        TypeHints[Type Hints]
        ErrorHandling[Error Handling]
    end
    
    CleanCode --> LLMHelp
    
    subgraph LLMHelp[LLM Assistance]
        CodeConversion[Code Conversion<br>Matlab to Python]
        CodeReview[Code Review<br>Ask if code is clean]
        SolutionGeneration[Generate Example Solutions]
    end
    
    LLMHelp --> AdvancedPython[Advanced Python<br>Fluent Python Book]
```


---

## Learn the basic syntax: Kaggle


![kaggle1.png](../assets/images/kaggle1.png)

Kaggle offers course on Python...

---

## Learn the basic syntax: tutorial

![kaggle2.png](../assets/images/kaggle2.png)

Kaggle offers course on Python...

