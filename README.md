# paper_review

### 23.08.01 - Attention Is All You Need (GPT-API 스터디 발표)

  생각해볼 것들. 
  
  - Q1. Positional encoding(PE)에서 512(d_model)개의 서로 다른 파장을 가진 sinusoid의 값을 PE vector로 사용하면, relative보다는 absolute position처럼 작동하는 것 아닌가? 512개 파장의 최대공약수만큼의 주기로 벡터의 값이 돌아올텐데.. 어떻게 계산하지?
  - Q2. sequence length n이 representation dimensionality d보다 작은 경우에 complexiry per layer에서 이점을 얻는데, 그럼 LLM에서는 restricted self-attention을 사용하는 건가?
    - A2. GPT-3.5에서는 restricted를 사용하지 않고, 최대 입력 sequence 길이를 4096개 토큰 정도로 제한하는 방식을 사용함. 최대 길이보다 긴 sequence를 처리하는 경우에는 전체 sequence를 적절히 나누어 입력하는 식으로 학습시킴.
  - Q3. Architecture figure(Figure 1)에서 output 아래 (shifted right)는 무슨 뜻일까?
    - A3. decoder에서 모델이 예측을 시작할 땐 출력 sequence가 없는 상태에서 SOS로 시작하므로 오른쪽으로 한 칸씩 이동했다라고 이해함. 

### 23.08.08 - Reinforcement Learning Upside Down (Journal seminar 발표)

  생각해볼 것들. 

  - Q1. Command를 Semantic하게 사용할 수 있다면 정말 좋을텐데. Reward를 좀 더 복잡하게 설계한다면? (-> like Multiple reward or Vector reward) word embedding처럼, reward도 의미론적으로 embedding할 수 있을까?
