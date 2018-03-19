---
title: Evaluation Criterion
layout: post
order: 4
---

# Metrics
* Mean Absolute Error (**MAE**) and Pearson correlation coefficient (**PCC**) are used to assess the performance of the algorithms for estimation of areas, dimensions and regional wall thicknesses. For the 30 subjects in the test dataset, there are a total of 600 images. For any LV indices in {A1, A2, D1~D3, RWT1~RWT6}, the MAE and PCC can be computed as:

$$MAE_{ind}=\frac{\sum_{i=1}^{600}|x_{ind}(i)-y_{ind}(i)|}{600}$$

$$PCC_{ind}=\frac{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}][y_{ind}(i)-\bar{y}_{ind}]}{\sqrt{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}]^2\sum_{i=1}^{600}[y_{ind}(i)-\bar{y}_{ind}]^2}}$$

where $$ind\in \{A1,A2, D1~D3, RWT1~RWT6\}$$, $$x_{ind}$$ is the groud truth value and $$y_{ind}$$ is the estimated value, $\bar{x}_{ind}$ and $\bar{y}_{ind}$ are their mean values.

* Error Rate (ER) is used to assess the performance of the algorithms for cardiac phase identification. It can be computed as:
$$ER_{phase}=\frac{\sum_{i=1}^{600}\mathbf{1}(x_phase(i)\neq y_{phase}(i))}{600}$$
where $\mathbf{1}()$ is the indication function, $x_{phase}$ and $y_{phase}$ are the ground truth value and the estimated value of cardiac phase, respectively.

# Ranking
