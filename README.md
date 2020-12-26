# SemanticSegmentation-CoreML

![platform-ios](https://img.shields.io/badge/platform-ios-lightgrey.svg)
![swift-version](https://img.shields.io/badge/swift-5.0-red.svg)
![lisence](https://img.shields.io/badge/license-MIT-black.svg)

This project is Object Segmentation on iOS with Core ML.<br>If you are interested in iOS + Machine Learning, visit [here](https://github.com/motlabs/iOS-Proejcts-with-ML-Models) you can see various DEMOs.<br>

| DEMO                                                         | Screenshot 1                                  | Screenshot 2                                  | Screenshot 3                                  |
| ------------------------------------------------------------ | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| <img src="https://user-images.githubusercontent.com/37643248/99242802-167ad280-2843-11eb-959a-5fe3b169d8f0.gif" width=240px> | <img src="resource/IMG_3633.PNG" width=240px> | <img src="resource/IMG_3632.PNG" width=240px> | <img src="resource/IMG_3635.PNG" width=240px> |

## How it works

> When use Metal

![image](https://user-images.githubusercontent.com/37643248/100520189-da9b2200-31df-11eb-928f-db6f503ea4e0.png)

## Requirements

- Xcode 10.2+
- iOS 12.0+
- Swift 5

## Model

### Download

Download model from [apple's model page](https://developer.apple.com/machine-learning/models/).

### Matadata

|                  |             input node              |                 output node                 |  size  |
| :--------------: | :---------------------------------: | :-----------------------------------------: | :----: |
|    DeepLabV3     | `[1, 513, 513, 3]`<br>name: `image` | `[513, 513]`<br>name: `semanticPredictions` | 8.6 MB |
|  DeepLabV3FP16   | `[1, 513, 513, 3]`<br>name: `image` | `[513, 513]`<br>name: `semanticPredictions` | 4.3 MB |
| DeepLabV3Int8LUT | `[1, 513, 513, 3]`<br>name: `image` | `[513, 513]`<br>name: `semanticPredictions` | 2.3 MB |

### Inference Time

| Device            | Inference Time | Total Time (GPU) | Total Time (CPU) |
| ----------------- | :------------: | :--------------: | :--------------: |
| iPhone 12 Pro     |   **29 ms**    |    **29 ms**     |      240 ms      |
| iPhone 12 Pro Max |       ⏲        |        ⏲        |        ⏲        |
| iPhone 12         |     30 ms      |      31 ms       |     253 ms       |
| iPhone 12 Mini    |     29 ms      |      30 ms       |   **226 ms**     |
| iPhone 11 Pro     |     39 ms      |      40 ms       |      290 ms      |
| iPhone 11 Pro Max |     35 ms      |      36 ms       |      280 ms      |
| iPhone 11         |       40 ms       |        42 ms        |        293 ms        |
| iPhone SE (2nd)   |       ⏲        |        ⏲         |        ⏲        |
| iPhone XS Max     |       ⏲        |        ⏲         |        ⏲        |
| iPhone XS         |     54 ms      |      55 ms        |      327 ms      |
| iPhone XR         |     133 ms     |        ⏲         |      402 ms      |
| iPhone X          |     137 ms     |      143 ms       |      376 ms      |
| iPhone 8+         |     140 ms     |      146 ms       |      420 ms      |
| iPhone 8          |     189 ms     |        ⏲         |      529 ms      |
| iPhone 7+         |     240 ms     |        ⏲         |      667 ms      |
| iPhone 7          |     192 ms     |      208 ms       |      528 ms      |
| iPhone 6S +       |     309 ms     |        ⏲         |     1015 ms      |

⏲: need to measure

## See also

- [motlabs/iOS-Proejcts-with-ML-Models](https://github.com/motlabs/iOS-Proejcts-with-ML-Models)<br>
  : The challenge using machine learning model created from tensorflow on iOS
- [deeplab on TensorFlow](https://github.com/tensorflow/models/tree/master/research/deeplab)<br>
  : The repository providing DeepLabV3 model
