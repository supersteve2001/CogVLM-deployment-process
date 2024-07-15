# CogVLM-deployment-process
The CogVLM deployment process is documented here。 Here you can find how to do model deployment and inference.

Open source link:https://huggingface.co/THUDM/cogvlm2-llama3-chinese-chat-19B

Firstly, don't forget to install conda.

Create conda environment,
```
conda create -n cogvlm python=3.11 -y
source activate cogvlm
```

Install torch torchvision torchaudio
```
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

Install cuda-runtime
```
conda install -y -c  cuda-runtime
```

Install the CogVLM dependency library， you can find it in: https://github.com/THUDM/CogVLM2/blob/main/basic_demo/requirements.txt
```
pip install -r requirements.txt
```
Run the inference of the model，
```
python deo.py
```
```
pip install accelerate
```





Some questions to solve:
```
AttributeError: 'str' object has no attribute 'shape'
```
solution: downgrade transformer lib to 4.40
