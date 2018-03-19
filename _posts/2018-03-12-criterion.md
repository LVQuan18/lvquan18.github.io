---
title: Evaluation Criterion
layout: post
order: 4
---

# Metrics
* Mean Absolute Error (**MAE**) and Pearson correlation coefficient (**PCC**) are used to assess the performance of the algorithms for estimation of areas, dimensions and regional wall thicknesses. For the 30 subjects in the test dataset, there are a total of 600 images. For any LV indices in {A1, A2, D1~D3, RWT1~RWT6}, the MAE and PCC can be computed as:
$$MAE_{ind}=\frac{\sum_{i=1}^{600}|x_{ind}(i)-y_{ind}(i)|}{600}$$
<br/>
$${\scriptstyle PCC_{ind}=\frac{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}][y_{ind}(i)-\bar{y}_{ind}]}{\sqrt{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}]^2\sum_{i=1}^{600}[y_{ind}(i)-\bar{y}_{ind}]^2}}}$$
<br/>where $$ind\in \{A1,A2, D1~D3, RWT1~RWT6\}$$, $$x_{ind}$$ is the groud truth value and $$y_{ind}$$ is the estimated value, $$\bar{x}_{ind}$$ and $$\bar{y}_{ind}$$ are their mean values.

* Error Rate (ER) is used to assess the performance of the algorithms for cardiac phase identification. It can be computed as:
$$ER_{phase}=\frac{\sum_{i=1}^{600}\mathbf{1}(x_{phase}(i)\neq y_{phase}(i))}{600}$$
<br/>
where $$\mathbf{1}()$$ is the indication function, $$x_{phase}$$ and $$y_{phase}$$ are the ground truth value and the estimated value of cardiac phase, respectively.

# Ranking
MAE and ER are used for the final ranking of all participants.

0. Initialization: <br/> For each participant, compute $$MAE_{ind}$$ for $$ind\in \{A1,A2, D1~D3, RWT1~RWT6\}$$ and $$ER_{phase}$$.
1. Compute the mean MAE values for areas, dimensions, and regional wall thicknesses, and obtain $$MAE_{area}$$, $$MAE{dim}$$, $$MAE{rwt}$$.
2. Build four ranking lists ($$R_{area}$$, $$R_{dim}$$, $$R_{rwt}$$, $$R_{phase}$$) of all participants according to $$MAE_{area}$$, $$MAE{dim}$$, $$MAE{rwt}$$ and $$ER_{phase}$$ in ascending order, respectively. Statistical test is conducted for areas, dimensions, and regional wall thicknesses to test the significance of difference between two participants. If no significance exists, the two participants will have the same rank in the list.
3. The final ranking list RALL is computed by sorting the summation of the four ranking lists above in ascending order.