---
layout: section
---

# Part 2.5: Domain-Specific Libraries
## Don't Reinvent the Wheel!

---

# 🎯 Find Your Domain's Tools First!

<div class="text-center mb-6">
<div class="text-3xl font-bold text-red-600">
⚠️ Critical Learning Principle ⚠️
</div>
<div class="text-xl mt-2">
Every scientific domain has specialized libraries that implement complex algorithms, data formats, and workflows.
<br><br>
<strong>Always research existing tools before writing your own!</strong>
</div>
</div>

<div class="grid grid-cols-2 gap-6 mt-8">
<div>


## ✅ Smart Approach

1. **Search** "[your domain] Python libraries"
2. **Check** domain-specific forums/communities
3. **Ask** colleagues what they use
4. **Review** published papers' code
5. **Explore** GitHub topics for your field

**Result:** Production-ready code in hours

</div>
</div>

---

# Domain Library Examples

<div class="grid grid-cols-3 gap-3 text-sm">
<div>

## 🌦️ Atmospheric Sciences
- **[MetPy](https://unidata.github.io/MetPy/)** - Meteorological calculations
- **[cfgrib](https://github.com/ecmwf/cfgrib)** - GRIB file handling
- **[atmopy](https://github.com/chrisroadmap/atmopy)** - Atmospheric physics
- **[pyrcel](https://github.com/darothen/pyrcel)** - Cloud parcel model
- **[climlab](https://climlab.readthedocs.io/)** - Climate modeling

</div>
<div>

## 🌊 Oceanography
- **[GSW](https://teos-10.github.io/GSW-Python/)** - Seawater thermodynamics
- **[xgcm](https://xgcm.readthedocs.io/)** - Grid operations
- **[pyTMD](https://pytmd.readthedocs.io/)** - Tidal analysis
- **[mixsea](https://mixsea.readthedocs.io/)** - Ocean mixing
- **[oceanspy](https://oceanspy.readthedocs.io/)** - Ocean model data
- **[argopy](https://argopy.readthedocs.io/)** - Argo float data

</div>
<div>

## 🛰️ Remote Sensing
- **[Satpy](https://satpy.readthedocs.io/)** - Satellite data processing
- **[pyresample](https://pyresample.readthedocs.io/)** - Resampling geospatial
- **[trollimage](https://trollimage.readthedocs.io/)** - Image enhancement
- **[rasterio](https://rasterio.readthedocs.io/)** - Geospatial rasters
- **[sentinelsat](https://sentinelsat.readthedocs.io/)** - Sentinel data access
- **[eo-learn](https://eo-learn.readthedocs.io/)** - Earth observation ML

</div>
</div>

<div class="grid grid-cols-3 gap-3 text-sm mt-4">
<div>

## 🌍 Geosciences
- **[ObsPy](https://www.obspy.org/)** - Seismology toolkit
- **[PyGMT](https://www.pygmt.org/)** - Geospatial plotting
- **[Verde](https://www.fatiando.org/verde/)** - Spatial data processing
- **[GemPy](https://www.gempy.org/)** - 3D geological modeling
- **[Landlab](https://landlab.readthedocs.io/)** - Earth surface dynamics

</div>
<div>

## 🧮 Statistics/ML
- **[statsmodels](https://www.statsmodels.org/)** - Statistical modeling
- **[scikit-learn](https://scikit-learn.org/)** - Machine learning
- **[xskillscore](https://xskillscore.readthedocs.io/)** - Forecast verification
- **[properscoring](https://github.com/properscoring/properscoring)** - Probabilistic scores
- **[climpred](https://climpred.readthedocs.io/)** - Climate predictions

</div>
<div>

## 🗺️ Geospatial
- **[Cartopy](https://scitools.org.uk/cartopy/)** - Map projections
- **[Shapely](https://shapely.readthedocs.io/)** - Geometric operations
- **[GeoPandas](https://geopandas.org/)** - Geospatial data
- **[Folium](https://python-visualization.github.io/folium/)** - Interactive maps
- **[pyproj](https://pyproj4.github.io/pyproj/)** - Coordinate transforms

</div>
</div>

---

# How to Find Libraries for YOUR Domain

<div class="grid grid-cols-2 gap-6">
<div>

## 🔍 Search Strategies

1. **GitHub Topics**
   - Go to: `github.com/topics/[your-domain]-python`
   - Example: [`/topics/oceanography-python`](https://github.com/topics/oceanography-python)

2. **Awesome Lists**
   - Search: "Awesome [your domain]"
   - [Awesome Earth Science](https://github.com/scottyhq/awesome-earth-science-computing)
   - [Awesome GIS](https://github.com/sshuair/awesome-gis)

3. **Paper Citations**
   - Check Methods sections
   - Look for "Data Availability"
   - Follow GitHub links

4. **Package Indexes**
   - [PyPI search](https://pypi.org/search/)
   - [Conda-forge](https://conda-forge.org/feedstock-outputs/)
   - [Papers with Code](https://paperswithcode.com/)

</div>
<div>

## 📋 Evaluation Checklist

Before choosing a library, check:

- [ ] **Active development?** (recent commits)
- [ ] **Good documentation?**
- [ ] **Community support?** (answered issues)
- [ ] **Installation ease?** (conda/pip available)
- [ ] **Test coverage?**
- [ ] **Citation/paper?** (for research)
- [ ] **Compatible licenses?**

**Red flags:**
- Last update > 2 years ago
- No documentation
- Many open issues
- Complex dependencies
- No examples

**Green flags:**
- Regular releases
- Active community
- Clear examples
- Good test coverage

</div>
</div>

---

# Real Example: Finding Ocean Tools

<div class="text-center mb-4">

## 🌊 "I need to calculate ocean mixed layer depth"

</div>

<div class="grid grid-cols-3 gap-4">
<div>

### ❌ Wrong Way
```python
# 200 lines of custom code
def calculate_mld(temp, depth):
    # Complex algorithm
    # Probably has bugs
    # Not validated
    # ...
```
**Time:** Weeks of development

</div>
<div>

### ✅ Right Way
```python
# Step 1: Search
# "ocean mixed layer depth python"

# Step 2: Find mixsea
pip install mixsea

# Step 3: Use it!
import mixsea as mx
mld = mx.mld.densitythreshold(
    depth, temp, dens
)
```
**Time:** 30 minutes

</div>
<div>

### 🎯 Even Better
```python
# Check multiple options:
# - mixsea
# - oceanspy  
# - xarrayMLD
# - GSW

# Compare features
# Read papers
# Choose best fit
```
**Bonus:** Learn from their code!

</div>
</div>

<div class="mt-6 text-center bg-blue-100 p-4 rounded">

💡 **The library probably implements the exact algorithm from the paper you're reading!**

</div>

---

# Building Your Domain Toolkit

<div class="grid grid-cols-2 gap-6">
<div>

## 📚 Start Your Library Collection

Create a `requirements.txt` for your domain:

```txt
# Core scientific stack
numpy>=1.24
pandas>=2.0
xarray>=2023.0

# Domain-specific (example: ocean)
gsw>=3.6          # TEOS-10 equations
xgcm>=0.8         # Grid operations  
argopy>=0.1       # Argo data
mixsea>=0.1       # Mixing analysis
cmocean>=3.0      # Colormaps

# Visualization
matplotlib>=3.7
cartopy>=0.22
```

Keep this updated and share with colleagues!

</div>
<div>

## 🎯 Learning Strategy

**Week 1-2:** Master the basics (NumPy, Pandas)

**Week 3-4:** Learn your domain's main library
- Read the docs thoroughly
- Run all examples
- Understand the API design

**Week 5+:** Add specialized tools as needed
- One library at a time
- Read the source code
- Contribute back!

**Pro tip:** Many domain libraries have excellent tutorials that teach both the library AND the science!

</div>
</div>

---

# Community Knowledge: Your Best Resource

<div class="grid grid-cols-3 gap-4 text-sm">
<div>

## 💬 Where to Ask

**Domain Forums:**
- [Pangeo Discourse](https://discourse.pangeo.io/)
- [ECMWF Support](https://confluence.ecmwf.int/)
- [Stack Overflow](https://stackoverflow.com/) + domain tags

**Slack/Discord:**
- Pytroll (satellite)
- Pangeo (geoscience)
- ESMValTool (climate)

</div>
<div>

## 🗣️ How to Ask

"I'm working on [specific problem] in [domain]. Are there existing Python libraries for this?"

**Good example:**
"I need to calculate significant wave height from wave spectra. What Python libraries do oceanographers use for wave analysis?"

**Include:**
- Specific task
- Data format
- Performance needs

</div>
<div>

## 🤝 Give Back

When you find great libraries:
- ⭐ Star on GitHub
- 📝 Write tutorials
- 🐛 Report issues
- 📖 Improve docs
- 💰 Support developers

**Your future self will thank you!**

</div>
</div>

<div class="mt-6 text-center text-2xl font-bold bg-yellow-100 p-4 rounded">

🚀 Remember: Every hour spent finding the right library saves weeks of development!

</div>