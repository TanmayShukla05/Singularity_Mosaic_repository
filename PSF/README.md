# CASA PSF Generator

This is a simple CASA-based Python script to generate **Point Spread Functions (PSFs)** for different Briggs weighting settings.  
It helps visualize how **robust parameter tuning** affects resolution and sensitivity during radio image reconstruction.

What’s in here:

- `psf_generator.py`
  - Uses `tclean()` with `niter=0` to produce PSF images only
  - Applies **Briggs weighting** with three `robust` values:
    - `+2` (Natural-like): most sensitive, large beam
    - `0` (Balanced): trade-off between resolution and sensitivity
    - `−2` (Uniform-like): sharpest resolution, less sensitive
  - Outputs three separate images for visual comparison

---

## How to Use

1. Open CASA (Common Astronomy Software Applications)
2. Replace `'your_data.ms'` in the script with your actual `.ms` dataset
3. Run the script
4. Check the generated images:
   - `psf_robust_plus2`
   - `psf_robust_0`
   - `psf_robust_minus2`

---

## This repository uses:

- **CASA** (v5 or v6)
- A valid `.ms` (Measurement Set) as input

---

## Notes

- `niter=0` ensures only the **dirty PSF** is computed, with no deconvolution
- Helps in understanding how **weighting affects beam shape** before full CLEAN

---