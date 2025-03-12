<div align="center">
Note: Code will be made available upon acceptance of the manuscript
</div>

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
Accurate spatio-temporal wind speed forecasting is crucial for optimizing wind energy production. Traditional forecasting relies on numerical weather prediction (NWP) models, which are computationally intensive, especially when implemented on large high-resolution grids. Recently, Deep Learning (DL) has emerged as an efficient alternative, utilizing historical data to learn patterns and predict future conditions. This work develops a regional DL-based forecasting system that reduces the computational burden of physical models, by using a long-term reanalysis dataset for the Arabian Peninsula (AP). The system forecasts hourly wind speed at 5 km spatial resolution up to 48 hours ahead. We focus on vertical levels, corresponding to the hub heights of wind turbines for energy production. We explore two approaches: recursive forecasting, which advances the system's state at a fine scale over time, and downscaling, which refines coarse-resolution forecasts into high-resolution counterparts. Furthermore, we propose merging both approaches by combining the propagation of spatio-temporal dynamics at fine-scale with coarse-scale predictions. The performance of the frameworks was evaluated qualitatively and quantitatively. Results show that the recursive approach accumulates errors over time steps, whereas the downscaling approach effectively generates high-resolution forecasts. Combining both approaches resulted in a more robust framework, demonstrating notably improved performance and stabilized error evolution.

## 🚀 Getting Started


### Environment Setup
First, let's set up the Conda environment to get you up and running. For simplicity, the conda environment is provided in the repo. Simply create a new environment using the provide YAML file.

```bash
conda env create -f wind.yml
```

## Network Architectures
The networks' architectures are based on Vision Transformers(ViTs)

### Recursive Forecasting 

<img src="/figures/genvit.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

<img src="/figures/multistepfinis.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

### Downscaling

<img src="./figures/swinlastmdown.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

<img src="./figures/swinlstmsturc.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

### Combined Approach

<img src="./figures/doubleenc.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

<img src="./figures/multistepimproved.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

## Summary of the Results

<img src="./figures/Nmae.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->

<img src="./figures/mae.png" alt="Graphical Abstract" width="700"> <!-- Sets the width to 500 pixels -->



## 📦 Trained Models
All Weight files for the trained models will be available 


- Recursive Forecasting:  
  - Lead1:➡️ [Download](https://drive.google.com/file/d/1Ovj02T4Ra-D-5Yb5Yg861HabN0JONKT1/view?usp=sharing)
  - Lead3:➡️ [Download](https://drive.google.com/file/d/148E0IpXsy5saqxv3V6l-GSVII6gMJRLB/view?usp=sharing)
  - Lead6:➡️ [Download](https://drive.google.com/file/d/1i4CBiwa0qUgISuSa9nfLmLTqDYyRFCyA/view?usp=sharing)
- Downscaling
  - D = 8:➡️ [Download](https://drive.google.com/file/d/1cEgoJRR0QULK9zu131_PG32Owgjyl55B/view?usp=sharing)
  - D = 16:➡️ [Download](https://drive.google.com/file/d/1o0SBoY0loBEeSB64Gi4RB2y8OzdarBt5/view?usp=sharing)
- Combined Approach
  - Lead1
  ---D = 8 ➡️ [Download](https://drive.google.com/file/d/1be2GWVZjEzHf70UVklvk8qUvrYedzq9V/view?usp=sharing)
  ---D = 16 ➡️ [Download](https://drive.google.com/file/d/1c8jN35jG6pFn_aMUcDSB06f965SI0Od7/view?usp=sharing)
  - Lead3
  ---D = 8 ➡️ [Download](https://drive.google.com/file/d/10hDf69330kTDh8KTf06pOKazjbaK8f2_/view?usp=sharing)
  ---D = 16 ➡️ [Download](https://drive.google.com/file/d/1K3ZgcoyHEziUgKPLZWW4XlhU_RLHJmNx/view?usp=sharing)
  - Lead6
  ---D = 8 ➡️ [Download](https://drive.google.com/drive/folders/1Lq_1MXG8BL-diuD9NNijLscBYmtebr5v?usp=sharing)
  ---D = 16 ➡️ [Download](https://drive.google.com/file/d/18PA0pVh2OK0KePVhxUiIoHbo71rIs2KA/view?usp=sharing)

The weight directory is organized as follows:
```
weights
│   
└───recursive
│   └─── lead1
|   |   
│   └─── lead3
|   |  
│   └─── lead6
|   |   
└───down
│   │   D8
│   │   D16
│   |
└───combined
│   └─── lead1
|   |    |   D8
|   |    |   D16
│   └─── lead3
|   |    |   D8
|   |    |   D16
│   └─── lead6
|   |    |   D8
|   |    |   D16
```



The data directory is organized as follows:
```
data
│  u.hdf5
|  v.hdf5
|  prs.hdf5
|  rho.hdf5
|  t.hdf5
|  topo.hdf5
```



The statistics directory is organized as follows:
```
statistics
| compute_stat.py
| submitstat.sh
| submitstatall.sh
└───stat
│   | u50m.npy,u80m.npy,u100m.npy,u120m.npy
|   | v50m.npy,v80m.npy,v100m.npy,v120m.npy
|   | prs50m.npy,prs80m.npy,prs100m.npy,prs120m.npy
|   | rho50m.npy,rho80m.npy,rho100m.npy,rho120m.npy
|   | t50m.npy,t80m.npy,t100m.npy,t120m.npy
```


## 📖 Citation
If you find WindForecast useful in your research, please consider citing:

```bibtex
@article{resifi5079080novel,
  title={A Novel Deep Learning Approach for Regional High-Resolution Spatio-Temporal Wind Speed Forecasting for Energy Applications},
  author={Resifi, Sofien and Al Aawar, Elissar and Hari Prasad, Dasari and Jebari, Hatem and Hoteit, Ibrahim},
  journal={Available at SSRN 5079080}
}
```

