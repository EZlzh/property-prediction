# Property Prediction

[Open Tasks](https://www.aicures.mit.edu/tasks)

## Prerequisites

* Python 3
* PyTorch (see <https://pytorch.org/get-started/locally/>)
* RDKit (see <http://www.rdkit.org/docs/Install.html>)
* DGL (see <https://www.dgl.ai/pages/start.html>)
* scikit-learn
* colorama
* click

```
sudo pip install scikit-learn colorama click
```

## Usage

See `python src/main.py train --help`.

e.g. train GCN (from DGL):

```
python src/main.py -v train -e 0.001 --train-with-test -m gcn --ndrop 0.90 --cuda
```

## Results

* ToyGCN

```
python src/main.py -v train -m toy-gcn --ndrop=0.85 > result/toy-gcn.txt
```

* GCN

```
python src/main.py -v train -m gcn > result/gcn.txt
```

## TODO

* Training framework
    * [x] Memory cache for molecule parsing.
    * [ ] Disk cache for molecule parsing.
    * [ ] Multiprocessing.
* Models
    * [x] GCN
    * [ ] GAT

## Contributors

* Lin Zihang ([@EZlzh](https://github.com/EZlzh))
* Xue Zhenliang ([@riteme](https://github.com/riteme))