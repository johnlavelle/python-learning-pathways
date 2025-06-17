---
theme: default
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Pathways to Learn Python for Scientific Software Development
  A comprehensive learning guide for DMI researchers
drawings:
  persist: false
transition: slide-left
title: Python Learning Pathways
---

# Pathways to Learn Python for Scientific Software Development

A Guide for DMI Researchers

---
transition: fade-out
---

# Why This Learning Path?

<div class="grid grid-cols-2 gap-4">
<div>

## The Challenge

- Python ecosystem is vast
- Scientific computing needs
- Quality matters in research
- Time is precious

</div>
<div>

## Our Approach

- Curated pathways by level
- Focus on meteorology & oceanography
- Modern best practices

</div>
</div>

---

# Your Learning Journey

<div class="text-center mb-8">

```mermaid
graph LR
    A[Beginner] --> B[Scientific Python]
    B --> C[Domain Tools]
    C --> D[Best Practices]
    D --> E[Contributing]

```

</div>

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## Phase 1: Foundations
- Python syntax & concepts
- Basic data structures
- Simple scripts
*Typical: 1-2 months*

</div>
<div>

## Phase 2: Scientific Stack
- NumPy, Pandas, Xarray
- Plotting with Matplotlib
- Jupyter workflows
*Typical: 2-3 months*

</div>
<div>

## Phase 3: Advanced
- Clean code principles
- Testing & debugging
- Collaboration tools
*Typical: 2-3 months*

</div>
</div>

**Note:** These timelines are flexible! Learn at your own pace - some go faster, some need more time. The journey matters more than the speed.

---
layout: section
---

# Part 1: Getting Started
## Choosing Your First Steps

---

# Learning Paths by Background

<div class="grid grid-cols-2 gap-6">
<div>

## Complete Beginner

