M87 image enhancement

This is a simple set of Python scripts for analyzing and enhancing astronomical images (FITS files). 
It includes code for checking image quality, reducing noise, and doing basic post-processing.

What’s in here:

• evaluate_image.py  
  - Calculates resolution (optical or radio-style)
  - Estimates local noise using RMS
  - Computes dynamic range in a selected region

• enhance_image.py  
  - Simulates gain calibration with amplitude and phase corrections
  - Includes a basic CLEAN-like algorithm for image deconvolution
  - Supports weighting methods for resolution vs sensitivity
  - Adds post-processing options like Gaussian and median filters

• imstat_tool.py  
  - A simple version of CASA’s imstat function
  - Gives useful statistics: mean, median, sigma, rms, min, max, etc.
  - Works for full image or a selected box region

This repository uses:

- numpy
- astropy
- scipy
