**This is the PyTorch implement of MobileNet V2**([Inverted Residuals and Linear Bottlenecks: Mobile Networks for Classification, Detection and Segment](128.84.21.199/abs/1801.04381))


### Usage

* Prepare data

This code takes ImageNet dataset as example. You can download ImageNet dataset and put them as follows:

```
├── train.py # train script
├── MobileNetV2.py # network of MobileNetV2
├── read_ImageNetData.py # ImageNet dataset read script
├── ImageData # train and validation data
	├── ILSVRC2012_img_train
		├── n01440764
		├──    ...
		├── n15075141
	├── ILSVRC2012_img_val
	├── ILSVRC2012_dev_kit_t12
		├── data
			├── ILSVRC2012_validation_ground_truth.txt
```

* Train

You can change batch size/gpus/lr and train from scratch:

```
python train.py --batch-size 512 --gpus 0,1,2,3 --lr 0.1
```