
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


### uv
```
uv venv --python=python3.9

source .venv/bin/activate

uv pip install -r requirements.txt

uv pip install -r pyproject.toml

uv pip sync pyproject.toml

uvicorn svc.main:app --port 5002 --reload

```

