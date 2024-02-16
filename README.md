# Taylor videos

## Usage

Using Taylor videos is a simple two-step process.

- To extract Taylor video, simply run `taylor-video.ipynb`.
- To use Taylor videos for action recognition, simply follow [open-mmlab/mmaction2](https://github.com/open-mmlab/mmaction2?tab=readme-ov-file):
  - Environmental setup: [Installation](https://mmaction2.readthedocs.io/en/latest/get_started/installation.html).

## Visualisation

Taylor frames indicate motion strengths and directions
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/dir-str.png)

Taylor videos remove redundancy, such as static backgrounds, unstable pixels, watermarks, and captions.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/rem-cap.png)

Qualitative impact of the number of terms used in Taylor series on the action ride bike in HMDB-51 (top row), a synthetic action video of CATER (middle row), and the finegrained action place in MPII Cooking Activity (bottom row). 
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/terms.png)

Taylor videos are able to remove distinct facial features of individuals compared to RGB videos. This allows the data collection and processing to have improved privacy.
![Alt Text](https://github.com/LeiWangR/video-ar/blob/main/images/face.png)

For visualizations in the form of videos, please refer to the folders provided in this repository.

## Citation

You can cite the following paper for the use of this work:

```
@misc{wang2024taylor,
      title={Taylor Videos for Action Recognition}, 
      author={Lei Wang and Xiuyuan Yuan and Tom Gedeon and Liang Zheng},
      year={2024},
      eprint={2402.03019},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

### Acknowledgements

[Xiuyuan Yuan](https://jackyuanx.github.io/) conducted the research under the supervision of [Lei Wang](https://leiwangr.github.io/) in the ANU Summer Scholars Program. He is supported by a Summer Research Internship provided by the ANU School of Computing. This work is also supported by the NCI Adapter Scheme, with computational resources provided by NCI Australia, an NCRIS-enabled capability supported by the Australian Government.
