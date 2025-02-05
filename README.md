# Crypto-LLM



# Result 

TODO

# Install 

```
conda install -c "nvidia/label/cuda-12.1.0" cuda-toolkit
conda install pytorch torchvision  pytorch-cuda=12.1 -c pytorch -c nvidia

# install vllm
pip3 install vllm==0.6.3 # or you can install 0.5.4, 0.4.2 and 0.3.1
pip3 install ray

# verl
pip install -e .

# flash attention 2
pip3 install flash-attn --no-build-isolation
# quality of life
pip install wandb IPython matplotlib
```

```
python -c "from modelscope import snapshot_download; snapshot_download('Qwen/Qwen2.5-0.5B', cache_dir='models')"
```

```
export N_GPUS=1
export BASE_MODEL=models/Qwen/Qwen2.5-0.5B
export DATA_DIR=~/data/countdown
export ROLLOUT_TP_SIZE=1
export EXPERIMENT_NAME=countdown-qwen2.5-0.5b
export VLLM_ATTENTION_BACKEND=XFORMERS
bash ./scripts/train_tiny_zero.sh
```


## Miscellaneous

It starts from a clone version of [TinyZero](https://github.com/Jiayi-Pan/TinyZero)
A tutorial for how to start can be found [here](https://www.philschmid.de/mini-deepseek-r1)



