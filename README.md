# paper_review

### 23.08.01 - Attention Is All You Need (GPT-API 스터디 발표)
https://arxiv.org/abs/1706.03762

  생각해볼 것들. 
  
  - Q1. Positional encoding(PE)에서 512(d_model)개의 서로 다른 파장을 가진 sinusoid의 값을 PE vector로 사용하면, relative보다는 absolute position처럼 작동하는 것 아닌가? 512개 파장의 최소공배수만큼의 주기로 벡터의 값이 돌아올텐데.. 어떻게 계산하지?
  - Q2. sequence length n이 representation dimensionality d보다 작은 경우에 complexiry per layer에서 이점을 얻는데, 그럼 LLM에서는 restricted self-attention을 사용하는 건가?
    - A2. GPT-3.5에서는 restricted를 사용하지 않고, 최대 입력 sequence 길이를 4096개 토큰 정도로 제한하는 방식을 사용함. 최대 길이보다 긴 sequence를 처리하는 경우에는 전체 sequence를 적절히 나누어 입력하는 식으로 학습시킴.
  - Q3. Architecture figure(Figure 1)에서 output 아래 (shifted right)는 무슨 뜻일까?
    - A3. decoder에서 모델이 예측을 시작할 땐 출력 sequence가 없는 상태에서 SOS로 시작하므로 오른쪽으로 한 칸씩 이동했다라고 이해함. 

### 23.08.08 - Reinforcement Learning Upside Down (Journal seminar 발표)
https://arxiv.org/abs/1912.02875

  생각해볼 것들. 

  - Q1. Command를 Semantic하게 사용할 수 있다면 정말 좋을텐데. Reward를 좀 더 복잡하게 설계한다면? (-> like Multiple reward or Vector reward) word embedding처럼, reward도 의미론적으로 embedding할 수 있을까?
  - Q2. 유명한 저자의 주목할만한 논문임에도 인용수가 굉장히 적다. 왜일까?

### 23.08.10 - Reinforcement Learning in a Neurally Controlled Robot Using Dopamin Modulated STDP (SNN study 발표)
https://arxiv.org/abs/1502.06096

  - Eligibility Traces, synaptic tag, Dual-path model의 개념에 대해 더 자세히 찾아보고 이해하기.

### 23.08.25 - Spiking Denoising Diffusion Probabilistic Models
https://arxiv.org/abs/2306.17046

  - Residual connection을 spiking block에 적용하기 위해 structure 순서를 바꾸는 발상이 재미있었다.

### 23.08.29 - RepVGG : Making VGG-style ConvNets Great Again
https://arxiv.org/abs/2101.03697

  - 시계열 예측 모델에 사용하기 위해 1D + submodule로 수정함 -> https://github.com/NoahYn/Conv1d_Modules/tree/main
  - 저자 레포를 확인하면 Structural Reparameterization technic을 VGG 외에도 많이 적용하고 있는데, 특히 RepLKNet이 흥미로웠다.(https://github.com/DingXiaoH/RepLKNet-pytorch)
  - 트레이닝 시 브랜치 효과를 극대화하기 위해 ReLU같은 비선형 레이어를 퓨징하는 방법은 없을까? 
