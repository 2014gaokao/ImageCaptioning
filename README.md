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
AoANet
```
{'Bleu_1': 0.8054903453672397, 'Bleu_2': 0.6523038976984842, 'Bleu_3': 0.5096621263772566, 'Bleu_4': 0.39140307771618477, 'METEOR': 0.29011216375635934, 'ROUGE_L': 0.5890369750273199, 'CIDEr': 1.2892294296245852}
```

Ours
```
{'Bleu_1': 0.806, 'Bleu_4': 0.392, 'METEOR': 0.290, 'ROUGE_L': 0.590, 'CIDEr': 1.292}
```
