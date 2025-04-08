---
theme: gaia
_class: lead
marp: true
paginate: true
---

# Python for Meteorological Scientists

**A Comprehensive Learning Path**

---

# 1. Fundamentals

- Basic syntax and data types
- Control structures (`if`/`else`, loops)
- Functions and modules

---

# 2. Python Idioms and Best Practices

- List comprehensions
- Generator expressions
- Context managers (`with` statements)
- Error handling (`try`/`except`)

---

# 3. Scientific Python Ecosystem

- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Xarray**: N-dimensional labeled arrays and datasets

---

# 4. Domain-Specific Libraries

- **MetPy**: Meteorological data analysis
- **Cartopy**: Geospatial data processing
- **Iris**: Meteorological and oceanographic data
- **PyNIO**: Scientific data formats I/O

---

# 5. Advanced Python Concepts

- Type hints and static type checking
- Functional programming (`itertools`, `functools`)
- Object-oriented programming
- Asynchronous programming (`asyncio`)

---

# 6. Software Engineering Principles

- Clean code practices
- Design patterns
- SOLID principles
- Code refactoring and optimization

---

# 7. Version Control and Collaboration

- **Git basics**
- **GitLab** for project management and CI/CD
- Code review practices

---

# 8. Development Tools and Environments

- Integrated Development Environments (IDEs): PyCharm, VS Code
- Jupyter Notebooks for interactive development
- Virtual environments and package management (`venv`, `pip`, `conda`)

---

# 9. Containerization and Reproducibility

- **Docker basics**
- Managing containers for scientific workflows
- Docker Compose for multi-container applications

---

# 10. Continuous Integration and Deployment (CI/CD)

- Automated testing (unit tests, integration tests)
- **GitLab CI/CD pipelines**
- Deployment strategies for scientific applications

---

# 11. High-Performance Computing

- Parallel processing with `multiprocessing` and threading
- Distributed computing with **Dask**
- GPU acceleration with CUDA and **CuPy**

---

# 12. Data Management and Big Data

- Working with large datasets
- Database interactions (SQL, NoSQL)
- Cloud storage solutions (AWS S3, Google Cloud Storage)

---

# 13. Machine Learning and AI in Meteorology

- **Scikit-learn** for traditional ML algorithms
- **TensorFlow** or **PyTorch** for deep learning
- Applications in weather prediction and climate modeling

---

# 14. Visualization and Reporting

- Advanced plotting with **Seaborn** and **Plotly**
- Interactive dashboards with **Dash** or **Streamlit**
- Automated report generation with **Jupyter Notebooks**

---

# 15. Open Science and Reproducibility

- Creating reproducible research workflows
- Publishing code and data
- Contributing to open-source projects

---

# Pythonic Code: Example 1

### Non-Pythonic Version

```python
import numpy as np

def matrix_mult_sum_non_pythonic(A, B):
    C = np.zeros((A.shape[0], B.shape[1]))
    for i in range(A.shape[0]):
        for j in range(B.shape[1]):
            for k in range(A.shape[1]):
                C[i, j] += A[i, k] * B[k, j]
    s = 0
    for i in range(C.shape[0]):
        for j in range(C.shape[1]):
            s += C[i, j]
    return s
```

---

# Pythonic Code: Example 1 (Continued)

### Pythonic Version

```python
import numpy as np

def matrix_mult_sum_pythonic(A, B):
    return np.sum(A @ B)
```

---

# Pythonic Code: Example 1 (Explanation)

- **Non-Pythonic**:
  - Manual loops for matrix multiplication and summation
  - Verbose and less efficient
- **Pythonic**:
  - Utilizes NumPy's optimized operations
  - Cleaner, more readable, and faster execution

---

# Pythonic Code: Example 2

### Non-Pythonic Version

```python
def process_data_non_pythonic(filename):
    data = []
    with open(filename, 'r') as file:
        for line in file:
            values = line.strip().split()
            row = []
            for val in values:
                row.append(float(val))
            data.append(row)
    result = []
    for row in data:
        sum_row = 0
        for val in row:
            sum_row += val
        result.append(sum_row / len(row))
    return result
```

---

# Pythonic Code: Example 2 (Continued)

