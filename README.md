# Diffusion Rejection Sampling (DiffRS) (ICML 2024)
This repository is the implementation of Diffusion Rejection Sampling, for Gaudi-v2 of the code below :
* [Na, B., Kim, Y., Park, M., Shin, D., Kang, W., & Moon, I. C. Diffusion Rejection Sampling. In Forty-first International Conference on Machine Learning.](https://github.com/aailabkaist/DiffRS)


| [paper](https://proceedings.mlr.press/v235/na24a.html) | [arXiv](https://arxiv.org/abs/2405.17880) | [poster](https://icml.cc/media/PosterPDFs/ICML%202024/34559.png?t=1721399675.3276865) |


**[Byeonghu Na](https://sites.google.com/view/byeonghu-na), [Yeongmin Kim](https://sites.google.com/view/yeongmin-space), Minsang Park, Donghyeok Shin, [Wanmo Kang](https://sites.google.com/site/wanmokang), and [Il-Chul Moon](https://aai.kaist.ac.kr/bbs/board.php?bo_table=sub2_1&wr_id=3)**   


--------------------

This paper introduces **Diffusion Rejection Sampling (DiffRS)**, a new diffusion sampling approach that ensures alignment between the reverse transition and the true transition at each timestep.

<img src="./figures/SamplingProcess_v10.png" width="1000" title="example" alt="Illustration of the sampling process for DiffRS. The path with the green background represents the DiffRS sampling process, and the rightmost images are generated when the images are sampled as a base sampler without rejection from the intermediate image. Timesteps are expressed as the noise level σ from the EDM scheme.">

<img src="./figures/overview_v10.png" width="1000" title="overview" alt="Overview of DiffRS. We sequentially apply the rejection sampling on the pre-trained transition kernel (red) to align the true transition kernel (blue). The acceptance probability is estimated by the time-dependent discriminator.">
