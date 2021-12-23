# Heterogeneous Graph
## Environment Requirement
The code has been tested running under Python 3.6.9. The required packages are as follows:
* pytorch == 1.0.1
* numpy == 1.17.2
* scikit-learn == 0.21.3

## Example to Run the Codes
The instruction of commands has been clearly stated in the codes (see the parser function in train.py).
* HGAT, Gender Prediction
```
CUDA_VISIBLE_DEVICES=0 python train.py --pkl-dir 00 --data-dir data --model gat --hidden-units 16,16 --heads 8,8,1 --train-ratio 75 --valid-ratio 12.5 --instance-normalization --weight-decay 5e-4 --class-weight-balanced --patience 10 --epochs 100 --task gender --use-word-feature --lr 0.005 --dropout 0.6 --batch 64
```

* HGCN, Age Prediction
```
CUDA_VISIBLE_DEVICES=1 python train.py --pkl-dir 01 --data-dir data --model gcn --hidden-units 128,128 --train-ratio 75 --valid-ratio 12.5 --instance-normalization --weight-decay 5e-4 --class-weight-balanced --patience 10 --epochs 100 --task age --use-word-feature --lr 0.1 --dropout 0.2 --batch 32
```

## Dataset
