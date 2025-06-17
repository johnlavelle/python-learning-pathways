# Python Learning Resources Overview for DMI Researchers

## Table of Contents
1. [Learning Platforms & Courses](#learning-platforms--courses)
2. [Books](#books)
3. [Development Tools](#development-tools)
4. [Data Access Tools](#data-access-tools)
5. [Scientific Libraries](#scientific-libraries)
6. [Visualization Libraries](#visualization-libraries)
7. [Communities & Support](#communities--support)
8. [Advanced Tools & Performance](#advanced-tools--performance)
9. [AI Coding Assistants](#ai-coding-assistants)
10. [Video Resources](#video-resources)
11. [Version Control & Collaboration](#version-control--collaboration)
12. [Testing & Code Quality](#testing--code-quality)
13. [Domain-Specific Resources](#domain-specific-resources)
14. [Quick Start Guides](#quick-start-guides)
15. [Common Pitfalls & Solutions](#common-pitfalls--solutions)

---

## 📚 Learning Platforms & Courses

### Software Carpentry Python
- **URL**: https://swcarpentry.github.io/python-novice-inflammation/
- **What it is**: Workshop-style lessons designed by researchers for researchers
- **Best for**: Complete beginners with research background
- **Time commitment**: 2 days intensive, or 2 weeks self-paced (1 hr/day)
- **Prerequisites**: None, but basic computer skills helpful
- **Key features**: 
  - Uses real scientific data (inflammation study)
  - Teaches good practices from the start
  - Includes version control basics
  - Command-line introduction
  - Defensive programming techniques
- **Learning outcomes**:
  - Load and visualize scientific data
  - Write functions and use loops effectively
  - Debug simple programs
  - Create reproducible workflows
- **Why use it**: Research-focused, peer-reviewed materials, tested on thousands of researchers

### Project Pythia
- **URL**: https://projectpythia.org/
- **What it is**: NSF-funded initiative for Python education in geosciences
- **Best for**: Earth scientists at any Python level
- **Structure**:
  - **Foundations Book**: https://foundations.projectpythia.org/
    - Python basics tailored for atmospheric science
    - Jupyter notebooks included
    - Git and GitHub introduction
  - **Pythia Cookbooks**: https://cookbooks.projectpythia.org/
    - Radar data processing
    - Climate model output analysis
    - Satellite data workflows
- **Unique features**:
  - Cloud-computing ready (works on Binder)
  - Real atmospheric/ocean datasets
  - Modern best practices (2020s era)
  - Active community contribution model
- **Example cookbook topics**:
  - CMIP6 data analysis
  - Weather radar visualization
  - Atmospheric soundings
- **Why use it**: Only learning platform specifically for atmospheric/ocean sciences

### Real Python
- **URL**: https://realpython.com/
- **What it is**: Professional Python learning platform with 500+ tutorials
- **Best for**: Intermediate learners wanting depth
- **Cost structure**:
  - Many free tutorials
  - Membership: $20/month or $199/year
  - Team plans available
- **Content types**:
  - Written tutorials with full code
  - Video courses (members only)
  - Weekly podcast
  - Learning paths (curated sequences)
- **Notable free tutorials**:
  - Python Virtual Environments Primer
  - Pandas DataFrames 101
  - Python Plotting with Matplotlib
  - Working with JSON Data
- **Member benefits**:
  - All video courses
  - Downloadable resources
  - Private Slack community
  - Office hours with instructors
- **Why use it**: Most comprehensive explanations, excellent for filling knowledge gaps

### ECMWF eLearning
- **URL**: https://learning.ecmwf.int/
- **Login**: Free ECMWF account required
- **What it is**: Official training for ECMWF tools and data
- **Course categories**:
  - **Data Access**:
    - MARS (Meteorological Archival and Retrieval System)
    - Web API usage
    - Efficient data retrieval strategies
  - **Software Tools**:
    - Metview for visualization and analysis
    - ecCodes for GRIB/BUFR handling
    - ecFlow for workflow management
  - **Numerical Weather Prediction**:
    - OpenIFS introduction
    - Understanding ECMWF products
    - Ensemble forecasting
- **Learning formats**:
  - Self-paced online modules
  - Recorded webinars
  - Hands-on exercises
  - Virtual workshops (scheduled)
- **Certification**: Completion certificates available
- **Why use it**: Essential for anyone using ECMWF data professionally

### EUMETSAT Training Portal
- **URL**: https://training.eumetsat.int/
- **What it is**: Comprehensive satellite meteorology training
- **Account**: Free registration required
- **Key learning paths**:
  - **Marine Applications**:
    - Ocean colour theory and applications
    - Sea surface temperature retrieval
    - Ocean currents from satellites
  - **Atmospheric Applications**:
    - RGB composite interpretation
    - Atmospheric motion vectors
    - Precipitation estimation
  - **Climate Monitoring**:
    - Long-term datasets
    - Calibration and validation
    - Climate data records
- **Special programs**:
  - EUMETLAB resources: https://gitlab.eumetsat.int/eumetlab
  - Copernicus training weeks
  - Jupyter notebook collections
- **Languages**: English, with some content in French, Spanish, Portuguese
- **Why use it**: Only comprehensive satellite meteorology training available

### Python for Everybody (Coursera)
- **URL**: https://www.coursera.org/specializations/python
- **Instructor**: Dr. Charles Severance (University of Michigan)
- **What it is**: Comprehensive Python introduction
- **Structure**: 5-course specialization
  1. Programming for Everybody
  2. Python Data Structures
  3. Using Python to Access Web Data
  4. Using Databases with Python
  5. Capstone: Retrieving, Processing, and Visualizing Data
- **Time commitment**: 8 months at 3 hrs/week
- **Cost**: Free to audit, $49/month for certificates
- **Why popular**: Excellent instructor, gradual progression, practical projects

---

## 📖 Books

### Python Crash Course (3rd Edition) - Eric Matthes
- **Publisher**: No Starch Press (2023)
- **Pages**: 552
- **Price**: ~$40 USD
- **URL**: https://nostarch.com/pythoncrashcourse3e
- **Structure**:
  - Part I: Basics (11 chapters)
    - Variables, data types, lists
    - Dictionaries, user input, functions
    - Classes, files, exceptions, testing
  - Part II: Projects (3 major projects)
    - Alien Invasion game (Pygame)
    - Data Visualization (Matplotlib, Plotly)
    - Web Application (Django)
- **Code resources**: https://github.com/ehmatthes/pcc_3e
- **Why it's great**:
  - Very clear explanations
  - Exercises with solutions
  - Real projects that are actually interesting
  - Updated for modern Python (3.9+)
- **Best practices taught**: PEP 8 style, virtual environments, Git basics

### Python for Data Analysis (3rd Edition) - Wes McKinney
- **Publisher**: O'Reilly (2022)
- **Pages**: 579
- **Price**: ~$60 USD (free online at https://wesmckinney.com/book/)
- **URL**: https://wesmckinney.com/book/
- **Prerequisites**: Basic Python knowledge
- **What's covered**:
  - NumPy internals and advanced features
  - Pandas from basics to advanced
  - Data cleaning and preparation (50% of real work!)
  - Time series analysis
  - Advanced GroupBy operations
  - Performance optimization
- **New in 3rd edition**:
  - Updated for Pandas 1.4
  - More on method chaining
  - Arrow and Parquet formats
  - Scaling with Dask
- **Code examples**: Downloadable Jupyter notebooks
- **Why essential**: Written by Pandas creator, shows real workflows

### A Hands-On Introduction to Using Python in the Atmospheric and Oceanic Sciences
- **Author**: Johnny Wei-Bing Lin
- **Publisher**: Self-published
- **URL**: https://www.johnny-lin.com/pyintro/
- **Price**: $35 print, FREE PDF for personal use
- **Unique aspects**:
  - All examples use atmospheric/ocean data
  - Covers specific file formats (NetCDF, GRIB)
  - Includes Fortran integration
  - Real research workflows
- **Topics covered**:
  - Basic Python with met/ocean examples
  - NumPy arrays as gridded fields
  - Visualization of maps and cross-sections
  - Time series analysis
  - Simple modeling examples
- **Exercise data**: Includes sample atmospheric datasets
- **Why use it**: Only book specifically for atmospheric/ocean scientists

### Effective Python (2nd Edition) - Brett Slatkin
- **Publisher**: Addison-Wesley (2019)
- **URL**: https://effectivepython.com/
- **What it is**: 90 specific ways to write better Python
- **Best for**: After 6 months of Python experience
- **Structure**: 90 independent items grouped into chapters
- **Key topics**:
  - Pythonic thinking
  - Lists and dictionaries best practices
  - Functions (args, kwargs, closures, decorators)
  - Classes and inheritance
  - Concurrency and parallelism
  - Robustness and performance
- **Example items**:
  - Item 3: Know the Differences Between bytes and str
  - Item 11: Use zip to Process Iterators in Parallel
  - Item 26: Define Function Decorators with functools.wraps
  - Item 74: Consider memoryview and bytearray for Zero-Copy Bytes
- **Why valuable**: Transforms working code into professional code

### Clean Code - Robert C. Martin
- **Publisher**: Prentice Hall (2008)
- **URL**: https://www.oreilly.com/library/view/clean-code-a/9780136083238/
- **What it is**: Principles for writing maintainable code
- **Language**: Examples in Java but principles universal
- **Key concepts**:
  - Meaningful names
  - Functions should do one thing
  - Comments are often failures
  - Error handling
  - Unit testing
- **Python-specific notes**: 
  - Python's "explicit is better than implicit"
  - Use Python idioms not Java patterns
  - Docstrings instead of comments
- **Why read**: Your future self will thank you

---

## 🛠️ Development Tools

### VS Code (Visual Studio Code)
- **URL**: https://code.visualstudio.com/
- **What it is**: Free, open-source code editor by Microsoft
- **Download size**: ~100MB
- **Platforms**: Windows, macOS, Linux
- **Essential extensions for Python**:
  - **Python** (ms-python.python): IntelliSense, debugging, formatting
  - **Pylance** (ms-python.vscode-pylance): Fast language server
  - **Jupyter** (ms-toolsai.jupyter): Notebook support
  - **GitLens** (eamodio.gitlens): Supercharge Git
  - **Remote-SSH** (ms-vscode-remote.remote-ssh): Edit on remote servers
  - **Python Docstring Generator** (njpwerner.autodocstring): Auto docstrings
- **Key features for scientists**:
  - Interactive Python window
  - Variable explorer
  - Plot viewer
  - Integrated terminal
  - Git integration
  - Remote development
- **Settings to configure** (settings.json):
  ```json
  {
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "python.formatting.provider": "black",
    "python.formatting.blackArgs": ["--line-length", "88"],
    "editor.formatOnSave": true,
    "python.testing.pytestEnabled": true
  }
  ```
- **Tips**:
  - Use Command Palette (Ctrl/Cmd+Shift+P)
  - Learn keyboard shortcuts
  - Configure workspace settings per project
  - Use multi-cursor editing
- **Why VS Code**: Best free Python IDE, huge community, monthly updates

### PyCharm
- **URL**: https://www.jetbrains.com/pycharm/
- **Editions**:
  - Community (free): Full Python development
  - Professional ($199/year): Scientific tools, remote, web
- **Strengths**:
  - Superior debugging capabilities
  - Excellent refactoring tools
  - Built-in scientific mode
  - Database tools (Pro)
  - Better code completion than VS Code
- **Scientific features** (Pro only):
  - Interactive scientific console
  - Data viewer for NumPy/Pandas
  - Integrated Jupyter notebooks
  - R plugin available
- **When to choose PyCharm**:
  - Large codebases
  - Complex debugging needs
  - Heavy refactoring
  - Team using JetBrains tools

### Miniconda / Conda
- **Miniconda URL**: https://docs.conda.io/en/latest/miniconda.html
- **What it is**: Minimal conda installer (~400MB vs Anaconda's 3GB)
- **Installation tips**:
  - Say YES to "conda init" during install
  - Don't add to system PATH on Windows
  - Install for "Just Me" not "All Users"
- **Essential conda commands**:
  ```bash
  # Environment management
  conda create -n myenv python=3.11
  conda activate myenv
  conda deactivate
  conda env list
  conda env remove -n myenv
  
  # Package management
  conda install numpy pandas xarray
  conda install -c conda-forge package_name
  conda update --all
  conda list
  
  # Environment export/import
  conda env export > environment.yml
  conda env create -f environment.yml
  ```
- **Conda channels**:
  - defaults: Anaconda's curated packages
  - conda-forge: Community packages (usually more up-to-date)
  - Set priority: `conda config --set channel_priority strict`
- **Mamba**: Drop-in replacement for faster solving
  ```bash
  conda install mamba -n base -c conda-forge
  mamba install numpy  # Much faster!
  ```
- **Environment file example** (environment.yml):
  ```yaml
  name: dmi-analysis
  channels:
    - conda-forge
    - defaults
  dependencies:
    - python=3.11
    - numpy
    - pandas
    - xarray
    - dask
    - netcdf4
    - matplotlib
    - cartopy
    - jupyter
    - pip
    - pip:
      - ecmwf-opendata
      - copernicus-marine-client
  ```

### Jupyter Ecosystem
- **JupyterLab**: https://jupyter.org/
- **What it is**: Web-based interactive computing platform
- **Installation**: `conda install -c conda-forge jupyterlab`
- **Starting JupyterLab**: `jupyter lab`
- **Key features**:
  - Multiple notebooks in tabs
  - File browser
  - Terminal access
  - Extension system
  - Real-time collaboration (new)
- **Essential extensions**:
  - Variable Inspector: See all variables
  - Table of Contents: Navigate long notebooks
  - Git: Version control integration
  - DrawIO: Diagrams in notebooks
- **Best practices**:
  - Clear output before committing
  - Use meaningful cell divisions
  - Don't use notebooks for complex logic
  - Name notebooks descriptively
  - Use markdown cells liberally
- **Keyboard shortcuts** (Command mode):
  - `A`: Insert cell above
  - `B`: Insert cell below
  - `DD`: Delete cell
  - `M`: Change to Markdown
  - `Y`: Change to code
  - `Shift+Enter`: Run cell and select below

### Alternative Editors

#### Spyder
- **URL**: https://www.spyder-ide.org/
- **What it is**: Scientific Python IDE (like MATLAB)
- **Best for**: MATLAB users transitioning to Python
- **Features**: Variable explorer, plots pane, help pane
- **Install**: `conda install spyder`

#### Vim/Neovim with Python
- **For**: Power users who love keyboard efficiency
- **Plugins**: python-mode, jedi-vim, black
- **Config**: Extensive setup required

---

## 🌍 Data Access Tools

### ECMWF Open Data
- **GitHub**: https://github.com/ecmwf/ecmwf-opendata
- **PyPI**: https://pypi.org/project/ecmwf-opendata/
- **Documentation**: https://confluence.ecmwf.int/display/DAC/ECMWF+open+data
- **What it is**: Python client for ECMWF real-time open data
- **Installation**: `pip install ecmwf-opendata`
- **Data available**: 
  - IFS HRES (0.4° for open data, ~44km)
  - IFS ENS (0.8° for open data, ~88km)
  - Forecasts up to 240 hours (10 days)
  - Updated 4 times daily (00, 06, 12, 18 UTC)
- **Parameters available**: Limited subset including:
  - Temperature (2t, t)
  - Pressure (msl, sp)
  - Wind (10u, 10v, u, v)
  - Precipitation (tp)
  - Cloud cover (tcc)
- **Basic usage**:
  ```python
  from ecmwf.opendata import Client
  client = Client()
  
  # Latest forecast for temperature
  client.retrieve(
      type="fc",
      param="2t",
      step=24,
      target="temperature_24h.grib2"
  )
  
  # Multiple parameters and steps
  client.retrieve(
      type="fc",
      param=["2t", "10u", "10v"],
      step=[0, 6, 12, 18, 24],
      target="multi_param.grib2"
  )
  ```
- **Advanced options**:
  ```python
  # Specific date and time
  client.retrieve(
      date="2024-01-15",
      time="12",
      type="fc",
      param="tp",
      step=list(range(0, 49, 6)),
      target="precipitation.grib2"
  )
  
  # Area subset (N/W/S/E)
  client.retrieve(
      type="fc",
      param="2t",
      step=24,
      area=[60, 10, 50, 15],  # Denmark region
      target="denmark_temp.grib2"
  )
  ```

### CDS API (Climate Data Store)
- **Homepage**: https://cds.climate.copernicus.eu/
- **API Guide**: https://cds.climate.copernicus.eu/api-how-to
- **PyPI**: `pip install cdsapi`
- **Setup required**: 
  1. Register at CDS
  2. Accept dataset licenses
  3. Create `.cdsapirc` file:
     ```
     url: https://cds.climate.copernicus.eu/api/v2
     key: YOUR-UID:YOUR-API-KEY
     ```
- **Major datasets**:
  - **ERA5**: 1940-present, hourly, 0.25°
  - **ERA5-Land**: Higher resolution land variables
  - **Seasonal forecasts**: Multiple systems
  - **Climate projections**: CMIP6, CORDEX
  - **Satellite observations**: Various missions
- **ERA5 example**:
  ```python
  import cdsapi
  c = cdsapi.Client()
  
  # Download temperature for Denmark, Jan 2023
  c.retrieve(
      'reanalysis-era5-single-levels',
      {
          'product_type': 'reanalysis',
          'format': 'netcdf',
          'variable': '2m_temperature',
          'year': '2023',
          'month': '01',
          'day': list(range(1, 32)),
          'time': ['00:00', '06:00', '12:00', '18:00'],
          'area': [58, 8, 54, 13],  # N, W, S, E
      },
      'denmark_temp_jan2023.nc'
  )
  ```
- **Tips**:
  - Use web interface to build requests
  - Download efficiency: fewer large requests > many small
  - Check queue status online
  - Consider ERA5 monthly means for climatologies

### Copernicus Marine Service (CMEMS)
- **Homepage**: https://marine.copernicus.eu/
- **Toolbox**: https://pypi.org/project/copernicus-marine-client/
- **Documentation**: https://help.marine.copernicus.eu/
- **Installation**: `pip install copernicus-marine-client`
- **Registration**: Free at https://marine.copernicus.eu/
- **Data categories**:
  - **Ocean Physics**: Temperature, salinity, currents, sea level
  - **Ocean Biogeochemistry**: Chlorophyll, nutrients, pH, oxygen
  - **Sea Ice**: Concentration, thickness, drift
  - **Waves**: Height, period, direction
- **Coverage**: Global, regional (Arctic, Baltic, Mediterranean, etc.)
- **Basic usage**:
  ```python
  import copernicus_marine_client as cm
  
  # List available datasets
  cm.describe()
  
  # Open dataset (lazy loading with xarray)
  ds = cm.open_dataset(
      dataset_id="cmems_mod_glo_phy_anfc_0.083deg_P1D-m",
      variables=["thetao", "so"],  # temperature, salinity
      minimum_longitude=10,
      maximum_longitude=13,
      minimum_latitude=54,
      maximum_latitude=58,
      start_datetime="2023-01-01",
      end_datetime="2023-01-31"
  )
  
  # Download to file
  cm.subset(
      dataset_id="cmems_mod_glo_phy_anfc_0.083deg_P1D-m",
      variables=["thetao", "so", "uo", "vo"],
      minimum_longitude=10,
      maximum_longitude=13,
      minimum_latitude=54,
      maximum_latitude=58,
      start_datetime="2023-01-01",
      end_datetime="2023-01-31",
      output_filename="baltic_ocean_data.nc"
  )
  ```
- **Product selection tips**:
  - "anfc" = analysis/forecast
  - "my" = multi-year (reanalysis)
  - Check spatial/temporal resolution
  - Note depth levels available

### EUMDAC (EUMETSAT Data Access Client)
- **PyPI**: https://pypi.org/project/eumdac/
- **Documentation**: https://user.eumetsat.int/docs/
- **GitLab**: https://gitlab.eumetsat.int/eumetlab/data-services/eumdac
- **Installation**: 
  ```bash
  pip install eumdac
  # or
  conda install -c eumetsat eumdac
  ```
- **Authentication**: Uses token from https://api.eumetsat.int/api-key/
- **Supported satellites**:
  - Meteosat Second Generation (MSG)
  - Meteosat Third Generation (MTG)
  - Metop series
  - Sentinel-3 (ocean/land)
  - Sentinel-6 (altimetry)
  - Jason series
- **Usage example**:
  ```python
  import eumdac
  
  # Create credentials
  credentials = eumdac.AccessToken(token="your-token-here")
  datastore = eumdac.DataStore(credentials)
  
  # Search for products
  collections = datastore.collections
  
  # Find Sentinel-3 OLCI products
  collection = datastore.get_collection("EO:EUM:DAT:SENTINEL-3:OL_1_EFR___")
  products = collection.search(
      start="2023-01-01",
      end="2023-01-02",
      geo={"type": "Polygon", "coordinates": [[[10,54],[13,54],[13,58],[10,58],[10,54]]]}
  )
  
  # Download products
  for product in products:
      product.download()
  ```

### Satpy
- **Documentation**: https://satpy.readthedocs.io/
- **GitHub**: https://github.com/pytroll/satpy
- **Installation**: `conda install -c conda-forge satpy`
- **What it is**: Python library for earth-observing satellite data
- **Key capabilities**:
  - Read 100+ satellite data formats
  - Create RGB composites
  - Resample to common grids
  - Atmospheric corrections
  - Parallelize with Dask
- **Supported instruments** (selection):
  - **Geostationary**: SEVIRI, ABI, AHI, AMI
  - **Polar**: MODIS, VIIRS, AVHRR, OLCI, SLSTR
  - **Other**: SAR, ASCAT, atmospheric sounders
- **Basic workflow**:
  ```python
  from satpy import Scene
  from glob import glob
  
  # Find and load files
  files = glob('/data/MSG/*202301151200*')
  scn = Scene(filenames=files, reader='seviri_l1b_hrit')
  
  # Load composite
  scn.load(['natural_color'])
  
  # Resample to area
  local_scn = scn.resample('denmark', radius_of_influence=5000)
  
  # Save image
  local_scn.save_dataset('natural_color', 'msg_denmark.png')
  
  # Save data
  local_scn.save_datasets(writer='cf', filename='msg_denmark.nc')
  ```
- **Creating custom composites**:
  ```python
  # Define RGB composite
  from satpy.composites import GenericCompositor
  comp = GenericCompositor("my_rgb")
  
  # Create composite from channels
  composite = comp([scn['IR_087'], scn['IR_108'], scn['IR_120']])
  ```
- **Performance tips**:
  - Use `reader_kwargs` to limit what's loaded
  - Resample before enhancement for speed
  - Use Dask for large datasets
  - Save to zarr for cloud workflows

---

## 📊 Scientific Libraries

### NumPy
- **Homepage**: https://numpy.org/
- **Documentation**: https://numpy.org/doc/stable/
- **Installation**: `conda install numpy` or `pip install numpy`
- **What it is**: Foundation of scientific Python
- **Learning path**:
  1. [Absolute Beginners Guide](https://numpy.org/doc/stable/user/absolute_beginners.html)
  2. [NumPy Quickstart](https://numpy.org/doc/stable/user/quickstart.html)
  3. [NumPy for MATLAB users](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html)
- **Core concepts**:
  - **ndarray**: N-dimensional array object
  - **Broadcasting**: Rules for element-wise operations
  - **Vectorization**: Avoid loops for speed
  - **Views vs copies**: Memory efficiency
- **Essential operations**:
  ```python
  import numpy as np
  
  # Array creation
  arr = np.array([1, 2, 3])
  zeros = np.zeros((3, 4))
  ones = np.ones((3, 4))
  range_arr = np.arange(0, 10, 0.5)
  linspace_arr = np.linspace(0, 1, 50)
  
  # Random arrays
  rng = np.random.default_rng(42)  # Seed for reproducibility
  random_arr = rng.normal(0, 1, size=(100, 100))
  
  # Array operations
  a = np.array([[1, 2], [3, 4]])
  b = np.array([[5, 6], [7, 8]])
  
  c = a + b  # Element-wise
  d = a @ b  # Matrix multiplication (Python 3.5+)
  e = np.dot(a, b)  # Also matrix multiplication
  
  # Broadcasting example
  arr = np.ones((3, 4))
  arr = arr + 10  # Adds 10 to all elements
  arr = arr * np.array([1, 2, 3, 4])  # Multiplies columns
  
  # Indexing and slicing
  arr = np.arange(10)
  print(arr[5])      # Single element
  print(arr[2:7])    # Slice
  print(arr[::2])    # Every 2nd element
  print(arr[::-1])   # Reverse
  
  # Boolean indexing
  data = rng.normal(0, 1, 1000)
  positive = data[data > 0]
  extreme = data[np.abs(data) > 2]
  ```
- **Performance tips**:
  - Use vectorized operations
  - Avoid Python loops
  - Use `np.einsum` for complex operations
  - Consider `numba` for custom functions
- **Common pitfalls**:
  - Modifying views affects original
  - Integer division changed Python 2→3
  - Default int type varies by platform

### Pandas
- **Homepage**: https://pandas.pydata.org/
- **Documentation**: https://pandas.pydata.org/docs/
- **10-minute intro**: https://pandas.pydata.org/docs/user_guide/10min.html
- **Installation**: `conda install pandas`
- **What it is**: Data manipulation and analysis
- **Core data structures**:
  - **Series**: 1D labeled array
  - **DataFrame**: 2D labeled data structure
- **Key features**:
  - Label-based indexing
  - Automatic alignment
  - Time series functionality
  - GroupBy operations
  - Missing data handling
  - IO tools (CSV, Excel, SQL, etc.)
- **Essential operations**:
  ```python
  import pandas as pd
  
  # Creating DataFrames
  df = pd.DataFrame({
      'station': ['CPH', 'AAR', 'ODE', 'CPH', 'AAR', 'ODE'],
      'date': pd.date_range('2023-01-01', periods=6),
      'temperature': [2.1, 1.8, 2.5, 2.3, 1.9, 2.6],
      'precipitation': [5.2, 3.1, 4.5, 0.0, 2.3, 1.2]
  })
  
  # Reading data
  df = pd.read_csv('data.csv', parse_dates=['date'])
  df = pd.read_excel('data.xlsx', sheet_name='Sheet1')
  
  # Exploration
  df.head()
  df.info()
  df.describe()
  df['temperature'].value_counts()
  
  # Selection
  df['temperature']  # Column
  df[['station', 'temperature']]  # Multiple columns
  df.loc[df['station'] == 'CPH']  # Boolean indexing
  df.iloc[0:3]  # Position-based
  
  # GroupBy operations
  monthly = df.groupby('station')['temperature'].mean()
  stats = df.groupby('station').agg({
      'temperature': ['mean', 'min', 'max'],
      'precipitation': 'sum'
  })
  
  # Time series
  df.set_index('date', inplace=True)
  monthly = df.resample('M').mean()
  rolling = df.rolling('7D').mean()
  
  # Pivoting
  pivot = df.pivot_table(
      values='temperature',
      index='date',
      columns='station',
      aggfunc='mean'
  )
  ```
- **Best practices**:
  - Use method chaining
  - Avoid loops - use vectorized operations
  - Be explicit about copies vs views
  - Handle missing data appropriately

### Xarray
- **Homepage**: https://xarray.dev/
- **Documentation**: https://docs.xarray.dev/
- **Tutorial**: https://tutorial.xarray.dev/
- **Why Xarray**: "Pandas for N-dimensional data"
- **Installation**: `conda install xarray`
- **Key features**:
  - Labeled N-dimensional arrays
  - NetCDF/GRIB/Zarr integration
  - Lazy loading with Dask
  - CF conventions aware
  - Intuitive operations
- **Data structures**:
  - **DataArray**: N-D array with labels
  - **Dataset**: Dict-like container of DataArrays
- **Essential usage**:
  ```python
  import xarray as xr
  
  # Open datasets
  ds = xr.open_dataset('era5_data.nc')
  
  # Lazy loading multiple files
  ds = xr.open_mfdataset('era5_*.nc', combine='by_coords')
  
  # Explore structure
  print(ds)
  print(ds.dims)
  print(ds.coords)
  print(ds.data_vars)
  
  # Selection
  # By value
  ds_dk = ds.sel(latitude=slice(58, 54), longitude=slice(8, 13))
  ds_jan = ds.sel(time='2023-01')
  
  # By index
  ds_subset = ds.isel(time=0, latitude=slice(10, 20))
  
  # Nearest neighbor
  point = ds.sel(latitude=55.7, longitude=12.6, method='nearest')
  
  # Computation
  monthly_mean = ds.groupby('time.month').mean()
  anomaly = ds.groupby('time.month') - monthly_mean
  
  # Plotting
  ds.temperature.plot()  # 2D plot
  ds.temperature.mean(['longitude']).plot()  # Lat-time Hovmöller
  
  # Save
  ds.to_netcdf('processed.nc')
  ds.to_zarr('processed.zarr')
  ```
- **Working with coordinates**:
  ```python
  # Add coordinates
  ds = ds.assign_coords(height=("level", [1000, 850, 500]))
  
  # Multi-dimensional coordinates
  lon2d, lat2d = np.meshgrid(lons, lats)
  ds = ds.assign_coords(lon=(["y", "x"], lon2d),
                        lat=(["y", "x"], lat2d))
  ```
- **CF Conventions**:
  ```python
  # Decode CF conventions
  ds = xr.open_dataset('file.nc', decode_cf=True)
  
  # Access CF attributes
  print(ds.temperature.attrs['units'])
  print(ds.temperature.attrs['long_name'])
  ```

### Dask
- **Homepage**: https://dask.org/
- **Documentation**: https://docs.dask.org/
- **What it is**: Parallel computing library
- **Installation**: `conda install dask`
- **When to use**:
  - Data larger than memory
  - Embarrassingly parallel operations
  - Multi-core/cluster computing
- **Integration with Xarray**:
  ```python
  # Open with Dask
  ds = xr.open_mfdataset('era5_*.nc', 
                         chunks={'time': 10, 'latitude': 100})
  
  # Parallel computation
  result = ds.temperature.mean(dim='time').compute()
  
  # Monitor progress
  from dask.diagnostics import ProgressBar
  with ProgressBar():
      result = big_calculation.compute()
  ```

---

## 📈 Visualization Libraries

### Matplotlib
- **Homepage**: https://matplotlib.org/
- **Gallery**: https://matplotlib.org/stable/gallery/index.html
- **Tutorials**: https://matplotlib.org/stable/tutorials/index.html
- **What it is**: Foundational plotting library
- **Installation**: `conda install matplotlib`
- **Two interfaces**:
  1. **pyplot** (MATLAB-like): Quick plots
  2. **Object-oriented**: Full control
- **Essential plotting**:
  ```python
  import matplotlib.pyplot as plt
  import numpy as np
  
  # Quick plot
  x = np.linspace(0, 10, 100)
  y = np.sin(x)
  plt.plot(x, y)
  plt.xlabel('Time')
  plt.ylabel('Amplitude')
  plt.title('Sine Wave')
  plt.show()
  
  # Object-oriented (recommended)
  fig, ax = plt.subplots(figsize=(10, 6))
  ax.plot(x, y, 'b-', label='sin(x)')
  ax.plot(x, np.cos(x), 'r--', label='cos(x)')
  ax.set_xlabel('Time')
  ax.set_ylabel('Amplitude')
  ax.set_title('Trigonometric Functions')
  ax.legend()
  ax.grid(True, alpha=0.3)
  plt.show()
  
  # Subplots
  fig, (ax1, ax2) = plt.subplots(2, 1, figsize=(10, 8))
  ax1.plot(x, y)
  ax1.set_title('Sine')
  ax2.plot(x, np.cos(x))
  ax2.set_title('Cosine')
  plt.tight_layout()
  
  # Save figure
  fig.savefig('plot.png', dpi=300, bbox_inches='tight')
  ```
- **Customization**:
  ```python
  # Style sheets
  plt.style.use('seaborn-v0_8-darkgrid')
  
  # Or create custom style
  plt.rcParams['figure.figsize'] = (10, 6)
  plt.rcParams['font.size'] = 12
  plt.rcParams['lines.linewidth'] = 2
  ```

### Cartopy
- **Homepage**: https://scitools.org.uk/cartopy/
- **Gallery**: https://scitools.org.uk/cartopy/docs/latest/gallery/index.html
- **Installation**: `conda install -c conda-forge cartopy`
- **What it is**: Cartographic projections and mapping
- **Key features**:
  - Map projections (100+)
  - Coastlines and borders
  - Grid lines and labels
  - Data transformation
- **Basic map**:
  ```python
  import cartopy.crs as ccrs
  import cartopy.feature as cfeature
  
  # Create map
  fig = plt.figure(figsize=(12, 8))
  ax = fig.add_subplot(1, 1, 1, projection=ccrs.PlateCarree())
  
  # Add features
  ax.add_feature(cfeature.LAND)
  ax.add_feature(cfeature.OCEAN)
  ax.add_feature(cfeature.COASTLINE)
  ax.add_feature(cfeature.BORDERS, linestyle=':')
  ax.add_feature(cfeature.LAKES, alpha=0.5)
  ax.add_feature(cfeature.RIVERS)
  
  # Set extent (Denmark)
  ax.set_extent([8, 13, 54, 58], crs=ccrs.PlateCarree())
  
  # Add gridlines
  gl = ax.gridlines(crs=ccrs.PlateCarree(), draw_labels=True,
                    linewidth=2, color='gray', alpha=0.5, linestyle='--')
  gl.top_labels = False
  gl.right_labels = False
  
  plt.show()
  ```
- **Plotting data**:
  ```python
  # With xarray
  data = xr.open_dataset('temperature.nc')
  
  fig = plt.figure(figsize=(12, 8))
  ax = fig.add_subplot(1, 1, 1, projection=ccrs.PlateCarree())
  
  # Plot data
  im = ax.contourf(data.longitude, data.latitude, data.temperature,
                   transform=ccrs.PlateCarree(), cmap='RdBu_r')
  
  # Add colorbar
  plt.colorbar(im, ax=ax, orientation='horizontal', pad=0.05)
  
  # Add map features
  ax.coastlines()
  ax.add_feature(cfeature.BORDERS)
  ```

### Holoviews
- **Homepage**: https://holoviews.org/
- **Getting Started**: https://holoviews.org/getting_started/Introduction.html
- **Installation**: `conda install -c conda-forge holoviews`
- **What it is**: High-level data visualization
- **Key advantage**: Less code for complex plots
- **Example**:
  ```python
  import holoviews as hv
  import xarray as xr
  hv.extension('matplotlib')
  
  # Load data
  ds = xr.open_dataset('era5.nc')
  
  # Create interactive plot with one line
  temp_plot = hv.Dataset(ds).to(hv.Image, ['longitude', 'latitude'])
  ```

### Seaborn
- **Homepage**: https://seaborn.pydata.org/
- **Gallery**: https://seaborn.pydata.org/examples/index.html
- **What it is**: Statistical data visualization
- **Best for**: Statistical plots, themes
- **Example**:
  ```python
  import seaborn as sns
  
  # Set theme
  sns.set_theme(style="whitegrid")
  
  # Statistical plots
  sns.scatterplot(data=df, x='temperature', y='precipitation',
                  hue='station', size='wind_speed')
  
  # Distributions
  sns.histplot(data=df, x='temperature', hue='season', kde=True)
  ```

---

## 🤝 Communities & Support

### Pytroll Slack
- **What it is**: Community for satellite data processing
- **How to join**: 
  1. Go to https://pytroll.github.io/
  2. Click "Getting in Touch"
  3. Join Slack via invitation link
- **Channels to join**:
  - #general - General discussion
  - #satpy - Satpy specific help
  - #pyresample - Resampling questions
  - #showcase - Share your work
- **Why valuable**:
  - Satpy developers respond quickly
  - European timezone friendly
  - Very welcoming to beginners
  - Real operational users
- **Etiquette**:
  - Search before asking
  - Provide minimal examples
  - Share solutions back

### Pangeo Community
- **Homepage**: https://pangeo.io/
- **Discourse**: https://discourse.pangeo.io/
- **What it is**: Community for big data geoscience
- **Key topics**:
  - Cloud-native workflows
  - Xarray optimization
  - Zarr storage
  - Dask scaling
  - JupyterHub deployments
- **Resources**:
  - Weekly community meetings
  - Tutorial collections
  - Example galleries
  - Cloud infrastructure guides
- **How to contribute**:
  - Share workflows
  - Report issues
  - Improve documentation
  - Present at meetings

### Project Pythia
- **Homepage**: https://projectpythia.org/
- **GitHub**: https://github.com/ProjectPythia
- **Community page**: https://projectpythia.org/community.html
- **What it is**: Education-focused community
- **How to participate**:
  - Pythia Cookbooks - contribute examples
  - Pythia Foundations - improve tutorials
  - Office hours - get help
  - Town halls - community updates
- **Cookbook contribution**:
  1. Fork cookbook template
  2. Add your scientific workflow
  3. Submit pull request
  4. Get review and feedback

### Stack Overflow
- **Python tag**: https://stackoverflow.com/questions/tagged/python
- **Scientific tags**:
  - [numpy]: Core array operations
  - [pandas]: DataFrame questions
  - [matplotlib]: Plotting issues
  - [xarray]: NetCDF/multidimensional
- **How to ask good questions**:
  - Minimal reproducible example
  - Clear problem statement
  - What you've tried
  - Expected vs actual output
  - Version information

### ECMWF Support
- **Confluence**: https://confluence.ecmwf.int/
- **User Forum**: https://confluence.ecmwf.int/display/UDOC/User+Forum
- **Support Portal**: https://support.ecmwf.int/
- **Topics covered**:
  - Data access issues
  - MARS queries
  - Product questions
  - Technical problems
- **Before posting**:
  - Check documentation
  - Search existing issues
  - Prepare MARS request details

### Local Communities

#### DMI Python Users Group
- Internal Slack channel
- Monthly virtual meetups
- Code review sessions
- Shared notebooks repository

#### Nordic RSE (Research Software Engineers)
- **Website**: https://nordic-rse.org/
- **Events**: Annual conference
- **Focus**: Best practices in research software

---

## 🚀 Advanced Tools & Performance

### Numba
- **Homepage**: https://numba.pydata.org/
- **What it is**: JIT compiler for Python
- **Installation**: `conda install numba`
- **When to use**:
  - Numerical loops that can't be vectorized
  - Custom numerical algorithms
  - Real-time processing needs
- **Basic usage**:
  ```python
  from numba import jit
  import numpy as np
  
  @jit(nopython=True)
  def haversine(lat1, lon1, lat2, lon2):
      """Calculate distance between two points on Earth"""
      R = 6371  # Earth radius in km
      dlat = np.radians(lat2 - lat1)
      dlon = np.radians(lon2 - lon1)
      a = (np.sin(dlat/2)**2 + 
           np.cos(np.radians(lat1)) * np.cos(np.radians(lat2)) * 
           np.sin(dlon/2)**2)
      c = 2 * np.arcsin(np.sqrt(a))
      return R * c
  
  # First call compiles, subsequent calls are fast
  distance = haversine(55.7, 12.6, 57.0, 10.0)
  ```
- **Advanced features**:
  - Parallel loops with `prange`
  - CUDA GPU support
  - Vectorize Python functions
  - Cache compiled functions

### CuPy
- **Homepage**: https://cupy.dev/
- **What it is**: NumPy-compatible GPU library
- **Installation**: Complex - requires CUDA
- **When to use**: Large array operations on NVIDIA GPUs
- **Example**:
  ```python
  import cupy as cp
  
  # Runs on GPU
  x_gpu = cp.array([1, 2, 3])
  y_gpu = cp.array([4, 5, 6])
  z_gpu = x_gpu + y_gpu
  
  # Transfer back to CPU
  z_cpu = cp.asnumpy(z_gpu)
  ```

### Zarr
- **Homepage**: https://zarr.dev/
- **What it is**: Cloud-optimized array storage
- **Why use**:
  - Cloud-native format
  - Concurrent reads/writes
  - Compression
  - Chunked storage
- **With Xarray**:
  ```python
  # Save to Zarr
  ds.to_zarr('data.zarr', mode='w')
  
  # Open from cloud
  ds = xr.open_zarr('s3://bucket/data.zarr')
  ```

### Intake
- **Homepage**: https://intake.readthedocs.io/
- **What it is**: Data catalog system
- **Purpose**: Simplify data access
- **Example catalog** (catalog.yml):
  ```yaml
  sources:
    era5_temperature:
      driver: netcdf
      args:
        urlpath: /data/era5/temperature/*.nc
        chunks:
          time: 10
    ocean_forecast:
      driver: zarr
      args:
        urlpath: s3://bucket/ocean/forecast.zarr
  ```

---

## 🤖 AI Coding Assistants

### GitHub Copilot
- **URL**: https://github.com/features/copilot
- **Cost**: $10/month, free for students/teachers
- **IDE Support**: VS Code, PyCharm, Neovim
- **Best for**:
  - Autocompletion on steroids
  - Boilerplate generation
  - Test writing
  - Documentation
- **How to use effectively**:
  - Write clear comments first
  - Use descriptive names
  - Accept/reject suggestions (Tab/Esc)
  - Review all generated code
- **Example prompting**:
  ```python
  # Calculate wind chill factor using the formula
  # for temperatures in Celsius and wind speed in m/s
  def calculate_wind_chill(temp_c, wind_ms):
      # Copilot will complete this
  ```

### Claude (Anthropic)
- **URL**: https://claude.ai/
- **Strengths**:
  - Explains complex concepts clearly
  - Good at refactoring
  - Catches subtle bugs
  - Writes comprehensive tests
- **Scientific use cases**:
  - "Explain this atmospheric physics equation"
  - "Convert this MATLAB code to Python/NumPy"
  - "Add type hints and docstrings to this function"
  - "What's wrong with this NetCDF reading code?"
- **Best practices**:
  - Provide context about your domain
  - Ask for explanations, not just code
  - Verify scientific accuracy

### ChatGPT
- **URL**: https://chat.openai.com/
- **Free tier**: GPT-3.5
- **Paid tier**: GPT-4 ($20/month)
- **Strengths**:
  - Wide knowledge base
  - Good for learning concepts
  - Debugging assistance
- **Example prompts**:
  - "Create a Python function to calculate relative humidity from temperature and dewpoint with proper error handling"
  - "Explain the difference between NumPy's copy() and view()"
  - "How do I parallelize this xarray computation with Dask?"

### Prompt Engineering for Science
- **Be specific**: Include units, coordinate systems, conventions
- **Provide context**: "For meteorological data in NetCDF format..."
- **Request validation**: "Include assertions for physical constraints"
- **Ask for tests**: "Write pytest tests for edge cases"
- **Example good prompt**:
  ```
  Create a Python function that:
  - Reads ERA5 temperature data from NetCDF
  - Calculates daily maximum temperatures
  - Handles missing data (NaN values)
  - Returns xarray DataArray with proper metadata
  - Uses CF conventions for attributes
  Include docstring with parameters and examples
  ```

---

## 📹 Video Resources

### YouTube Channels

#### ArjanCodes
- **URL**: https://www.youtube.com/@ArjanCodes
- **Subscribers**: 500k+
- **Focus**: Software design, clean code, best practices
- **Key playlists**:
  - Software Design Patterns in Python
  - Code Roasts (refactoring real code)
  - Python Features You Should Know
- **Why watch**: Transforms intermediate coders into professionals

#### mCoding (James Murphy)
- **URL**: https://www.youtube.com/@mCoding
- **Focus**: Deep dives into Python internals
- **Notable videos**:
  - "Python's most POWERFUL feature"
  - "Async for the impatient"
  - "The flaws of inheritance"
- **Why watch**: Understand Python deeply

#### Corey Schafer
- **URL**: https://www.youtube.com/@coreyms
- **Focus**: Comprehensive Python tutorials
- **Series**:
  - Python OOP Tutorial (best on YouTube)
  - Flask/Django web development
  - Git tutorials
- **Why watch**: Clear, thorough explanations

#### Real Python
- **URL**: https://www.youtube.com/@realpython
- **What**: Video version of articles
- **Content**: Interviews, tutorials, tips

#### sentdex
- **URL**: https://www.youtube.com/@sentdex
- **Focus**: Python + data science + ML
- **Projects**: Self-driving car, trading bots

### MetPy Mondays
- **URL**: https://www.youtube.com/playlist?list=PLQut5OXpV-0ir4IdllSt1iEZKTwFBa7kO
- **By**: Unidata (UCAR)
- **Format**: Weekly 30-minute tutorials
- **Topics covered**:
  - Sounding analysis
  - Surface observations
  - Cross sections
  - Satellite data
  - Model output
- **Code**: Available on GitHub

### Conference Talks

#### PyData
- **YouTube**: https://www.youtube.com/user/PyDataTV
- **Notable talks**: Search for "xarray", "dask", "pangeo"

#### SciPy Conference
- **YouTube**: https://www.youtube.com/user/EnthoughtMedia
- **Tracks**: Earth & Space Science mini-symposium

---

## 🔧 Version Control & Collaboration

### Git Fundamentals
- **Pro Git Book**: https://git-scm.com/book (free, translated)
- **Interactive Tutorial**: https://learngitbranching.js.org/
- **GitHub Skills**: https://skills.github.com/
- **Essential commands**:
  ```bash
  # Configuration (one time)
  git config --global user.name "Your Name"
  git config --global user.email "you@dmi.dk"
  
  # Start new project
  git init
  git add .
  git commit -m "Initial commit"
  
  # Daily workflow
  git status
  git add file.py
  git commit -m "Add temperature analysis function"
  git push origin main
  
  # Branching
  git checkout -b feature/add-precipitation
  # ... make changes ...
  git add .
  git commit -m "Add precipitation analysis"
  git checkout main
  git merge feature/add-precipitation
  
  # Collaboration
  git clone https://github.com/user/repo.git
  git pull origin main
  git push origin feature-branch
  ```

### GitHub/GitLab
- **GitHub**: Public repositories, community
- **GitLab**: Can self-host, CI/CD built-in
- **DMI GitLab**: Internal instance for private work
- **Best practices**:
  - Write descriptive commit messages
  - Use branches for features
  - Review before merging
  - Tag releases

### Collaborative Workflows

#### GitHub Flow
1. Create branch from main
2. Make changes
3. Open Pull Request
4. Review and discuss
5. Merge to main

#### Git Conventional Commits
- **Format**: `type(scope): description`
- **Types**: feat, fix, docs, style, refactor, test, chore
- **Example**: `feat(data): add ERA5 download function`
- **Tools**: commitizen for automation

---

## 🧪 Testing & Code Quality

### pytest
- **Homepage**: https://pytest.org/
- **Installation**: `pip install pytest`
- **Why pytest**: Simple, powerful, standard
- **Basic test**:
  ```python
  # test_calculations.py
  import pytest
  from my_module import calculate_dewpoint
  
  def test_dewpoint_positive():
      """Test dewpoint calculation with positive values"""
      result = calculate_dewpoint(temp=20, rh=50)
      assert abs(result - 9.3) < 0.1
  
  def test_dewpoint_invalid():
      """Test error handling for invalid input"""
      with pytest.raises(ValueError):
          calculate_dewpoint(temp=20, rh=150)
  
  # Run with: pytest test_calculations.py
  ```
- **Fixtures** (reusable test data):
  ```python
  @pytest.fixture
  def sample_dataset():
      """Create sample xarray dataset for testing"""
      return xr.Dataset({
          'temperature': (['time', 'lat', 'lon'], 
                         np.random.randn(10, 5, 5))
      })
  
  def test_mean_calculation(sample_dataset):
      result = calculate_mean(sample_dataset)
      assert result.dims == ('lat', 'lon')
  ```

### Code Quality Tools

#### Black (Formatter)
- **Install**: `pip install black`
- **Use**: `black my_code.py`
- **Configuration** (pyproject.toml):
  ```toml
  [tool.black]
  line-length = 88
  target-version = ['py39']
  ```

#### pylint/flake8 (Linters)
- **Install**: `pip install pylint flake8`
- **Use**: `pylint my_module.py`
- **VS Code integration**: Automatic

#### Type Hints
- **Since Python 3.5+**
- **Example**:
  ```python
  from typing import List, Dict, Optional
  import numpy as np
  import xarray as xr
  
  def process_temperature(
      data: xr.DataArray,
      threshold: float = 0.0,
      units: str = "celsius"
  ) -> xr.DataArray:
      """Process temperature data with threshold."""
      if units == "fahrenheit":
          data = (data - 32) * 5/9
      return data.where(data > threshold)
  ```

#### Pre-commit
- **Homepage**: https://pre-commit.com/
- **Purpose**: Run checks before commit
- **Configuration** (.pre-commit-config.yaml):
  ```yaml
  repos:
  - repo: https://github.com/psf/black
    rev: 23.1.0
    hooks:
    - id: black
  - repo: https://github.com/pycqa/flake8
    rev: 6.0.0
    hooks:
    - id: flake8
  ```

---

## 🌊 Domain-Specific Resources

### Meteorology/Atmospheric Sciences

#### MetPy
- **Docs**: https://unidata.github.io/MetPy/latest/
- **Calculations**: 400+ meteorological functions
- **Examples**:
  ```python
  import metpy.calc as mpcalc
  from metpy.units import units
  
  # Thermodynamics
  dewpoint = mpcalc.dewpoint_from_relative_humidity(
      temperature=20 * units.degC,
      relative_humidity=65 * units.percent
  )
  
  # Kinematics
  divergence = mpcalc.divergence(u_wind, v_wind)
  vorticity = mpcalc.vorticity(u_wind, v_wind)
  ```

#### cf-python
- **URL**: https://ncas-cms.github.io/cf-python/
- **Purpose**: CF conventions compliance
- **Features**: Regridding, aggregation, metadata

### Oceanography

#### GSW (Gibbs SeaWater)
- **URL**: https://teos-10.github.io/GSW-Python/
- **What**: TEOS-10 equation of state
- **Install**: `conda install -c conda-forge gsw`
- **Usage**:
  ```python
  import gsw
  
  # Practical salinity to absolute salinity
  SA = gsw.SA_from_SP(SP=35, p=0, lon=12, lat=55)
  
  # Conservative temperature
  CT = gsw.CT_from_t(SA=SA, t=10, p=0)
  
  # Density
  rho = gsw.rho(SA=SA, CT=CT, p=0)
  ```

#### xgcm
- **URL**: https://xgcm.readthedocs.io/
- **Purpose**: Analyze GCM output
- **Features**: Grid-aware operations

#### OceanSpy
- **URL**: https://oceanspy.readthedocs.io/
- **What**: Analysis of ocean model output
- **Features**: Budgets, water masses, sections

### Climate Science

#### xclim
- **URL**: https://xclim.readthedocs.io/
- **Purpose**: Climate indices calculation
- **Features**: ETCCDI indices, bias correction
- **Example**:
  ```python
  import xclim.indices as indices
  
  # Calculate growing degree days
  gdd = indices.growing_degree_days(
      tas=temperature,
      thresh='10 degC',
      freq='YS'
  )
  ```

#### climlab
- **URL**: https://climlab.readthedocs.io/
- **What**: Climate modeling toolkit
- **Use**: Energy balance models, radiative transfer

---

## 🚀 Quick Start Guides

### Day 1: Environment Setup
1. **Download Miniconda** from https://docs.conda.io/
2. **Install** (accept defaults, say yes to conda init)
3. **Create environment**:
   ```bash
   conda create -n dmi python=3.11
   conda activate dmi
   ```
4. **Install essentials**:
   ```bash
   conda install -c conda-forge \
     numpy pandas xarray matplotlib \
     cartopy jupyter netcdf4
   ```
5. **Install VS Code** from https://code.visualstudio.com/
6. **Install Python extension** in VS Code
7. **Test setup**:
   ```python
   import numpy as np
   import xarray as xr
   print("Success!")
   ```

### Week 1: Python Basics Checklist
- [ ] Complete Python.org tutorial chapters 1-5
- [ ] Write first Python script
- [ ] Understand: variables, lists, loops, functions
- [ ] Install and use Jupyter notebook
- [ ] Join Pytroll Slack
- [ ] Set up Git and GitHub account

### Month 1: Scientific Python Checklist
- [ ] NumPy basics: arrays, indexing, operations
- [ ] Pandas basics: DataFrames, reading CSV
- [ ] First plot with Matplotlib
- [ ] Load NetCDF file with xarray
- [ ] Create Git repository for learning
- [ ] Solve 10 exercises from Software Carpentry

### Project Ideas for Learning

#### Beginner Projects
1. **Temperature Converter**
   - GUI with tkinter
   - Handle multiple units
   - Add data validation

2. **Weather Station Data Analyzer**
   - Read CSV data
   - Calculate statistics
   - Plot time series

3. **NetCDF File Explorer**
   - Load file with xarray
   - Print metadata
   - Basic visualization

#### Intermediate Projects
1. **Automated Weather Report**
   - Download ECMWF data
   - Generate plots
   - Create PDF report

2. **Satellite Image Processor**
   - Use Satpy for RGB composites
   - Batch processing
   - Save georeferenced output

3. **Climate Index Calculator**
   - Calculate NAO index
   - Compare with observations
   - Statistical analysis

#### Advanced Projects
1. **Real-time Data Pipeline**
   - Scheduled downloads
   - Process with Dask
   - Update dashboard

2. **Forecast Verification System**
   - Compare forecasts to observations
   - Calculate skill scores
   - Generate reports

---

## 🚨 Common Pitfalls & Solutions

### Environment Issues

#### Problem: "Module not found"
**Solutions**:
- Check active environment: `conda info --envs`
- Install in correct env: `conda activate myenv`
- VS Code: Select correct interpreter (Ctrl+Shift+P)

#### Problem: Conda is slow
**Solutions**:
- Use mamba: `conda install mamba -n base -c conda-forge`
- Use libmamba solver: `conda config --set solver libmamba`
- Limit channels: Use conda-forge primarily

### Data Issues

#### Problem: Memory errors with large files
**Solutions**:
```python
# Use chunks
ds = xr.open_dataset('large_file.nc', chunks={'time': 10})

# Select before loading
ds_small = ds.sel(latitude=slice(50, 60), longitude=slice(10, 20))
data = ds_small.load()

# Use Dask
import dask.array as da
```

#### Problem: Slow data processing
**Solutions**:
- Vectorize with NumPy instead of loops
- Use numba for custom functions
- Process in parallel with Dask
- Profile code to find bottlenecks

### Coding Issues

#### Problem: "Works on my machine"
**Solutions**:
- Use environments consistently
- Pin package versions
- Share environment.yml files
- Use Docker for full reproducibility

#### Problem: Jupyter notebook chaos
**Solutions**:
- Clear outputs before committing
- Use meaningful cell structure
- Move complex logic to .py files
- Version control notebooks carefully

### Git Issues

#### Problem: Large files in Git
**Solutions**:
- Use .gitignore for data files
- Git LFS for necessary large files
- Store data separately (cloud/server)
- Only commit code and small configs

#### Problem: Merge conflicts
**Solutions**:
- Pull before starting work
- Work in feature branches
- Communicate with team
- Use Git GUI tools for complex merges

---

## 📋 Appendix: Useful Code Snippets

### Data Loading Templates

#### NetCDF with attributes
```python
import xarray as xr

# Load with CF conventions
ds = xr.open_dataset('data.nc', decode_cf=True)

# Load multiple files
ds = xr.open_mfdataset('data_*.nc', combine='by_coords')

# Load with Dask for large files
ds = xr.open_mfdataset('data_*.nc', chunks={'time': 10}, 
                       parallel=True)
```

#### GRIB files
```python
# Requires cfgrib
ds = xr.open_dataset('data.grib', engine='cfgrib')

# Multiple messages
ds = xr.open_datasets('data.grib', engine='cfgrib')
```

### Common Operations

#### Climatology calculation
```python
# Monthly climatology
clim = ds.groupby('time.month').mean('time')

# Anomalies
anom = ds.groupby('time.month') - clim

# Rolling mean
smooth = ds.rolling(time=30, center=True).mean()
```

#### Area averaging
```python
# Weight by latitude
weights = np.cos(np.deg2rad(ds.latitude))
ds_weighted = ds.weighted(weights)
mean = ds_weighted.mean(['longitude', 'latitude'])
```

#### Regridding
```python
import xesmf as xe

# Define target grid
ds_target = xr.Dataset({
    'lat': (['lat'], np.arange(-90, 91, 2.0)),
    'lon': (['lon'], np.arange(0, 360, 2.0))
})

# Create regridder
regridder = xe.Regridder(ds, ds_target, 'bilinear')

# Apply
ds_regrid = regridder(ds)
```

### Plotting Templates

#### Map with data
```python
import matplotlib.pyplot as plt
import cartopy.crs as ccrs
import cartopy.feature as cfeature

fig = plt.figure(figsize=(12, 8))
ax = plt.axes(projection=ccrs.PlateCarree())

# Plot data
im = ax.contourf(lons, lats, data, transform=ccrs.PlateCarree(),
                 cmap='RdBu_r', levels=20)

# Add features
ax.add_feature(cfeature.COASTLINE)
ax.add_feature(cfeature.BORDERS, alpha=0.5)

# Gridlines
gl = ax.gridlines(draw_labels=True, alpha=0.5)
gl.top_labels = gl.right_labels = False

# Colorbar
plt.colorbar(im, ax=ax, orientation='horizontal', 
             pad=0.05, shrink=0.8)

plt.title('Temperature Anomaly')
plt.show()
```

#### Time series with uncertainty
```python
fig, ax = plt.subplots(figsize=(10, 6))

# Plot mean
ax.plot(time, mean_values, 'b-', label='Mean')

# Add uncertainty
ax.fill_between(time, lower_bound, upper_bound, 
                alpha=0.3, color='blue')

# Formatting
ax.set_xlabel('Time')
ax.set_ylabel('Temperature (°C)')
ax.grid(True, alpha=0.3)
ax.legend()

# Date formatting
import matplotlib.dates as mdates
ax.xaxis.set_major_formatter(mdates.DateFormatter('%Y-%m'))
fig.autofmt_xdate()
```

---

## 🎯 Final Tips

1. **Start small**: Master basics before advanced topics
2. **Code daily**: 15 minutes > 0 minutes
3. **Read others' code**: Learn from open source
4. **Ask questions**: No question is too basic
5. **Share your work**: Help others learn
6. **Document everything**: Future you will thank you
7. **Version control always**: Even for small scripts
8. **Test your code**: Catch bugs early
9. **Refactor regularly**: Improve as you learn
10. **Have fun**: Build something you care about

---

*This guide is a living document. Contribute updates via DMI GitLab.*

*Last updated: January 2024*
*Maintained by: DMI Python Community*
*Version: 2.0*