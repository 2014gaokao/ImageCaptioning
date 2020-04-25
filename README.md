# AoSA
Explore Self-Attention on Image Captioning

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
# CUDA_VISIBLE_DEVICES=0 python eval.py --model log/log_aoanet_rl/model.pth --infos_path log/log_aoanet_rl/infos_aoanet.pkl  --dump_images 0 --dump_json 1 --num_images -1 --language_eval 1 --beam_size 2 --batch_size 100 --split test
```

### Performance
