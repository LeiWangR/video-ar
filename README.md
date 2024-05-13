# Taylor videos and Taylor skeleton sequences

## 1. Application to action recognition

Using Taylor videos for action recognition is a simple two-step process.

- To extract Taylor video from an RGB video, simply run `taylor-video.ipynb`.
- To extract Taylor-transformed skeletons from human skeleton sequences, simply run `taylor-skeleton.ipynb`. Note that we only use the displacement concept for Taylor skeleton sequence computation. The provided Jupyter notebook also displays animations of Taylor skeleton sequences overlaid on top of the original skeletons.
- To use Taylor videos for action recognition, simply follow the instructions provided in [open-mmlab/mmaction2](https://github.com/open-mmlab/mmaction2?tab=readme-ov-file):
  - Environmental setup: [Installation](https://mmaction2.readthedocs.io/en/latest/get_started/installation.html).
- To use Taylor skeleton sequences for action recognition, simply replace the use of original skeleton sequences with the computed Taylor skeleton sequences. 
- Note that Taylor videos and Taylor-transformered skeletons can be applied to various video processing tasks such as anomaly detection, deep fake, motion extraction, video generation, etc.


## 2. Visualisation

For visualizations in the form of videos (Taylor videos with different numbers of terms), please refer to the folders provided in the repository. The pixel values are scaled for better visualisation purposes. Below, we present some visualizations and comparisons of Taylor frames.

### 2.1: Motion strengths and directions
Taylor frames indicate motion strengths and directions. Each channel of the Taylor frame represents a motion concept with positive and negative values indicating motion directions (0 for static pixels). Velocity and acceleration channels are computed per video temporal block, capturing relative motion directions from the initial frame.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/dir-str.png)

### 2.2: Redundancy removal
Taylor videos remove redundancy, such as static backgrounds, unstable pixels, watermarks, and captions.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/rem-cap.png)

### 2.3: Impact of the number of terms
Qualitative impact of the number of terms used in Taylor series on the action ride bike in HMDB-51 (top row), a synthetic action video of CATER (middle row), and the finegrained action place in MPII Cooking Activity (bottom row). We observe that as the number of terms increases, more motion patterns are captured. In scenarios with a moving camera, such as ride bike in the top row, using more terms leads to the inclusion of more background details, such as crosswalk and crowds.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/terms.png)

### 2.4: Potential applications to privacy
Taylor videos are able to remove distinct facial features of individuals compared to RGB videos. This allows the data collection and processing to have improved privacy.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/face.png)

## 3. Citation

You can cite the following paper for the use of this work:

```
@inproceedings{
wang2024taylor,
title={Taylor Videos for Action Recognition},
author={Lei Wang and Xiuyuan Yuan and Tom Gedeon and Liang Zheng},
booktitle={Forty-first International Conference on Machine Learning (ICML)},
year={2024}
}
```

### Acknowledgements

[Xiuyuan Yuan](https://jackyuanx.github.io/) conducted this research under the supervision of [Lei Wang](https://leiwangr.github.io/) in the [ANU Summer Scholars Program](https://cecc.anu.edu.au/current-students/research-opportunities/summer-research-projects-2023). Lei Wang focused on mathematical analysis and modeling, while Xiuyuan Yuan implemented the code and conducted experiments. Xiuyuan Yuan is supported by a Summer Research Internship provided by the ANU School of Computing. This work is also supported by the NCI Adapter Scheme, with computational resources provided by NCI Australia, an NCRIS-enabled capability supported by the Australian Government. 
