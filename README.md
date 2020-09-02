# ImageCaptioning
Modification based on [AoANet](https://github.com/husthuaan/AoANet) with higher CIDEr score

## Requirements
* Python 3.6
* Java 1.8
* PyTorch 1.0
* cider
* coco-caption
* tensorboardX

## Model
### Encoder
[Augmenting Self-attention with Persistent Memory](https://arxiv.org/pdf/1907.01470.pdf)
</br>

<img src="https://github.com/2014gaokao/ImageCaptioning/blob/master/vis/encoder.jpg" alt="图片替换文本" width="600" height="450"/>

### Decoder
</br>

![image](https://github.com/2014gaokao/ImageCaptioning/blob/master/vis/sparse.jpg)

## Training

### Prepare data
See details in data/README.md <br>

### Start training
```
# CUDA_VISIBLE_DEVICES=0 sh train.sh
```

### Evaluation
```
# CUDA_VISIBLE_DEVICES=0 sh test.sh
```

### Performance
| method | Bleu_1 | Bleu_2 | Bleu_3 | Bleu_4 | METEOR | ROUGE_L | CIDEr |
|:-----:|---|---|---|---|---|---|---|
|AoANet|0.8054903453672397|0.6523038976984842|0.5096621263772566|0.39140307771618477|0.29011216375635934|0.5890369750273199|1.2892294296245852|
|Ours|0.8072861444505534|0.6546857633417253|0.5105614254570193|0.391872107934891|0.2892757681786928|0.5890655008118075|1.2896424046401054|
