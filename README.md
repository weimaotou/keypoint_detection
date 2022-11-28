该文档是用pytorch内置的keypoint_rcnn模型来对自建的数据集进行训练

*对pycocotools库中的cocoeval.py文件进行修改。
```python
#modify self.kpt_oks_sigmas = np.array([.26, .25, .25, .35, .35, .79, .79, .72, .72, .62,.62, 1.07, 1.07, .87, .87, .89, .89])/10.0
#to
self.kpt_oks_sigmas = np.array([.5, .5]) / 10.0
```

数据集标注工具 : [**labelImg**](https://github.com/heartexlabs/labelImg)
数据集格式转换，转换成keypoint_rcnn要求的格式

展望：
* 数据集的收集可以多样化：模拟数据和现实数据