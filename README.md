### 该文档是用pytorch内置的keypoint_rcnn模型来对自建的数据集进行训练
### 需要对pycocotools库中的cocoeval.py文件进行修改。
### self.kpt_oks_sigmas = np.array([.5, .5]) / 10.0
### 数据集标注工具 : [**labelImg**](https://github.com/heartexlabs/labelImg)
### 数据集格式转换，转换成keypoint_rcnn要求的格式
### 数据集的收集可以多样化：模拟数据和现实数据