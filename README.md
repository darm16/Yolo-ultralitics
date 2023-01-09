<div align="center">
  <p>
    <a align="center" href="https://ultralytics.com/yolov8" target="_blank">
      <img width="850" src="https://raw.githubusercontent.com/ultralytics/assets/main/yolov8/banner-yolov8.png"></a>
  </p>

[English](README.md) | [简体中文](README.zh-CN.md)
<br>

<div>
    <a href="https://github.com/ultralytics/ultralytics/actions/workflows/ci.yaml"><img src="https://github.com/ultralytics/ultralytics/actions/workflows/ci.yaml/badge.svg" alt="Ultralytics CI"></a>
    <a href="https://zenodo.org/badge/latestdoi/264818686"><img src="https://zenodo.org/badge/264818686.svg" alt="YOLOv8 Citation"></a>
    <a href="https://hub.docker.com/r/ultralytics/yolov5"><img src="https://img.shields.io/docker/pulls/ultralytics/yolov5?logo=docker" alt="Docker Pulls"></a>
    <br>
    <a href="https://bit.ly/yolov5-paperspace-notebook"><img src="https://assets.paperspace.io/img/gradient-badge.svg" alt="Run on Gradient"></a>
    <a href="https://colab.research.google.com/github/ultralytics/ultralytics/blob/main/examples/tutorial.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
    <a href="https://www.kaggle.com/ultralytics/yolov5"><img src="https://kaggle.com/static/images/open-in-kaggle.svg" alt="Open In Kaggle"></a>
  </div>
  <br>

[Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) is the latest version of the YOLO object detection and image segmentation model developed by [Ultralytics](https://ultralytics.com). YOLOv8 is a cutting-edge, state-of-the-art (SOTA) model that builds upon the success of previous YOLO versions and introduces new features and improvements to further boost performance and flexibility.

The YOLOv8 models are designed to be fast, accurate, and easy to use, making them an excellent choice for a wide range of object detection, image segmentation and image classification tasks.

Whether you are a seasoned machine learning practitioner or new to the field, we hope that the resources on this page will help you get the most out of YOLOv8.

<div align="center">
    <a href="https://github.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-github.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.linkedin.com/company/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-linkedin.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://twitter.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-twitter.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.producthunt.com/@glenn_jocher" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-producthunt.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://youtube.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-youtube.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.facebook.com/ultralytics" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-facebook.png" width="2%" alt="" /></a>
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="2%" alt="" />
    <a href="https://www.instagram.com/ultralytics/" style="text-decoration:none;">
      <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-instagram.png" width="2%" alt="" /></a>
  </div>
</div>

## <div align="center">Documentation</div>

See below for quickstart intallation and usage example, and see the [YOLOv8 Docs](https://docs.ultralytics.com) for full documentation on training, validation, prediction and deployment.

<details open>
<summary>Install</summary>

Pip install the ultralytics package including all [requirements.txt](https://github.com/ultralytics/ultralytics/blob/main/requirements.txt) in a
[**Python>=3.7.0**](https://www.python.org/) environment, including
[**PyTorch>=1.7**](https://pytorch.org/get-started/locally/).

```bash
pip install ultralytics
```

</details>

<details open>
<summary>Usage</summary>

YOLOv8 may be used in a python environment:

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")  # load a pretrained YOLOv8n model

model.train(data="coco128.yaml")  # train the model
model.val()  # evaluate model performance on the validation set
model.predict(source="https://ultralytics.com/images/bus.jpg")  # predict on an image
model.export(format="onnx")  # export the model to ONNX format
```

Or with CLI `yolo` commands:

```bash
yolo task=detect    mode=train    model=yolov8n.pt        args...
          classify       predict        yolov8n-cls.yaml  args...
          segment        val            yolov8n-seg.yaml  args...
                         export         yolov8n.pt        format=onnx  args...
```

[Models](https://github.com/ultralytics/ultralytics/tree/main/ultralytics/yolo/v8/models) download automatically from the latest
Ultralytics [release](https://github.com/ultralytics/ultralytics/releases).

</details>

## <div align="center">Checkpoints</div>

All YOLOv8 pretrained models are available here. Detection and Segmentation models are pretrained on the COCO dataset, while Classification models are pretrained on the ImageNet dataset.

[Models](https://github.com/ultralytics/ultralytics/tree/main/ultralytics/yolo/v8/models) download automatically from the latest
Ultralytics [release](https://github.com/ultralytics/ultralytics/releases) on first use.

<details open><summary>Detection</summary>
  
| Model                                                                                     | size<br><sup>(pixels) | mAP<sup>val<br>50-95 | Speed<br><sup>CPU<br>(ms) | Speed<br><sup>T4 GPU<br>(ms) | params<br><sup>(M) | FLOPs<br><sup>(B) |
| ----------------------------------------------------------------------------------------- | --------------------- | -------------------- | ------------------------- | ---------------------------- | ------------------ | ----------------- |
| [YOLOv8n](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8n.pt) | 640                   | 37.3                 | -                         | -                            | 3.2                | 8.9               |
| [YOLOv8s](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8s.pt) | 640                   | 44.9                 | -                         | -                            | 11.2               | 28.8              |
| [YOLOv8m](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8m.pt) | 640                   | 50.2                 | -                         | -                            | 25.9               | 79.3              |
| [YOLOv8l](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8l.pt) | 640                   | 52.9                 | -                         | -                            | 43.7               | 165.7             |
| [YOLOv8x](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8x.pt) | 640                   | 53.9                 | -                         | -                            | 68.2               | 258.5             |

- **mAP<sup>val</sup>** values are for single-model single-scale on [COCO val2017](http://cocodataset.org) dataset.
<br>Reproduce by `yolo mode=val task=detect data=coco.yaml device=0`
- **Speed** averaged over COCO val images using a [AWS p3.2xlarge](https://aws.amazon.com/ec2/instance-types/p3/) instance.
<br>Reproduce by `yolo mode=val task=detect data=coco128.yaml batch=1 device=0/cpu`

</details>


<details><summary>Segmentation</summary>
  
| Model                                                                                     | size<br><sup>(pixels) | mAP<sup>val<br>50-95 | Speed<br><sup>CPU<br>(ms) | Speed<br><sup>T4 GPU<br>(ms) | params<br><sup>(M) | FLOPs<br><sup>(B) |
| ----------------------------------------------------------------------------------------- | --------------------- | -------------------- | ------------------------- | ---------------------------- | ------------------ | ----------------- |
| [YOLOv8n](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8n-seg.pt) | 640                   | 37.3                 | -                         | -                            | 3.2                | 8.9               |
| [YOLOv8s](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8s-seg.pt) | 640                   | 44.9                 | -                         | -                            | 11.2               | 28.8              |
| [YOLOv8m](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8m-seg.pt) | 640                   | 50.2                 | -                         | -                            | 25.9               | 79.3              |
| [YOLOv8l](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8l-seg.pt) | 640                   | 52.9                 | -                         | -                            | 43.7               | 165.7             |
| [YOLOv8x](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8x-seg.pt) | 640                   | 53.9                 | -                         | -                            | 68.2               | 258.5             |

- **mAP<sup>val</sup>** values are for single-model single-scale on [COCO val2017](http://cocodataset.org) dataset.
<br>Reproduce by `yolo mode=val task=detect data=coco.yaml device=0`
- **Speed** averaged over COCO val images using a [AWS p3.2xlarge](https://aws.amazon.com/ec2/instance-types/p3/) instance.
<br>Reproduce by `yolo mode=val task=detect data=coco128.yaml batch=1 device=0/cpu`

</details>


<details><summary>Classification</summary>
  
| Model                                                                                     | size<br><sup>(pixels) | mAP<sup>val<br>50-95 | Speed<br><sup>CPU<br>(ms) | Speed<br><sup>T4 GPU<br>(ms) | params<br><sup>(M) | FLOPs<br><sup>(B) |
| ----------------------------------------------------------------------------------------- | --------------------- | -------------------- | ------------------------- | ---------------------------- | ------------------ | ----------------- |
| [YOLOv8n](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8n-cls.pt) | 640                   | 37.3                 | -                         | -                            | 3.2                | 8.9               |
| [YOLOv8s](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8s-cls.pt) | 640                   | 44.9                 | -                         | -                            | 11.2               | 28.8              |
| [YOLOv8m](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8m-cls.pt) | 640                   | 50.2                 | -                         | -                            | 25.9               | 79.3              |
| [YOLOv8l](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8l-cls.pt) | 640                   | 52.9                 | -                         | -                            | 43.7               | 165.7             |
| [YOLOv8x](https://github.com/ultralytics/ultralytics/releases/download/v8.0.0/yolov8x-cls.pt) | 640                   | 53.9                 | -                         | -                            | 68.2               | 258.5             |

- **mAP<sup>val</sup>** values are for single-model single-scale on [COCO val2017](http://cocodataset.org) dataset.
<br>Reproduce by `yolo mode=val task=detect data=coco.yaml device=0`
- **Speed** averaged over COCO val images using a [AWS p3.2xlarge](https://aws.amazon.com/ec2/instance-types/p3/) instance.
<br>Reproduce by `yolo mode=val task=detect data=coco128.yaml batch=1 device=0/cpu`

</details>


## <div align="center">Integrations</div>

<br>
<a align="center" href="https://bit.ly/ultralytics_hub" target="_blank">
<img width="100%" src="https://github.com/ultralytics/assets/raw/main/im/integrations-loop.png"></a>
<br>
<br>

<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-roboflow.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="15%" height="0" alt="" />
  <a href="https://cutt.ly/yolov5-readme-clearml">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-clearml.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="15%" height="0" alt="" />
  <a href="https://bit.ly/yolov5-readme-comet">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-comet.png" width="10%" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="15%" height="0" alt="" />
  <a href="https://bit.ly/yolov5-neuralmagic">
    <img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/logo-neuralmagic.png" width="10%" /></a>
</div>

|                                                           Roboflow                                                           |                                                            ClearML ⭐ NEW                                                            |                                                                        Comet ⭐ NEW                                                                         |                                           Neural Magic ⭐ NEW                                           |
| :--------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------: |
| Label and export your custom datasets directly to YOLOv8 for training with [Roboflow](https://roboflow.com/?ref=ultralytics) | Automatically track, visualize and even remotely train YOLOv8 using [ClearML](https://cutt.ly/yolov5-readme-clearml) (open-source!) | Free forever, [Comet](https://bit.ly/yolov5-readme-comet2) lets you save YOLOv8 models, resume training, and interactively visualise and debug predictions | Run YOLOv8 inference up to 6x faster with [Neural Magic DeepSparse](https://bit.ly/yolov5-neuralmagic) |

## <div align="center">Ultralytics HUB</div>

[Ultralytics HUB](https://bit.ly/ultralytics_hub) is our ⭐ **NEW** no-code solution to visualize datasets, train YOLOv8 🚀 models, and deploy to the real world in a seamless experience. Get started for **Free** now! Also run YOLOv8 models on your iOS or Android device by downloading the [Ultralytics App](https://ultralytics.com/app_install)!

<a align="center" href="https://bit.ly/ultralytics_hub" target="_blank">
<img width="100%" src="https://github.com/ultralytics/assets/raw/main/im/ultralytics-hub.png"></a>

## <div align="center">Contribute</div>

We love your input! YOLOv5 and YOLOv8 would not be possible without help from our community. Please see our [Contributing Guide](CONTRIBUTING.md) to get started, and fill out our [Survey](https://ultralytics.com/survey?utm_source=github&utm_medium=social&utm_campaign=Survey) to send us feedback on your experience. Thank you 🙏 to all our contributors!

<!-- SVG image from https://opencollective.com/ultralytics/contributors.svg?width=990 -->

<a href="https://github.com/ultralytics/yolov5/graphs/contributors"><img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/image-contributors-1280.png"/></a>

## <div align="center">License</div>

YOLOv8 is available under two different licenses:

- **GPL-3.0 License**: See [LICENSE](https://github.com/ultralytics/ultralytics/blob/main/LICENSE) file for details.
- **Enterprise License**: Provides greater flexibility for commercial product development without the open-source requirements of GPL-3.0. Typical use cases are embedding Ultralytics software and AI models in commercial products and applications. Request an Enterprise License at [Ultralytics Licensing](https://ultralytics.com/license).

## <div align="center">Contact</div>

For YOLOv8 bugs and feature requests please visit [GitHub Issues](https://github.com/ultralytics/ultralytics/issues). For professional support please [Contact Us](https://ultralytics.com/contact).

<br>
<div align="center">
  <a href="https://github.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-github.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.linkedin.com/company/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-linkedin.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://twitter.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-twitter.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.producthunt.com/@glenn_jocher" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-producthunt.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://youtube.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-youtube.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.facebook.com/ultralytics" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-facebook.png" width="3%" alt="" /></a>
  <img src="https://github.com/ultralytics/assets/raw/main/social/logo-transparent.png" width="3%" alt="" />
  <a href="https://www.instagram.com/ultralytics/" style="text-decoration:none;">
    <img src="https://github.com/ultralytics/assets/raw/main/social/logo-social-instagram.png" width="3%" alt="" /></a>
</div>
