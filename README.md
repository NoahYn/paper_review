# paper_review
review of paper related machine learning 


23.08.01 - "Attention Is All You Need(2017)" : Attention mechanism and Transformer architecture

  생각해봐야 할 것.
    1. Positional encoding(PE)에서 512(d_model)개의 서로 다른 파장을 가진 sinusoid의 값을 PE vector로 사용하면, relative position보다는 absolute position처럼 작동하는 것 아닌가? 512개 파장의 최대공약수만큼의 주기로 벡터의 값이 돌아올텐데.. 어떻게 계산하지?
    2. sequence length n이 representation dimensionality d보다 작은 경우에 complexiry per layer에서 이점이 생기는데, 그럼 LLM에서는 restricted self-attention을 사용하는 건가?
    3. Architecture figure(Figure 1)에서 output은 SOS로 시작. decoder의 masked attention layer의 query와 encoder output의 key, value를 사용해 output을 추가. output 아래 shifted right는 무슨 뜻일까?
