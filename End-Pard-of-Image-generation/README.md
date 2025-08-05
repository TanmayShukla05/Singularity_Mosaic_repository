# Uncertainity Analysis

# M87 Bayesian Uncertainty Quantification (GPU Accelerated)

This project performs Bayesian uncertainty quantification using MCMC sampling for the M87 interferometric image. It uses visibility data from UVFITS files and reconstructs an image using probabilistic inference, accelerated on GPU with CuPy.

## 🚀 Features

- GPU-accelerated image reconstruction using CuPy
- MCMC sampling using Metropolis-Hastings
- Posterior mean, standard deviation, confidence intervals
- Batch-wise visibility handling for large data
- Visualization of uncertainty and signal-to-noise ratio

## 📁 Files Used

- **M87_final_image.fits** — Target FITS image for comparison  
- **M87_combined_distinct.uvfits** — UV visibility data

## 🧠 Main Components

### `main()`
1. **Load FITS and UVFITS data**
2. **Estimate noise from visibilities**
3. **Initialize image**
4. **Run Metropolis-Hastings MCMC sampling**
5. **Compute image statistics (mean, std, CI)**
6. **Save output FITS files**
7. **Visualize posterior mean, uncertainty, CI width, SNR**
8. **Compute MSE vs original image**

### Output Files:
- `M87_MCMC_mean_fixed.fits`
- `M87_MCMC_uncertainty_fixed.fits`
- `M87_MCMC_lower_ci_fixed.fits`
- `M87_MCMC_upper_ci_fixed.fits`
- `M87_MCMC_uncertainty_fixed.png`

## 📦 Requirements

- Python 3.7+
- CuPy
- NumPy
- Matplotlib
- Astropy
- SciPy

You can install the dependencies with:

```bash
pip install numpy matplotlib astropy scipy cupy
