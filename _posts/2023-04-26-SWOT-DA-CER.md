---
layout: post
title: SWOT Data Assimilation with Correlated Error Reduction
cover-img: /assets/img/Gulf_Stream_par_SWOT.JPG
thumbnail-img: /assets/img/Gulf_Stream_par_SWOT.png
tags: [swot]
---

The Surface Water and Ocean Topography (SWOT) satellite mission, set to launch in late 2022, will provide unprecedented high-resolution measurements of sea surface height (SSH) over the global oceans. However, the accuracy of SWOT data is limited by the presence of large spatially correlated errors, particularly in the cross-track direction, which can be difficult to remove through standard processing methods.



To address this challenge, researchers are exploring new methods to reduce SWOT's correlated errors and improve the accuracy of the SSH data. In this study, we focus on developing a Bayesian approach to solving for the correlated errors in SWOT data assimilation. Our goal is to show preliminary results that reduce the cross-track variations of SWOT correlated errors and demonstrate the potential for solving correlated SWOT errors as part of the assimilation process.

We begin by introducing the SWOT satellite, which generates a 120-km-wide swath of SSH data with a 20-km gap at its center. The simulated SWOT errors include multiple terms such as timing error, roll error, and phase error, and are known to exhibit large spatially correlated errors. We demonstrate a simple case where the roll error is constant along the track but correlated in the cross-track direction. We also consider a baseline dilation error that is modeled as a quadratic term.

![Example figure showing SWOT versus AVISO](/assets/img/Gulf_Stream_par_SWOT.JPG)

Next, we compare the one-step and two-step approaches to solving for the most probable solution of x with Bayesian approach. With the one-step approach, solving correlated error as part of the assimilation, correlated errors are almost entirely removed, and large-scale SSH signals are also removed. However, for the two-step approach, the off-track extrapolation is very bad, and the residual variance is over 86%.

Our results suggest that the one-step approach provides a better result in terms of reducing correlated errors and extrapolation off-track. While there is still work to be done in refining the two-step approach, our study highlights the potential of Bayesian approach to solving SWOT's correlated errors and improving the accuracy of SSH data assimilation.

Overall, this study contributes to the ongoing efforts to improve the accuracy of SWOT data and advance our understanding of the ocean's complex dynamics. With the launch of the SWOT satellite, we are poised to gain new insights into ocean circulation, sea level rise, and extreme weather events. The development of robust data assimilation methods will be critical to unlocking the full potential of this groundbreaking mission.



