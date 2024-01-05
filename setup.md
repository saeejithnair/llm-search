
# Setup
### Clone repo
```
git clone https://github.com/saeejithnair/llm-search.git
```

### Create conda environment and install packages
```
conda create --name llm_search python=3.10
conda activate llm_search
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```

### Set up environment variables
```
source ./setvars.sh
```

### Install packages
```
pip install -e .
```

### Make folder structure
```
mkdir -p llm/embeddings llm/cache llm/models llm/config sample_docs
```

### Download models
```
cd llm/cache
wget https://huggingface.co/TheBloke/airoboros-l2-13B-gpt4-1.4.1-GGUF/resolve/main/airoboros-l2-13b-gpt4-1.4.1.Q4_K_M.gguf
```

## Create embeddings
```
llmsearch index create -c sample_templates/obsidian_conf_test_rerank.yaml
```

## Run 
