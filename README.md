# paper_review

### 23.08.01 - Attention Is All You Need (GPT-API 스터디 발표)

  생각해볼 것들. 
  
  - Q1. Positional encoding(PE)에서 512(d_model)개의 서로 다른 파장을 가진 sinusoid의 값을 PE vector로 사용하면, relative position보다는 absolute position처럼 작동하는 것 아닌가? 512개 파장의 최대공약수만큼의 주기로 벡터의 값이 돌아올텐데.. 어떻게 계산하지?
  - Q2. sequence length n이 representation dimensionality d보다 작은 경우에 complexiry per layer에서 이점이 생기는데, 그럼 LLM에서는 restricted self-attention을 사용하는 건가?
  - Q3. Architecture figure(Figure 1)에서 output 아래 (shifted right)는 무슨 뜻일까?
    - A3. decoder에서 모델이 예측을 시작할 땐 출력 sequence가 없는 상태에서 SOS로 시작하므로 오른쪽으로 한 칸씩 이동했다라고 이해함. 