### Pythonic Version

```python
import numpy as np

def process_data_pythonic(filename):
    data = np.loadtxt(filename)
    return np.mean(data, axis=1)
```

---

# Pythonic Code: Example 2 (Explanation)

- **Non-Pythonic**:
  - Manual file reading and data processing
  - Nested loops increase complexity
- **Pythonic**:
  - Uses NumPy's `loadtxt` and `mean` functions
  - Simplifies code and improves performance

---

# Big Ball of Mud Anti-Pattern

- **Definition**: A codebase lacking a perceivable architecture
- **Characteristics**:
  - Spaghetti code with interwoven components
  - Difficult to maintain or extend
- **Example**:

```python
def do_everything():
    # Data processing
    # UI logic
    # Database operations
    # Error handling
    # Logging
    # All in one function
```

---

# The God Class Anti-Pattern

- **Definition**: A class that knows too much or does too much
- **Characteristics**:
  - Violates the Single Responsibility Principle
  - Becomes a maintenance nightmare
- **Example**:

```python
class WeatherSystem:
    def process_data(self): ...
    def generate_forecast(self): ...
    def update_database(self): ...
    def render_map(self): ...
    def send_alerts(self): ...
    # Many more methods
```

---

# Clean Code Principles

1. **Meaningful Names**: Clear and descriptive identifiers
2. **Single Responsibility**: Functions/classes with one job
3. **DRY (Don't Repeat Yourself)**: Avoid duplication
4. **Keep It Simple**: Simplicity over complexity
5. **Proper Error Handling**: Anticipate and handle exceptions

---

# Clean Code: Before and After

### Before Refactoring

```python
def calc_temp(data):
    s = 0
    n = 0
    for temp in data:
        s += temp
        n += 1
    avg = s / n
    return avg
```

### After Refactoring

```python
def calculate_average_temperature(temperatures):
    """Calculate the average temperature from readings."""
    if not temperatures:
        raise ValueError("No temperature data provided.")
    return sum(temperatures) / len(temperatures)
```

---

# Using LLMs for Coding

- **Enhance code quality using AI tools**
- **Example Prompts**:
  - "Refactor this code to adhere to clean code principles."
  - "Modify this code to follow the Single Responsibility Principle."
  - "Add type hints to this code."
  - "Optimize this code for performance."
  - "Make this code more modular and extensible."
  - "How can I improve this code?"
  - "Explain what this code does."
  - "Fix the error in this code."

---

# Using LLMs: Example Interaction

### Your Code

```python
def func(a,b):
    return a/b
```

### Prompt

"Refactor this code to include error handling and type hints."

### LLM's Suggestion

```python
def divide(a: float, b: float) -> float:
    """Divide two numbers safely."""
    if b == 0:
        raise ZeroDivisionError("Cannot divide by zero.")
    return a / b
```

---

# Introduction to IDEs

| IDE           | Pros                                      | Cons                                |
|---------------|-------------------------------------------|-------------------------------------|
| **VS Code**   | Lightweight, extensible, free             | Extension setup can be complex      |
| **Spyder**    | Scientific focus, MATLAB-like interface   | Less customizable                   |
| **JupyterLab**| Interactive, great for exploration        | Not ideal for large codebases       |
| **PyCharm**   | Feature-rich, intelligent code analysis   | Heavy on resources, slower startup  |

---

# Python Books

1. **"Python Crash Course"** by Eric Matthes
   - A fast-paced introduction to Python fundamentals
2. **"Python for Data Analysis"** by Wes McKinney
   - Focus on data manipulation with Pandas
3. **"Fluent Python"** by Luciano Ramalho
   - Deep dive into Python's advanced features

---

# Online Resources

- **Real Python**: [realpython.com](https://realpython.com/)
  - Tutorials and articles on Python topics
- **ArjanCodes YouTube Channel**:
  - [youtube.com/@ArjanCodes/videos](https://www.youtube.com/@ArjanCodes/videos)
  - Videos on clean code and software design

---

# Thank You!

**Questions?**

Feel free to reach out for further discussion.

---

# Additional Slides (Optional)

*Include any extra content or resources here if needed.*

---

# End of Presentation

Thank you for your attention!

---


---