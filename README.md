# ImageCaptioning
Modification based on AoANet with higher CIDEr score

## Requirements
* Python 3.6
* Java 1.8
* PyTorch 1.0
* cider
* coco-caption
* tensorboardX

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
|Ours|0.8058726534753762|0.6527200356550622|0.5095779998314923|0.39176873009761093|0.29022030127786064|0.5891619079505703|1.2919884683604208|
