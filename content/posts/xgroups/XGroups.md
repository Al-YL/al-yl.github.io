---
title: "Measuring the X-ray luminosities of DESI groups from eFEDS"
date: 2023-10-17T01:05:27+08:00
image: "/posts/xgroups/desierosita.png"
categories:
    - Galaxy Groups
tags:
    - Galaxy Groups
---

A galaxy group is a concentration of galaxies assumed to be embedded within an extended dark matter halo, providing cosmological probes of the spatial distribution and growth history of large-scale structure.

We use the eROSITA Final Equatorial-Depth Survey (**eFEDS**) to measure the rest-frame 0.1–2.4 keV band X-ray luminosities of ~ 600,000 DESI groups.

## DESI Group Catalog

The group catalog is taken from [Yang et al. (2021)](https://iopscience.iop.org/article/10.3847/1538-4357/abddb2), which extended the halo-based group finder developed by [Yang et al. (2005)](http://dx.doi.org/10.1111/j.1365-2966.2005.08560.x) and applied it to the DESI Legacy Imaging Surveys.

This group catalogue has been further updated based on the galaxy catalogue, which has been updated to DR9, containing five-band photometries ($g$, $r$, $z$, W1, W2), with a sky coverage of ∼ 100 million groups with ∼ 120 million galaxy members having ∼ 18200 deg$^2$.

The halo mass ($M_h$) of each group has been estimated based on abundance matching between the total group luminosity and ~ 600,000 DESI groups overlaid on eFEDS footprint.

![](/posts/xgroups/basicstat.png)

These groups span a large redshift range of $0.0 \le z_g \le 1.0$ and (group) halo mass of $10^{10.76}h^{-1}M_\odot \le M_h \le 10^{15.0}h^{-1}M_\odot$.


## The identification of Blind-detected X-ray Sources

[Brunner et al. (2021)](https://iopscience.iop.org/article/10.3847/1538-4357/abddb2), present catalogs of 27910 (main) and 4774 (supplementary) X-ray sources detected in the 0.2–2.3 keV band. [Salvato et al. (2021)](https://www.aanda.org/articles/aa/abs/2022/05/aa41631-21/aa41631-21.html) presented that ~ 10% blind-detected point sources (Extended Likelihood = 0) are more likely to be galactic sources.

Before measuring the count rates for each group, we cross-match the DESI groups with these blind-detected sources. We find 10932 blind-detected sources might emitted from the hot gas or AGN within groups and these sources are regarded as the X-ray center of the matched group.

![](/posts/xgroups/2906.png)

> The above figure shows an example eFEDS image (left-hand panel) for a blind-detected source (blue solid circle) overplotted with the probable DESI groups that might host it. The red solid circles show the regions within a distance of $R_{180}$ from the BGG of each candidate group. In this example, we regard the most massive one (group #2906) hosts that X-ray emission. The neighbour X-ray emission (blue-dashed circles) is also considered as part of the extended X-ray emission from the same group, while the others (grey-dashed circles) are regarded as contaminants. The red-dashed circle represents the region within a distance of $R_{180}$ but re-centred on that X-ray emission. The right-hand panel shows the corresponding DESI image. In both panels, the BGG and satellites of group #2906 are marked by magenta filled and green opened circles, respectively.

Most of the groups donot have blind-detected counterparts, their BGG are thus regarded as the X-ray center. By stacking the X-ray images of the groups that have no resolved X-ray centres, the BGG can well represent the X-ray peak of a group system, and the average surface brightness profiles roughly follow the β-model prediction.


## Calculate the Count Rate for each Group

We use two different algorithms to measure the luminosities in soft X-ray (rest-frame 0.1– 2.4 keV) band:

- **Mean Background Subtraction**: Calculating a background level averaged over the annulus of $1.5 - 2.0R_{180}$ of each group. The count rates are computed via subtracting the mean background level directly.
- **Patrol Background Subtraction**: Removing all of the regions enclosed by contaminants, masked pixels, and the aperture radius of DESI groups. The background level (patrol level) averaged over the remaining regions might potentially contributed by the instrument background, very distant sources, or small groups below the threshold. 

The count rates computed via subtracting the patrol level suffer the projection effect. First, we assume a tentative $L_{X} − M_{h}$ relation, then generate the mock image and calculate the fraction contributed by each group. we recompute the tentative $L_{X} − M_{h}$ relation and reproduce the process iteratively.

After deriving the count rates for each DESI group, we convert it into soft X-ray flux by dividing the source count rates to ECF. The details can be found [here](https://ui.adsabs.harvard.edu/abs/2023MNRAS.523.4909Z/abstract) and the derived catalog can be found [here](https://github.com/Al-YL/XLumsForDESIGroups/tree/main/DR9Y1_zbd).


## Merchandise related to this paper

![](/posts/xgroups/mug.jpg)

![](/posts/xgroups/tshirt.jpg)


Images in different wavebands have been created for variuos galaxy groups. You can download these images and print them on mugs or T-shirts.

![](/posts/xgroups/ima/158.png)

![](/posts/xgroups/ima/300.png)

![](/posts/xgroups/ima/442.png)

![](/posts/xgroups/ima/461.png)

![](/posts/xgroups/ima/545.png)

![](/posts/xgroups/ima/604.png)

![](/posts/xgroups/ima/829.png)

![](/posts/xgroups/ima/977.png)

![](/posts/xgroups/ima/1052.png)

![](/posts/xgroups/ima/1255.png)

![](/posts/xgroups/ima/1407.png)

![](/posts/xgroups/ima/1620.png)

![](/posts/xgroups/ima/1774.png)

![](/posts/xgroups/ima/1996.png)

![](/posts/xgroups/ima/2302.png)

![](/posts/xgroups/ima/2531.png)

![](/posts/xgroups/ima/2623.png)

![](/posts/xgroups/ima/2704.png)

![](/posts/xgroups/ima/2881.png)

![](/posts/xgroups/ima/2906.png)

![](/posts/xgroups/ima/3153.png)

![](/posts/xgroups/ima/3263.png)

