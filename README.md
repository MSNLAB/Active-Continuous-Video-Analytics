#  ActVideo: Active Continuous Learning for Video Analytics

This project explores building an efficient edge video analytics platform
by *Active Continuous Learning* to reduce **human labeling** and **edge
storage**. It helps to judiciously select small but valuable partitions
of video frames for continuous learning in video analytics.

- [2022.11.06] Our [paper](https://raw.githubusercontent.com/leeeizhang/leeeizhang/refs/heads/assets/actvideo.pdf) is accepted to ACM SenSys'22 CML-IOT Workshop.

## Repository Organization

```
├── core/                         # ⚡ Core Python package
│   ├── datasets/                 #    - Dataset loaders for video analytic tasks
│   ├── examplers/                #    - Exampler strategies for rehearsal-based learning
│   ├── metrics/                  #    - Training and testing tools for monitoring
│   ├── models/                   #    - Models for video analytic tasks
│   ├── retrainer/                #    - Continuous learning strategies and interfaces
│   ├── strategies/               #    - Sampling strategies for active learner
│   └── utils/                    #    - Utility functions and classes
│
├── exps/                         # 🔬 Examples of active continuous learning
│   ├── common.py                 #    - Interfaces for common experiment supports
│   ├── core50_nic_exp.py         #    - Experiment on CORe50 benchmark
│   └── video_detection_exp.py    #    - Experiment on video object detections
│
├── scripts/                      # 🛠️ Experiment scripts for running and testing
│
└── videos/                       # 📦 Prepared video datasets for testing
```

## Installation

1. Install all dependencies from `requirements.txt` after creating your
   own python environment with `python >= 3.8.0`.

```shell
$ pip3 install -u -r requirements.txt
```

2. Download prepared datasets ([Google Drive](https://drive.google.com/file/d/1b0SWDmDR7WAahO8OTyAfwBicGhHXCAVL/view?usp=sharing)), and then unzip on the projects root path.

```shell
$ tar -zxvf ***.tar.gz
```

## Examples

We provide working examples for running:

- Classification on [CORe50](https://vlomonaco.github.io/core50/) datasets.

```shell
$ bash ./scripts/core50_***.sh
```

- Object Detecting on video datasets.
    - Dash Camera:  `$ bash ./scripts/dashcam_***.sh`
    - Drone Video:  `$ bash ./scripts/drone_***.sh`
    - Traffic Video:  `$ bash ./scripts/traffic_***.sh`

## Contributing

The codes are expanded on the Active-Learning-as-a-Service
([ALaaS](https://github.com/MLSysOps/Active-Learning-as-a-Service)), and
Video-Platform-as-a-Service ([VPaaS](https://arxiv.org/abs/2102.03012)).

This project is still under demo developing. Pull requests are more than welcome! 

If you have any questions please feel free to contact us.

## Cite us

```markdown
@inproceedings{zhang2022towards,
  title={Towards Data-Efficient Continuous Learning for Edge Video Analytics via Smart Caching},
  author={Zhang, Lei and Gao, Guanyu and Zhang, Huaizheng},
  booktitle={Proceedings of the 20th ACM Conference on Embedded Networked Sensor Systems},
  pages={1136--1140},
  year={2022}
}

@article{huang2022active,
  title={Active-Learning-as-a-Service: An Efficient MLOps System for Data-Centric AI},
  author={Huang, Yizheng and Zhang, Huaizheng and Li, Yuanming and Lau, Chiew Tong and You, Yang},
  journal={arXiv preprint arXiv:2207.09109},
  year={2022}
}
```

## License
The project is available as open source under the terms of the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).
