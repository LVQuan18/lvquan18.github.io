---
title: Evaluation Criterion
layout: post
order: 4
---

# Metrics
Mean Absolute Error (**MAE**) and Pearson correlation coefficient (**PCC**) are used to assess the performance of the algorithms for estimation of areas, dimensions and regional wall thicknesses. For the 30 subjects in the test dataset, there are a total of 600 images. For any LV indices in {A1, A2, D1~D3, RWT1~RWT6}, the MAE and PCC can be computed as:


$$MAE_{ind}=\frac{\Sum_{i=1}^{600}|x_{ind}(i)-y_{ind}(i)|}{600}$$
$$PCC_{ind}=\frac{\Sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}][y_{ind}(i)-\bar{y}_{ind}]}{\sqrt{\Sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}]^2\Sum_{i=1}^{600}[y_{ind}(i)-\bar{y}_{ind}]^2}}$$
