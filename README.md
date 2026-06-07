### Dependencies

* Python 3.9
* PyTorch 1.13.1
* DGL 0.9.1
* scikit-learn 1.1.2
* SciPy 1.9.0
* PyYAML 6.0
* tqdm 4.64.1

  The ACM dataset can be obtained via the following link: https://github.com/RuixZh/SR-RSC

Usage
  python main.py \
  --dataset     <DATASET>         \   # ACM / DBLP / Yelp
  --split-strategy <STRATEGY>     \   # subject / venue / location
  --framework   <FRAMEWORK>       \   # FedHGN / FedAvg / FedProx / Local / Central
  --num-clients <K>               \   # number of clients (default: 3)
  --gpu         <GPU_ID>          \   # GPU index; -1 for CPU
  --random-seed <SEED>                # default: 1000

For example
  python main.py -d ACM -s subject -f FedHGN -c 3 -g 0 --use-attr-completion
