---
layout: post
title: Correlated Error Reduction in Data Assimilation - Utilizing AVISO Proxy for Future SWOT Observations
cover-img: /assets/img/Gulf_Stream_par_SWOT.JPG
thumbnail-img: /assets/img/Gulf_Stream_par_SWOT.JPG
tags: [swot]
---

The Surface Water and Ocean Topography (SWOT) satellite mission, launched in December 2022, will provide unprecedented high-resolution measurements of sea surface height (SSH) over the global oceans. However, the accuracy of SWOT data is limited by the presence of large spatially correlated errors, particularly in the cross-track direction, which can be difficult to remove through standard processing methods.

To address this challenge, researchers are exploring new methods to reduce SWOT-correlated errors and improve the accuracy of the SSH data. In this study, we focus on developing a Bayesian approach to solving for the correlated errors in SWOT data assimilation. Our goal is to show preliminary results that reduce the cross-track variations of SWOT correlated errors and demonstrate the potential for solving correlated SWOT errors as part of the assimilation process. We introduce the 1-stage approach, which consolidates the reduction of spatially correlated errors and the data assimilation into a single process, enabling an efficient retrieval of the Sea Surface Height field. Conversely, the 2-stage approach (metref et al. 2019) separates these tasks, first reducing the spatially correlated errors, followed by the data assimilation, necessitating more computational steps and potential loss of accuracy due to the segmented treatment.

We begin by introducing the SWOT satellite, which generates a 120-km-wide swath of SSH data with a 20-km gap at its center. The simulated SWOT errors include multiple terms such as timing error, roll error, and phase error, and are known to exhibit large spatially correlated errors. We demonstrate a simple case where the roll error is constant along the track but correlated in the cross-track direction. We also consider a baseline dilation error that is modeled as a quadratic term.

![Example figure showing SWOT versus AVISO](/assets/img/Gulf_Stream_par_SWOT.JPG)

Next, we compare the one-stage and two-stage approaches to solving the most probable solution of x with the Bayesian approach. The 1-stage approach performs more robustly than the 2-stage approach when estimating SSH signal and correlated errors. The 1-stage approach can estimate over 90% of the SSH signal, with a 7% decrease in the SSH estimation skill as the correlated error increases.  In contrast, in the 2-stage approach, SSH estimate skill drops from 91% to 35% as error increases. The 1-stage error estimate increases as the error increases, plateauing around 80%, and the 2-stage error estimate changes drastically from -214% to 35%. Our findings suggest that solving for the correlated errors within the assimilation framework can help mitigate the impact of measurement errors on SSH estimates, thereby improving the accuracy and reliability of assimilated SWOT products. Our results suggest that the one-stage approach provides a better result in terms of reducing correlated errors and extrapolation off-track. While there is still work to be done in refining the two-stage approach, our study highlights the potential of the Bayesian approach to solving SWOT's correlated errors and improving the accuracy of SSH data assimilation.

![Example figure showing SWOT versus AVISO](/assets/img/skill_ssh_errr_rmse_ratio.png)



Overall, this study contributes to the ongoing efforts to improve the accuracy of SWOT data and advance our understanding of the ocean's complex dynamics. With the launch of the SWOT satellite, we are poised to gain new insights into ocean circulation, sea level rise, and extreme weather events. The development of robust data assimilation methods will be critical to unlocking the full potential of this groundbreaking mission.

reference: 
Metref, S., Cosme, E., Le Sommer, J., Poel, N., Brankart, J.-M., Verron, J., & Gomez Navarro, L. (2019). Reduction of spatially structured errors in wide-swath altimetric satellite data using data assimilation. Remote Sensing, 11(11), 1336. https://doi.org/10.3390/rs11111336

