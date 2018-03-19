---
title: Evaluation Criterion
layout: post
order: 4
---

# Metrics
* Mean Absolute Error (**MAE**) and Pearson correlation coefficient (**PCC**) are used to assess the performance of the algorithms for estimation of areas, dimensions and regional wall thicknesses. For the 30 subjects in the test dataset, there are a total of 600 images. For any LV indices in {A1, A2, D1~D3, RWT1~RWT6}, the MAE and PCC can be computed as:
$${\scriptstyle MAE_{ind}=\frac{\sum_{i=1}^{600}|x_{ind}(i)-y_{ind}(i)|}{600}}$$
<br/>
$${\scriptstyle PCC_{ind}=\frac{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}][y_{ind}(i)-\bar{y}_{ind}]}{\sqrt{\sum_{i=1}^{600}[x_{ind}(i)-\bar{x}_{ind}]^2\sum_{i=1}^{600}[y_{ind}(i)-\bar{y}_{ind}]^2}}}$$
<br/>where $${\scriptstyle ind\in \{A1,A2, D1~D3, RWT1~RWT6\}}$$, $${\scriptstyle x_{ind}}$$ is the groud truth value and $${\scriptstyle y_{ind}}$$ is the estimated value, $${\scriptstyle \bar{x}_{ind}}$$ and $${\scriptstyle \bar{y}_{ind}}$$ are their mean values.

* Error Rate (ER) is used to assess the performance of the algorithms for cardiac phase identification. It can be computed as:
$${\scriptstyle ER_{phase}=\frac{\sum_{i=1}^{600}\mathbf{1}(x_{phase}(i)\neq y_{phase}(i))}{600}}$$
<br/>
where $${\scriptstyle \mathbf{1}()}$$ is the indication function, $${\scriptstyle x_{phase}}$$ and $${\scriptstyle y_{phase}}$$ are the ground truth value and the estimated value of cardiac phase, respectively.

# Ranking
MAE and ER are used for the final ranking of all participants.

0. Initialization: <br/> For each participant, compute $${\scriptstyle MAE_{ind}}$$ for $${\scriptstyle ind\in \{A1,A2, D1~D3, RWT1~RWT6\}}$$ and $${\scriptstyle ER_{phase}}$$.
1. Compute the mean MAE values for areas, dimensions, and regional wall thicknesses, and obtain $${\scriptstyle MAE_{area}}$$, $${\scriptstyle MAE{dim}}$$, $${\scriptstyle MAE{rwt}}$$.
2. Build four ranking lists ($${\scriptstyle R_{area}}$$, $${\scriptstyle R_{dim}}$$, $${\scriptstyle R_{rwt}}$$, $${\scriptstyle R_{phase}}$$) of all participants according to $${\scriptstyle MAE_{area}}$$, $${\scriptstyle MAE{dim}}$$, $${\scriptstyle MAE{rwt}}$$ and $${\scriptstyle ER_{phase}}$$ in ascending order, respectively. Statistical test is conducted for areas, dimensions, and regional wall thicknesses to test the significance of difference between two participants. If no significance exists, the two participants will have the same rank in the list.
3. The final ranking list RALL is computed by sorting the summation of the four ranking lists above in ascending order.