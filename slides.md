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

A Comprehensive Learning Guide for DMI Researchers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

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

## Our Solution

- Curated learning pathways
- Practical resources
- Scientific applications
- Modern practices

</div>
</div>

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Learning Roadmap

<div class="text-sm">

### 🚀 Weeks 1-4: Fundamentals
- Basic syntax and data types
- Control structures and functions

### 🔬 Weeks 5-12: Scientific Stack
- NumPy, Pandas, Matplotlib
- Domain-specific libraries

### 🏗️ Weeks 13-20: Best Practices
- Clean code and testing
- Version control

### 🎯 Ongoing: Advanced Topics
- Performance optimization
- Machine learning

</div>

---

# Starting Your Journey

## 🎓 Complete Beginner Resources

<div class="grid grid-cols-2 gap-4 text-sm">
<div>

**Interactive Learning:**
- [Codecademy Python](https://www.codecademy.com/learn/learn-python-3)
- [Python.org Tutorial](https://docs.python.org/3/tutorial/)
- [Google's Python Class](https://developers.google.com/edu/python)

</div>
<div>

**Essential Books:**
- ["Python Crash Course"](https://nostarch.com/pythoncrashcourse2e)
- ["Automate the Boring Stuff"](https://automatetheboringstuff.com/)

**Time:** 20-30 hours for basics

</div>
</div>

---

# Online Learning Platforms

<div class="grid grid-cols-2 gap-6">
<div>

## University Courses

- [MIT 6.00.1x](https://www.edx.org/course/introduction-to-computer-science-and-programming-7) (EdX)
- [Python for Everybody](https://www.coursera.org/specializations/python) (Coursera)

</div>
<div>

## Scientific Python

- [Software Carpentry](https://swcarpentry.github.io/python-novice-inflammation/)
- [Kaggle Learn](https://www.kaggle.com/learn/python)
- [SciPy Lectures](https://scipy-lectures.org/)

</div>
</div>

---

# YouTube Learning Channels

<div class="grid grid-cols-2 gap-4">
<div>

## 🎥 Best Practices
- [ArjanCodes](https://www.youtube.com/@ArjanCodes)
  - Clean code & SOLID
  - Design patterns
- [Corey Schafer](https://www.youtube.com/c/Coreyms)
  - Comprehensive tutorials

</div>
<div>

## 🔬 Scientific Python
- [sentdex](https://www.youtube.com/c/sentdex)
  - Data science projects
- [PyData](https://www.youtube.com/user/PyDataTV)
  - Conference talks

</div>
</div>

---
layout: two-cols
---

# Essential Books

::default::

## Core Python
- 🟢 ["Python Crash Course"](https://nostarch.com/pythoncrashcourse2e)
- 🟡 ["Effective Python"](https://effectivepython.com/)
- 🔴 ["Fluent Python"](https://www.oreilly.com/library/view/fluent-python-2nd/9781492056348/)

📺 Watch: [ArjanCodes: Python Books Review](https://www.youtube.com/watch?v=O7pqp_q6br4)

::right::

## Scientific & Engineering
- ["Python for Data Analysis"](https://wesmckinney.com/book/)
- ["Clean Code"](https://www.oreilly.com/library/view/clean-code-a/9780136083238/)
- ["The Pragmatic Programmer"](https://pragprog.com/titles/tpp20/)

---

# Scientific Python Ecosystem

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## 🔧 Foundation
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [SciPy](https://scipy.org/)

</div>
<div>

## 🌍 Geo/Meteo
- [Xarray](https://xarray.pydata.org/)
- [MetPy](https://unidata.github.io/MetPy/)
- [Cartopy](https://scitools.org.uk/cartopy/)
- [Iris](https://scitools-iris.readthedocs.io/)

</div>
<div>

## ⚡ Performance
- [Numba](https://numba.pydata.org/)
- [Dask](https://dask.org/)
- [CuPy](https://cupy.dev/)

</div>
</div>

---

# Development Environments

<div class="grid grid-cols-2 gap-6">
<div>

## 💻 IDEs

**[VS Code](https://code.visualstudio.com/)**
- Free, extensible
- Great Python support

**[PyCharm](https://www.jetbrains.com/pycharm/)**
- Professional features
- Scientific mode

**[JupyterLab](https://jupyter.org/)**
- Interactive notebooks
- Great for exploration

</div>
<div>

## 📦 Package Management

**[uv](https://github.com/astral-sh/uv)**
- Ultra-fast installer
- Modern alternative to pip

**[Miniconda](https://docs.conda.io/en/latest/miniconda.html)**
- Scientific packages
- Environment management

**[conda-forge](https://conda-forge.org/)**
- Community packages

</div>
</div>

---

# Pythonic Code

<div class="grid grid-cols-2 gap-4">
<div>

## ❌ Non-Pythonic
```python
data = []
for line in file:
    values = line.strip().split()
    row = []
    for val in values:
        row.append(float(val))
    data.append(row)
```

</div>
<div>

## ✅ Pythonic
```python
data = [[float(val) for val in line.split()] 
        for line in file]
```

**Key:** Use comprehensions, built-ins, and Python idioms

</div>
</div>

📺 Watch: [ArjanCodes: 25 Python Tricks](https://www.youtube.com/watch?v=8OKTAedgFYg)

---

# Clean Code: SOLID Principles

<div class="grid grid-cols-2 gap-4 text-sm">
<div>

## ❌ God Class
```python
class WeatherSystem:
    def process_data(self): ...
    def generate_forecast(self): ...
    def update_database(self): ...
    def render_map(self): ...
    def send_alerts(self): ...
```

</div>
<div>

## ✅ Single Responsibility
```python
class DataProcessor: ...
class ForecastGenerator: ...
class DatabaseManager: ...
class MapRenderer: ...
class AlertService: ...
```

</div>
</div>

📺 Watch: [ArjanCodes SOLID](https://www.youtube.com/watch?v=pTB30aXl9l4)

---

# DRY Principle

## Don't Repeat Yourself

```python
# ❌ WET (Write Everything Twice)
def celsius_to_fahrenheit(temps):
    return [t * 9/5 + 32 for t in temps]

def kelvin_to_fahrenheit(temps):
    return [(t - 273.15) * 9/5 + 32 for t in temps]

# ✅ DRY
def to_fahrenheit(temps, from_unit='celsius'):
    converters = {
        'celsius': lambda t: t * 9/5 + 32,
        'kelvin': lambda t: (t - 273.15) * 9/5 + 32
    }
    return [converters[from_unit](t) for t in temps]
```

📺 Watch: [ArjanCodes: Code Smells](https://www.youtube.com/watch?v=LrtnLEkOwFE)

---

# Testing & Quality

<div class="grid grid-cols-2 gap-4">
<div>

## 🧪 Testing Pyramid

1. **Unit Tests** (many)
   - [pytest](https://pytest.org/)
   - Test functions
2. **Integration Tests** (some)
   - Test interactions
3. **E2E Tests** (few)
   - Test workflows

</div>
<div>

## 🚀 CI/CD

```python
# test_temperature.py
def test_conversion():
    assert to_fahrenheit([0], 'celsius') == [32]
    assert to_fahrenheit([273.15], 'kelvin') == [32]
```

**[GitLab CI/CD](https://about.gitlab.com/stages-devops-lifecycle/continuous-integration/)**
- Automated testing
- Coverage reports

</div>
</div>

📺 Watch: [ArjanCodes: Unit Testing](https://www.youtube.com/watch?v=6tNS--WetLI)

---

# Version Control

<div class="grid grid-cols-2 gap-4">
<div>

## Git Basics
```bash
git init
git add .
git commit -m "feat: add temperature converter"
git push
```

</div>
<div>

## Commit Messages
```
feat: Add temperature conversion
fix: Handle edge case in parser
docs: Update installation guide
test: Add unit tests for converter
```

</div>
</div>

**Branching:** `main` → `develop` → `feature/*`

---

# Leveraging LLMs

## 🤖 AI-Assisted Development

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

### Generate
"Create a function to calculate wind chill factor"

</div>
<div>

### Convert
"Convert this MATLAB code to Python with NumPy"

</div>
<div>

### Improve
"Refactor using SOLID principles and add type hints"

</div>
</div>

**Tools:** [GitHub Copilot](https://github.com/features/copilot) • ChatGPT • Claude • [Cursor](https://cursor.sh/)

---

# Effective LLM Prompting

## 📝 Good Prompt Example

```text
Create a Python class for handling meteorological data with:
- Reading NetCDF files
- Calculating daily averages
- Handling missing data
- Following clean code principles
Include docstrings and type hints
```

**Best Practices:**
✅ Be specific • ✅ Request tests • ✅ Verify output • ✅ Iterate

---
layout: center
---

# Advanced Topics

<div class="grid grid-cols-3 gap-4">
<div>

## 🚀 HPC
- Parallel processing
- [Dask](https://dask.org/)
- GPU with [CuPy](https://cupy.dev/)

</div>
<div>

## 🧠 ML/AI
- [Scikit-learn](https://scikit-learn.org/)
- [PyTorch](https://pytorch.org/)
- Weather prediction

</div>
<div>

## 📊 Big Data
- [Xarray + Dask](https://xarray.pydata.org/en/stable/user-guide/dask.html)
- Cloud storage
- [Zarr](https://zarr.readthedocs.io/)

</div>
</div>

---

# Your Learning Plan

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## 📅 Month 1-2
- [ ] Python basics (30h)
- [ ] NumPy fundamentals (20h)
- [ ] Git basics (10h)

</div>
<div>

## 📅 Month 3-4
- [ ] Pandas & visualization
- [ ] Jupyter notebooks
- [ ] Domain libraries

</div>
<div>

## 📅 Month 5-6
- [ ] Clean code
- [ ] Testing with pytest
- [ ] CI/CD pipelines

</div>
</div>

**Remember:** Practice daily, even just 30 minutes! 🎯

---

# Community & Learning

<div class="grid grid-cols-2 gap-6">
<div>

## 🌐 Online
- [Python Forum](https://discuss.python.org/)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/python)
- [r/Python](https://www.reddit.com/r/Python/)

</div>
<div>

## 🎤 Conferences
- [PyCon](https://pycon.org/)
- [PyData](https://pydata.org/)
- [SciPy](https://conference.scipy.org/)

</div>
</div>

**Contribute:** Docs → Bugs → Tools → Mentor

---
layout: center
class: text-center
---

# Quick Reference

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## 🎓 Learn
[MIT 6.00.1x](https://www.edx.org/course/introduction-to-computer-science-and-programming-7)
[Kaggle](https://www.kaggle.com/learn/python)
[Software Carpentry](https://swcarpentry.github.io/python-novice-inflammation/)

</div>
<div>

## 📹 Watch
[ArjanCodes](https://www.youtube.com/@ArjanCodes)
[Corey Schafer](https://www.youtube.com/@coreyms)
[Real Python](https://www.youtube.com/@realpython)

</div>
<div>

## 🛠️ Tools
[VS Code](https://code.visualstudio.com/)
[uv](https://github.com/astral-sh/uv)
[pytest](https://pytest.org/)

</div>
</div>

---
layout: center
class: text-center
---

# Thank You! 🐍

## Next Steps

1. **Assess** your current level
2. **Choose** 2-3 resources
3. **Practice** daily
4. **Join** the community

<br>

### Questions?

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>