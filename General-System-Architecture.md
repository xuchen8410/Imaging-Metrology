**Optical Aberrations Summary Table：**
| Aberration                            | Type          | Physical Cause                                         | Field Location | Wavefront Aberration Term        | Typical Image Effect                                | Key System Factors                         | Common Correction                            |
| ------------------------------------- | ------------- | ------------------------------------------------------ | -------------- | -------------------------------- | --------------------------------------------------- | ------------------------------------------ | -------------------------------------------- |
| **Spherical Aberration**              | Monochromatic | Marginal rays focus differently than paraxial rays     | On-axis        | W040 * rho^4                     | Circular blur spot                                  | aperture size, surface curvature, f-number | aspheric surface, aperture stop optimization |
| **Coma**                              | Monochromatic | Different pupil zones produce different magnifications | Off-axis       | W131 * rho^3 * h * cos(theta)    | Comet-shaped blur                                   | field angle, aperture size, stop location  | symmetric design, stop placement             |
| **Astigmatism**                       | Monochromatic | Tangential and sagittal rays focus at different planes | Off-axis       | W222 * rho^2 * h^2 * cos(2theta) | Line or elliptical blur                             | field height, lens symmetry                | balanced lens groups                         |
| **Field Curvature**                   | Monochromatic | Petzval sum causes curved image surface                | Off-axis       | W220 * rho^2 * h^2               | Image best focus lies on curved surface             | optical power distribution                 | field flattener                              |
| **Distortion**                        | Monochromatic | Magnification varies across field                      | Off-axis       | W311 * rho * h^3 * cos(theta)    | Barrel or pincushion distortion                     | field angle, principal ray geometry        | lens group redistribution                    |
| **Longitudinal Chromatic Aberration** | Chromatic     | Refractive index varies with wavelength                | On-axis        | focal length = f(lambda)         | Different colors focus at different axial locations | glass dispersion, wavelength band          | achromatic doublet                           |
| **Lateral Chromatic Aberration**      | Chromatic     | Magnification varies with wavelength                   | Off-axis       | magnification = m(lambda)        | Color fringing at edges                             | field height, glass dispersion             | apochromatic design                          |

####
**像差与光学参数关系**
| 参数                             | 主要影响像差                      |
| ------------------------------ | --------------------------- |
| **Aperture / f-number**        | spherical aberration、coma   |
| **Field of View**              | coma、astigmatism、distortion |
| **Optical power distribution** | field curvature             |
| **Stop location**              | coma、distortion             |
| **Wavelength band**            | chromatic aberrations       |
| **Principal plane location**   | distortion、field curvature  |
| **Lens symmetry**              | coma、distortion             |


####
**主点-** The cardinal points of an optical system include two focal points, two principal points, and two nodal points. These six points describe the first-order imaging properties of a system.
#####
**主平面-** Principal planes are reference planes in an optical system where refraction is assumed to occur in the equivalent thin-lens model.
When the refractive indices of object space and image space are the same, the nodal points coincide with the principal points.
####
**设计实例-**
Telephoto lens 的 principal plane 在镜头外面，复杂镜组改变了H' location。导致 EFL >> physical length

