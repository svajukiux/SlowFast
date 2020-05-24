# Getting Started with PySlowFast

This document provides a brief intro of launching jobs for training. Before launching any job, make sure you have properly installed the PySlowFast following the instruction in [README.md](README.md) and you have prepared the dataset following [DATASET.md](slowfast/datasets/DATASET.md) with the correct format.

## Train a Model from Scratch

The training of the original network or a modification can be started by writing this into the command line with an appropriate .yaml config file, which can be found in configs/UCF/:

```
python tools/run_net.py \
  --cfg configs/UCF/SlowFast_4x16_Original.yaml \
  DATA.PATH_TO_DATA_DIR "./csv_files" \
  NUM_GPUS 1 \
  TRAIN.BATCH_SIZE 16 \
```

## Resume from an Existing Checkpoint
To resume training from an existing checkpoint, you can add the following line in the command line, or you can also add it in the YAML config:

```
TRAIN.CHECKPOINT_FILE_PATH path_to_your_PyTorch_checkpoint
```
