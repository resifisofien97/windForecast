<div align="center">

# A Novel Deep Learning Approach for Regional High-Resolution Spatio-Temporal Wind Speed Forecasting for Energy Applications

<div>
  <a href="https://scholar.google.com/citations?user=fzG5VxsAAAAJ&hl=en">Sofien Resifi</a><sup>1</sup>&nbsp;&nbsp;
  <a href="https://scholar.google.com/citations?user=r4wrjtsAAAAJ&hl=en">Elissar Al Aawar</a><sup>1</sup>&nbsp;&nbsp;
  <a href="https://scholar.google.com/citations?user=VrQC0_gAAAAJ&hl=en">Hari Parsad Darsari</a><sup>1</sup>&nbsp;&nbsp;
  <a href="https://scholar.google.com/citations?user=KuvOKcwAAAAJ&hl=en">Hatem Jebri</a><sup>1</sup>&nbsp;&nbsp;
  <a href="https://scholar.google.com/citations?user=Ez_xk3sAAAAJ&hl=en">Ibrahim Hoteit</a><sup>1</sup>&nbsp;&nbsp;
  <br>
  <sup>1</sup> KAUST,
</div>

---

![Wind Speed Forecasts](wind.gif)

</div>
   
## 📜 Abstract
Accurate spatio-temporal wind speed forecasting is crucial for optimizing wind energy production. Traditional forecasting relies on numerical weather prediction (NWP) models, which are computationally intensive, especially when implemented on large high-resolution grids. Recently, Deep Learning (DL) has emerged as an efficient alternative, utilizing historical data to learn patterns and predict future conditions. This work develops a regional DL-based forecasting system that reduces the computational burden of physical models, by using a long-term reanalysis dataset for the Arabian Peninsula (AP). The system forecasts hourly wind speed at 5~km spatial resolution up to 48 hours ahead. We focus on vertical levels, corresponding to the hub heights of wind turbines for energy production. We explore two approaches: recursive forecasting, which advances the system's state at a fine scale over time, and downscaling, which refines coarse-resolution forecasts into high-resolution counterparts. Furthermore, we propose merging both approaches by combining the propagation of spatio-temporal dynamics at fine-scale with coarse-scale predictions. The performance of the frameworks was evaluated qualitatively and quantitatively. Results show that the recursive approach accumulates errors over time steps, whereas the downscaling approach effectively generates high-resolution forecasts. Combining both approaches resulted in a more robust framework, demonstrating notably improved performance and stabilized error evolution.

## 🚀 Getting Started