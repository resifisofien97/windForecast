<div align="center">

# A Novel Deep Learning Approach for Regional High-Resolution Spatio-Temporal Wind Speed Forecasting for Energy Applications

<div>
  <a>Sofien Resifi</a><sup>1</sup>&nbsp;&nbsp;
  <a>Elissar Al Aawar</a><sup>1</sup>&nbsp;&nbsp;
  <a>Hari Parsad Darsari</a><sup>1</sup>&nbsp;&nbsp;
  <a>Hatem Jebri</a><sup>1</sup>&nbsp;&nbsp;
  <a>Ibrahim Hoteit</a><sup>1</sup>&nbsp;&nbsp;
  <br>
  <sup>1</sup> KAUST,
</div>

---

![Wind Speed Forecasts](simulations/wind.gif)

</div>
   
## 📜 Abstract
Accurate spatio-temporal wind speed forecasting is crucial for optimizing wind energy production. Traditional forecasting relies on numerical weather prediction (NWP) models, which are computationally intensive, especially when implemented on large high-resolution grids. Recently, Deep Learning (DL) has emerged as an efficient alternative, utilizing historical data to learn patterns and predict future conditions. This work develops a regional DL-based forecasting system that reduces the computational burden of physical models, by using a long-term reanalysis dataset for the Arabian Peninsula (AP). The system forecasts hourly wind speed at 5~km spatial resolution up to 48 hours ahead. We focus on vertical levels, corresponding to the hub heights of wind turbines for energy production. We explore two approaches: recursive forecasting, which advances the system's state at a fine scale over time, and downscaling, which refines coarse-resolution forecasts into high-resolution counterparts. Furthermore, we propose merging both approaches by combining the propagation of spatio-temporal dynamics at fine-scale with coarse-scale predictions. The performance of the frameworks was evaluated qualitatively and quantitatively. Results show that the recursive approach accumulates errors over time steps, whereas the downscaling approach effectively generates high-resolution forecasts. Combining both approaches resulted in a more robust framework, demonstrating notably improved performance and stabilized error evolution.

## 🚀 Getting Started


### Environment Setup
First, let's set up the Conda environment to get you up and running. For simplicity, the conda environment is provided in the repo. Simply create a new environment using the provide YAML file.

```bash
conda env create -f wind.yml
```

## Network Architectures

### Recursive Forecasting 
<div>
<img src="/figures/genvit.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->

<img src="/figures/multistepfinis.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->

</div>
### Downscaling

<img src="./figures/swinlastmdown.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->


<img src="./figures/swinlstmsturc.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->

### Combined Approach

<img src="./figures/doubleenc.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->


<img src="./figures/multistepimproved.pdf" alt="Graphical Abstract" width="500"> <!-- Sets the width to 500 pixels -->



## 📦 Trained Models
All Weight files for the trained models will be available