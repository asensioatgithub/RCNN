# A simple implements of RCNN with tensorflow
# Requirements
- python3.6
- tensorflow 1.2.1
# Content
- `finetune_alexnet/`: Storage each epoch's weights in checkpints and log the finetuning progress in TensorBoard.
- `Models/`: To storage alexnet weights and SVM Models.
- `alexnet.py`: an TensorFLow implementation of [AlexNet](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) by Alex Krizhevsky at all.
- `validate_alexnet`: If you wanna to validate alexnet, this script is helpful, you need are the pretrained weights, which you can find [here](http://www.cs.toronto.edu/%7Eguerzhoy/tf_alexnet/bvlc_alexnet.npy), place the weights file in 'Models/AlexNet/' and try command "python validat_alexnet.py":
![images](https://github.com/asensioatgithub/RCNN/blob/master/validate.png)
- `finetune.py`、`datagenerator.py`: Scripts to finetune alexnet, [here](https://github.com/kratzert/finetune_alexnet_with_tensorflow) is the detail instructions to finetune alexnet.
- `ckpt2npy`: Change the format form '.ckpy' to '.npy' of alexnet weights.
- `tool.py`: Some func implements for other files calls, such as non maximum suppression(NMS)、Intersection over Union(IOU)..., and also a func to call module `selectivesearch.selective_search`, you can try "python tool.py" to check the proposal rectangles generate by 'selective_search':
![image](https://github.com/asensioatgithub/RCNN/blob/master/pro_rect.png)
