# yolov6n_v2.0_caffe_onnx_rknn

yolov6n 2.0 部署版本，后处理用python语言和C++语言形式进行改写，便于移植不同平台（caffe、onnx、rknn）。


说明：由于 onnx 对 silu 不支持，导出 onnx 时直接将 silu 改成了 relu，因此效果会比pytorch效果差一些。

# 文件夹结构说明

yolov6n_caffe：去除维度变换层的prototxt、caffeModel、测试图像、测试结果、测试demo脚本

yolov6n_onnx：onnx模型、测试图像、测试结果、测试demo脚本

yolov6n_rknn：rknn模型、测试（量化）图像、测试结果、onnx2rknn转换测试脚本

# 测试结果

![image](https://github.com/cqu20160901/yolov6n_v2.0_onnx_rknn/blob/main/yolov6n_rknn/test_rknn_result.jpg)
