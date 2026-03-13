# proof-the-sorce-of-data-in-workshop3
data from training ai model in python env

so u need to run it in python DMLAP env（owned by Dr Irini karzani）----https://github.com/IriniKlz/DMLAP/tree/main/python/01-intro-to-python
，and must have jupyter notebook（this can be found in VSCODE）


To install convnext is not a easy thing to me because i met multiple techinical issues(i spent 3hours to dealing with this thing with the help of gpt),which make me unable to train this model for longer.(just train 1 hour).i have to ask gpt for help for many process of it.
So its important to try my best to let others know what CONDITION is required:

torch 2.5.1+cu121
CUDA 12.1
GPU 

STEP1-torch 2.5.1+cu121
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121

STEP2-
pip install "transformers==4.40.2"
TEST it--python -c "import torch, transformers; print(torch.__version__); print(transformers.__version__); print(torch.cuda.is_available())"

if it shows 
2.5.1+cu121
4.40.2
True
it will be good


STEP3-
pip uninstall torch torchvision torchaudio -y
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121
Update pytorch to 12.1


if all are good,print these:
import torch

device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
model.to(device)

print("Using device:", device)



【if all these are nonsense....ASK GPT(OMG I CANT BELIEVE I HAVE TO SAY THAT)】
