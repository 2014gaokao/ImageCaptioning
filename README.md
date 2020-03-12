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
(notes: We set word_count_threshold in scripts/prepro_labels.py to 4 to generate a vocabulary of size 10,369.) <br><br>
You should also preprocess the dataset and get the cache for calculating cider score for SCST:
```
# python scripts/prepro_ngrams.py --input_json data/dataset_coco.json --dict_json data/cocotalk.json --output_pkl data/coco-train --split train
```

### Start training
```
# CUDA_VISIBLE_DEVICES=0 sh train.sh
```

### Evaluation
```
# CUDA_VISIBLE_DEVICES=0 python eval.py --model log/log_aoanet_rl/model.pth --infos_path log/log_aoanet_rl/infos_aoanet.pkl  --dump_images 0 --dump_json 1 --num_images -1 --language_eval 1 --beam_size 2 --batch_size 100 --split test
```

### Performance