**Start Here:**
1. **[Python Crash Course (3rd Edition)](https://nostarch.com/python-crash-course-3rd-edition)** - Comprehensive book with projects
2. **[Software Carpentry](https://swcarpentry.github.io/python-novice-inflammation/)** - Research-focused workshops
3. **[Python.org Tutorial](https://docs.python.org/3/tutorial/)** - Official guide

**Time:** 4-6 weeks (1-2 hrs/day)

**Community:** Join [Pytroll Slack](https://pytroll.github.io/#getting-in-touch) on Day 1!

</div>
<div>

## Coming from MATLAB/R/Fortran

**Start Here:**
1. **[NumPy for MATLAB users](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html)** - Direct translation guide
2. **[Project Pythia](https://projectpythia.org/)** - Earth sciences focus
3. **[Python for Data Analysis (3rd Ed)](https://wesmckinney.com/book/)** - By pandas creator

**Time:** 2-3 weeks (1-2 hrs/day)

**First Project:** Port existing analysis

**Next Book:** [Fluent Python](https://www.oreilly.com/library/view/fluent-python-2nd/9781492056348/) for Python mastery

</div>
</div>

---

# Modern Learning Resources Comparison

| Resource | Best For | Format | Time | Cost | DMI Relevance |
|----------|----------|---------|------|------|---------------|
| **[Software Carpentry](https://swcarpentry.github.io/python-novice-inflammation/)** | Research beginners | Workshop-style | 2 days | Free | ⭐⭐⭐⭐⭐ |
| **[Project Pythia](https://projectpythia.org/)** | Atmospheric scientists | Tutorials + Videos | Self-paced | Free | ⭐⭐⭐⭐⭐ |
| **[Real Python](https://realpython.com/)** | All levels | Articles + Courses | Ongoing | Free/Paid | ⭐⭐⭐⭐ |
| **[Codecademy Python](https://www.codecademy.com/learn/learn-python-3)** | Absolute beginners | Interactive | 25 hours | Free/Pro | ⭐⭐⭐ |
| **[Python for Everybody](https://www.coursera.org/specializations/python)** | General programming | Video lectures | 8 months | Free/Paid | ⭐⭐⭐ |

**Recommendation:** Start with Software Carpentry + Project Pythia for the perfect research focus

---
layout: section
---

# Part 2: Scientific & Domain Tools
## Building Your Technical Stack

---

# Essential Scientific Stack

<div class="grid grid-cols-3 gap-4">
<div>

## Data Handling
```python
import numpy as np
import pandas as pd
import xarray as xr
```
- **NumPy**: Efficient array computing and mathematical operations
- **Pandas**: Tabular data analysis with DataFrames
- **Xarray**: Labeled multi-dimensional arrays for NetCDF/climate data

[NumPy](https://numpy.org/doc/stable/user/absolute_beginners.html) → [Pandas](https://pandas.pydata.org/docs/user_guide/10min.html) → [Xarray](https://docs.xarray.dev/en/stable/getting-started-guide/quick-overview.html)

</div>
<div>

## Visualization
```python
import matplotlib.pyplot as plt
import cartopy.crs as ccrs
import holoviews as hv
```
- **Matplotlib**: Foundation plotting library for static graphs
- **Cartopy**: Map projections and geospatial plotting
- **HoloViews**: High-level data visualization with interactivity

[Matplotlib](https://matplotlib.org/stable/tutorials/index.html) • [Cartopy](https://scitools.org.uk/cartopy/docs/latest/gallery/index.html) • [HoloViews](https://holoviews.org/getting_started/Introduction.html)

</div>
<div>

## Domain Tools
```python
# Atmosphere
import metpy
import satpy
# Ocean  
import xarray
import gsw  # oceanography
```
- **MetPy**: Meteorological calculations and weather analysis
- **Satpy**: Reading and processing satellite data
- **GSW**: Oceanographic thermodynamics (TEOS-10)
- **xgcm**: Grid-aware operations for ocean/atmosphere models

[MetPy](https://unidata.github.io/MetPy/latest/tutorials/index.html) • [GSW](https://teos-10.github.io/GSW-Python/) • [xgcm](https://xgcm.readthedocs.io/)

</div>
</div>

<div class="mt-8 text-center">

**Learning Order:** [NumPy basics](https://numpy.org/learn/) (1 week) → [Pandas intro](https://pandas.pydata.org/docs/getting_started/intro_tutorials/) (1 week) → [Xarray tutorial](https://tutorial.xarray.dev/intro.html) (2 weeks) → Domain tools

</div>

---

# Weather & Climate Data Access

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## 🌤️ Atmosphere/Land

**[ECMWF Open Data](https://github.com/ecmwf/ecmwf-opendata)**
```python
from ecmwf.opendata import Client
client = Client()
# Real-time forecasts
```
Access real-time ECMWF weather forecasts from high-resolution and ensemble models

**[ERA5 Reanalysis](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels)**
```python
import cdsapi
c = cdsapi.Client()
# Historical weather
```
Comprehensive atmospheric reanalysis from 1940-present with hourly data

[CDS setup](https://cds.climate.copernicus.eu/how-to-api)

</div>
<div>

## 🌊 Ocean/Marine

**[Copernicus Marine](https://marine.copernicus.eu/)**
```python
import copernicusmarine as cm
cm.open_dataset(
    dataset_id="cmems_mod_glo_phy_anfc_0.083deg_P1D-m"
)
```
Provides ocean observations, analyses, forecasts, and reanalyses for European seas and global ocean

[Python Toolbox](https://pypi.org/project/copernicus-marine-client/) • [Documentation](https://help.marine.copernicus.eu/en/articles/7970514-copernicus-marine-toolbox-introduction)

**[C3S Climate Data](https://climate.copernicus.eu/)**
- Sea ice, SST, ocean indicators
- Climate projections
- [CDS API](https://cds.climate.copernicus.eu/api-how-to)

Climate Data Store with reanalyses, seasonal forecasts, and climate projections

</div>
<div>

## 🛰️ Satellite

**[Satpy](https://satpy.readthedocs.io/)** (Multi-sensor)
```python
from satpy import Scene
scn = Scene(filenames=files)
scn.load(['natural_color'])
```
Python library for reading and processing earth-observing satellite data

**[EUMDAC](https://pypi.org/project/eumdac/)**
```python
import eumdac
# EUMETSAT archive
```
Access EUMETSAT's entire satellite data archive programmatically

[Setup guide](https://user.eumetsat.int/resources/user-guides/eumetsat-data-access-client-eumdac-guide)

</div>
</div>

**Setup:** `conda install -c conda-forge satpy xarray cfgrib` • `uv pip install copernicusmarine`

**Learn More:** [Pythia Cookbooks](https://cookbooks.projectpythia.org/) • [Pangeo Gallery](https://gallery.pangeo.io/) • [CMEMS Use Cases](https://marine.copernicus.eu/services/use-cases)

---
layout: section
---

# Part 3: Development Environment
## Setting Up for Success

---

# Your Development Setup

<div class="grid grid-cols-2 gap-6">
<div>

## IDE Choice

**[VS Code](https://code.visualstudio.com/)** (Recommended)
- Free, lightweight
- [Great Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- Integrated terminal
- [Remote development](https://code.visualstudio.com/docs/remote/remote-overview)

**Alternatives:**
- [PyCharm](https://www.jetbrains.com/pycharm/) (full-featured)
- [JupyterLab](https://jupyter.org/) (notebooks)
- [Spyder](https://www.spyder-ide.org/) (MATLAB-like)

</div>
<div>

## Environment Management

**Using [Miniconda](https://docs.conda.io/en/latest/miniconda.html)** - the standard for scientific Python
- Free and open source
- No licensing restrictions
- Preferred by research institutions
- Same features as Anaconda
- Installs pre-compiled binaries (not just Python packages)

```bash
# Create environment
conda create -n dmi-work python=3.11
conda activate dmi-work

# Install scientific stack from conda-forge
# https://conda-forge.org/
conda install -c conda-forge \
  numpy pandas xarray \
  matplotlib cartopy \
  jupyter satpy

# Install from PyPI
pip install ecmwf-opendata
```

</div>
</div>

---

# Modern Package Management with uv

<div class="grid grid-cols-2 gap-6">
<div>

## What is uv?

[`uv`](https://github.com/astral-sh/uv) is an extremely fast Python package installer and resolver written in Rust

**Benefits:**
- 10-100x faster than pip
- Better dependency resolution
- Drop-in pip replacement
- Works perfectly with Miniconda

**Install uv:**
```bash
# Using pip
pip install uv

# Using conda (recommended)
conda install -c conda-forge uv

# Standalone installer
curl -LsSf https://astral.sh/uv/install.sh | sh
```

</div>
</div>

---

# 📦 Best Practice Workflow

<div class="grid grid-cols-1 gap-6">
<div>

```bash
# 1. Use Miniconda for base environment
conda create -n project python=3.11
conda activate project

# 2. Install complex packages with conda
conda install -c conda-forge \
  cartopy gdal netcdf4

# 3. Use uv for pure Python packages
uv pip install pandas xarray

# 4. Create requirements.txt
uv pip freeze > requirements.txt

# 5. Reproduce environment elsewhere
conda env export > environment.yml
```

**Why this approach?** Miniconda handles complex dependencies, uv provides speed

</div>
</div>

---

# Effective Development Workflow

<div class="grid grid-cols-2 gap-6">
<div>

## Version Control

```bash
# Start every project with
git init
git add .
git commit -m "Initial commit"

# Create feature branch
git checkout -b feature/add-analysis

# Share your work
git push origin main
```

**Learn:** Basic Git in first month
- [Pro Git Book](https://git-scm.com/book) (free)
- [GitHub Skills](https://skills.github.com/)
- [Visual Git Guide](https://marklodato.github.io/visual-git-guide/index-en.html)

</div>
<div>

## Jupyter Best Practices

1. **Notebooks for exploration** ([Jupyter docs](https://jupyter.org/documentation))
2. **Scripts for production**
3. **Clear cell outputs before commit**
4. **Use meaningful names**

```python
# Good notebook structure
# 1. Imports
# 2. Configuration  
# 3. Data loading
# 4. Analysis
# 5. Visualization
```

</div>
</div>

---
layout: section
---

# Part 4: Writing Better Code
## From Scripts to Software

---

# Code Quality Progression

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## Starting Out
```python
# Works but not ideal
data = []
for i in range(len(temps)):
    if temps[i] > 0:
        data.append(temps[i])
```

Focus on: **Making it work**

</div>
<div>

## Getting Better
```python
# Pythonic approach
data = [t for t in temps 
        if t > 0]

# Or using NumPy
data = temps[temps > 0]
```

Focus on: **Readability**

</div>
<div>

## Advanced
```python
def filter_positive_temps(
    temps: np.ndarray
) -> np.ndarray:
    """Filter positive temperatures.
    
    Args:
        temps: Temperature array
        
    Returns:
        Positive temperatures only
    """
    return temps[temps > 0]
```

Focus on: **Maintainability**

</div>
</div>

**Learn from:** [ArjanCodes](https://www.youtube.com/@ArjanCodes) • [mCoding](https://www.youtube.com/@mCoding) • [Real Python](https://www.youtube.com/@realpython)

**Professional Development Books:**
- **[Fluent Python](https://www.oreilly.com/library/view/fluent-python-2nd/9781492056348/)** - Deep Python idioms
- **[The Pragmatic Programmer](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/)** - Software craftsmanship

---

# Testing Your Code

<div class="grid grid-cols-2 gap-6">
<div>

## Start Simple

```python
# test_temperature.py
def test_celsius_to_kelvin():
    assert celsius_to_kelvin(0) == 273.15
    assert celsius_to_kelvin(-273.15) == 0
    
def test_invalid_temperature():
    with pytest.raises(ValueError):
        celsius_to_kelvin(-300)
```

**Run:** `pytest test_temperature.py`

</div>
<div>

## Testing Benefits

1. **Confidence** in changes
2. **Documentation** via examples
3. **Better design** thinking
4. **Faster debugging**

**Start when:** You use code twice

**Tools:** [pytest](https://pytest.org/), [hypothesis](https://hypothesis.readthedocs.io/)

</div>
</div>

---
layout: section
---

# Part 5: AI-Assisted Development
## Modern Tools for Faster Learning

---

# LLMs (AI Chatbots) 

<div class="grid grid-cols-2 gap-6">
<div>

## Good Use Cases

✅ **Boilerplate code**
- "Create click CLI for data processing"

✅ **Algorithm implementation**
- "Implement Kalman filter in NumPy"

✅ **Code translation**
- "Convert this MATLAB code to Python"

✅ **Code Improvement**
- "How can I improve this code"

✅ **Understand Existing Code**
- Explain this step by step

✅ **Documentation**
- "Add docstrings to this class"
- "Create a README.md file for this code"


**Tip:** 

</div>
<div>

---

## LLM Comparison

**[GitHub Copilot](https://github.com/features/copilot)** 🇺🇸 - *Best for: Code completion*  
Seamless IDE integration across VS Code, PyCharm, and Vim. Real-time suggestions as you type, understands project context and coding patterns.

**[ChatGPT](https://chat.openai.com/)** 🇺🇸 - *Best for: General coding*  
Excellent at explaining complex concepts, debugging code, and providing step-by-step tutorials. Strong natural language understanding for varied prompts.

**[Claude](https://claude.ai/)** 🇺🇸 - *Best for: Code analysis*  
Handles large codebases (200K+ tokens), excellent at refactoring and architectural analysis. Superior reasoning through complex multi-step problems.

**[JetBrains AI](https://www.jetbrains.com/ai/)** 🇨🇿 - *Best for: PyCharm users*  
Native PyCharm integration with intelligent refactoring suggestions. Context-aware code generation that understands your project structure and dependencies.

**[Le Chat](https://chat.mistral.ai/)** 🇫🇷 - *Best for: Fast responses*  
Ultra-fast 1000+ words/sec generation with transparent reasoning mode. Web search integration with citations, strong at scientific computing tasks.

**[Gemini](https://gemini.google.com/)** 🇺🇸 - *Best for: Multimodal tasks*  
Excellent at processing images, documents, and code together. Strong reasoning capabilities with Google Search integration for up-to-date information.

</div>
</div>

**Remember:** AI is a powerful learning accelerator, but real mastery comes from understanding fundamentals.

---
layout: section
---

# Part 6: Community & Continuous Learning  
## Building Your Support Network

---

# Essential Communities & Resources

<div class="grid grid-cols-2 gap-6">
<div>

## Join These Communities

**[Pytroll Slack](https://pytroll.github.io/#getting-in-touch)** - Satellite data processing
- Active daily help
- Real-world examples
- Direct access to tool authors

**[Pangeo Discourse](https://discourse.pangeo.io/)** - Big data geoscience
- Xarray, Dask expertise
- Cloud computing discussions

**[Project Pythia](https://projectpythia.org/resource-gallery.html)** - Educational resources
- Cookbooks with examples
- Training materials

**[ECMWF eLearning](https://www.ecmwf.int/en/learning)** - Professional training
- Free courses on NWP and data

</div>
<div>

## Quick Reference Bookmarks

**Core Documentation:**
- [Python.org](https://docs.python.org/3/) - Language reference
- [NumPy User Guide](https://numpy.org/doc/stable/user/) - Array computing
- [Xarray Docs](https://docs.xarray.dev/) - Multidimensional data
- [Matplotlib Tutorials](https://matplotlib.org/stable/tutorials/) - Plotting

**Domain Tools:**
- [Satpy Gallery](https://satpy.readthedocs.io/en/stable/auto_examples/index.html) - Satellite examples
- [Cartopy Examples](https://scitools.org.uk/cartopy/docs/latest/gallery/index.html) - Map plotting
- [MetPy Tutorials](https://unidata.github.io/MetPy/latest/tutorials/index.html) - Meteorology
- [Copernicus Marine Help](https://help.marine.copernicus.eu/) - Ocean data

**Bookmark Strategy:** Save one link per tool as you learn it

</div>
</div>

---

# Data Analysis Examples
- **[Pythia Cookbooks](https://cookbooks.projectpythia.org/)** - Step-by-step tutorials
- **[Pangeo Gallery](https://gallery.pangeo.io/)** - Real-world workflows
- **[Pytroll Examples](https://github.com/pytroll/pytroll-examples)** - Satellite processing
- **[CMEMS Use Cases](https://marine.copernicus.eu/services/use-cases)** - Ocean data applications

</div>
</div>

---
layout: center
class: text-center
---

# Start Your Journey Today!

## Next Steps

1. **Pick your track** (NWP, Ocean, or Satellite)
2. **[Install Miniconda](https://docs.conda.io/en/latest/miniconda.html)** for Python environment management
3. **[Install uv](https://github.com/astral-sh/uv)** for fast package management
4. **[Join Pytroll Slack](https://pytroll.github.io/#getting-in-touch)** for support
5. **Start with ONE resource**
6. **Code daily**, even 15 minutes

<br>

---

# Multiple Ways to Learn

<div class="grid grid-cols-3 gap-4 text-center">
<div>

## Read
These slides and detailed documentation

</div>
<div>

## Listen
25-minute AI podcast discussion covering all resources

<audio controls class="mt-2">
  <source src="../assets/Python_Pathways_Podcast.wav" type="audio/wav">
</audio>

</div>
<div>

## Watch
Video tutorials and conference talks linked throughout

</div>
</div>

---

### Remember: Everyone started as a beginner!

<div class="mt-8">

Questions? Find me on [Slack](https://pytroll.slack.com) or [GitHub](https://github.com)

</div>