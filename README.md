该文档是用pytorch内置的keypoint_rcnn模型来对自建的数据集进行训练

## 实验环境和相关预备
|key|value|
|----------|----------|
|系统环境|Ubuntu 18.04|
|CPU|Intel(R) Xeon(R) CPU E5-2678 v3 @ 2.50GHz|
|GPU|NVIDIA Tesla K80|
|Python版本|jupyter-notebook python3.7.10 (anaconda installed python3.7.10 virtual environment)|
|torch版本|1.13.0+cu116|
|模型版本|torchvision.models.detection.keypointrcnn_resnet50_fpn|
|摄像头像元尺寸|未知|
|摄像头传感器尺寸|未知|
|摄像头视角角度|未知|
|摄像头输出分辨率|640*480|
|其他|Bittle，Bittle支架，摄像头支架|

*对pycocotools库中的cocoeval.py文件进行修改。
```python
#modify self.kpt_oks_sigmas = np.array([.26, .25, .25, .35, .35, .79, .79, .72, .72, .62,.62, 1.07, 1.07, .87, .87, .89, .89])/10.0
#to
self.kpt_oks_sigmas = np.array([.5, .5]) / 10.0
```

数据集标注工具 : [**labelImg**](https://github.com/heartexlabs/labelImg)

数据集格式转换，转换成keypoint_rcnn要求的格式,见[Convert_labels](./Convert_labels.ipynb).

展望：
* 数据集的收集可以多样化：模拟数据和现实数据