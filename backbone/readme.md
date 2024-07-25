# Backbone

## Skeletonal AR backbone

### Prerequisites
We use the ST-GCN model (AAAI 2018) with all setups following the original settings. The codebase is based on **Python 3** (>=3.5), and there are a few dependencies required to run the code. The major libraries are
- [PyTorch](http://pytorch.org/)
- Other Python libraries can be installed by `pip install -r requirements.txt`

### Installation
```
cd torchlight; python setup.py install; cd ..
```

### Training
To train a new ST-GCN model, run
```
python main.py recognition -c config/st_gcn/kinetics-skeleton/train.yaml [--work_dir <work folder>]
```
<!-- ```
python main.py recognition -c config/st_gcn/<dataset>/train.yaml [--work_dir <work folder>]
```
where the ```<dataset>``` must be ```nturgbd-cross-view```, ```nturgbd-cross-subject``` or ```kinetics-skeleton```, depending on the dataset you want to use. -->
The training results, including **model weights**, configurations and logging files, will be saved under the ```./work_dir``` by default or ```<work folder>``` if you appoint it.

You can modify the training parameters such as ```work_dir```, ```batch_size```, ```step```, ```base_lr``` and ```device``` in the command line or configuration files. The order of priority is:  command line > config file > default parameter. For more information, use ```main.py -h```.

Finally, custom model evaluation can be achieved by this command as we mentioned above:
```
python main.py -c config/st_gcn/<dataset>/test.yaml --weights <path to model weights>
```





