# PyAFAR

PyAFAR is a Python-based, open-source facial action unit detection library for use with adults and infants.

## Requirements

PyAFAR comes as a executable file for Windows, Linux (Ubuntu) and Mac platforms. It can be used as an out-of-the-box software with no additional dependency requirements.

### Last validated system configuration

Saurabh to help

#### Windows


#### Ubuntu


#### MacOS


## Modules

- `Facial Landmarks & Head Pose`: Face detection and landmark prediction is done using the [MediaPipe](https://research.google/pubs/pub48292/) library. Tracking is performed using the [FaceNet](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Schroff_FaceNet_A_Unified_2015_CVPR_paper.pdf). The Perspective-n-Point (PnP) method is used to predict Roll, Pitch and Yaw
- `Face Normalization`: The landmark predictions are used to normalize faces using the [dlib](http://dlib.net/) library.
- `AU predictions`: Separate detection modules for occurrence are available for both adults and infants. Intensity predictions are available for adults only.
- `Output`: PyAFAR can output frame-level predictions in CSV and JSON formats to enable easy reading with most platforms used by both computational as well as domain experts.

## How to run

A step-by-step instruction guide with screenshots on how to run PyAFAR can be found [here](./resources/readme/instructions.md).


## Output format

A complete description of each variable in the output can be found [here](./resources/readme/output_format.md).


## Citations

PyAFAR is a result of the following publications. If you use PyAFAR in your work, cite our following contributions:


**Pipeline**
```
@inproceedings{hindujapyafar,
  title={PyAFAR: Python-based Automated Facial Action Recognition library for use in Infants and Adults},
  author={Hinduja, Saurabh and Ertugrul, Itir Onal and Bilalpur, Maneesh and Messinger, Daniel S and Cohn, Jeffrey F},
  booktitle={International Conference on Affective Computing and Intelligent Interaction},
  year={2023},
  organization={IEEE}
}
```
**Infant AU detector**

```
@article{onal2023infant,
  title={Infant AFAR: Automated facial action recognition in infants},
  author={Onal Ertugrul, Itir and Ahn, Yeojin Amy and Bilalpur, Maneesh and Messinger, Daniel S and Speltz, Matthew L and Cohn, Jeffrey F},
  journal={Behavior research methods},
  volume={55},
  number={3},
  pages={1024--1035},
  year={2023},
  publisher={Springer}
}
```

**Adult AU detector:**
```
@inproceedings{ertugrul2019cross,
  title={Cross-domain AU Detection: Domains, Learning Approaches, and Measures},
  author={Onal Ertugrul, Itir and Cohn, Jeffrey F and Jeni, L{\'a}szl{\'o} A and Zhang, Zheng and Yin, Lijun and Ji, Qiang},
  booktitle={2019 14th IEEE International Conference on Automatic Face \& Gesture Recognition (FG 2019)},
  year={2019},
  organization={IEEE}
}
```

## MIT License

Copyright (c) 2022 AffectAnalysisGroup (merge and publish rights also given??)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.