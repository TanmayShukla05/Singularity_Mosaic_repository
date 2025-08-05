# M87 Image Processing (CASA)

This project processes EHT 2017 `.uvfits` data of M87 to produce a final image using CASA.

---

## Steps:

1. **Import UVFITS**  
   Convert `.uvfits` to `.ms` using `importuvfits`.

2. **Fix MS**  
   Use `mstransform()` to clean each `.ms`.

3. **Combine Datasets**  
   Merge all `.ms` files into one with `concat()`.

4. **Visualize UV Coverage**  
   Plot using `plotms()` with time and channel averaging.

5. **Imaging**  
   Run `tclean()` to generate `M87_final_image.image`.

6. **Export**  
   Save as FITS using `exportfits()`.

---

## Notes:

- **Beam**: 20μas × 20μas  
- **Image size**: 512 × 512  
- **Cell size**: 0.25μas  
- **Weighting**: uniform  
- **Data**: Stokes I from 2017 EHT public release
