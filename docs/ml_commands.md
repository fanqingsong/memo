
# machine learning

## commands

### conda
```
sudo docker run --gpus all --ipc=host --network=host  --name=xxxxx  -v /mnt:/mnt  -it continuumio/anaconda3 bash

conda create -n xxxxx python=3.11

conda env list

conda activate xxxxx

conda deactivate

conda env remove --name xxxxx
```

