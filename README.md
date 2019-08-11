# 네이버 영화 평점 데이터로 자연어처리 논문 구현 시작하기 (2019 PyCon Kr Tutorial)

NLP 논문을 구현할 때, 항상 수반하는 전처리(Vocabulary, Tokenizer, Embedding, etc)등의 개념을 소개하고, 이를 효율적으로 처리하는 코드와 논문 구현을 위한 project template 구성 방법을 소개합니다. 소개한 내용을 토대로 PyTorch와 NSMC (Naver sentiment movie corpus) 데이터셋을 이용 분류 문제와 관련된 아래의 논문을 구현하며, 논문 구현 방법론을 체득합니다.

### Contents
+ 10:00 ~ 10:50 : NLP 논문 구현을 위한 전처리, Project template 소개
	1. [Structuring your first NLP project.pdf](https://github.com/aisolab/strnlp/blob/master/materials/190815_Structuring%20your%20first%20NLP%20project.pdf)
+ 11:00 ~ 12:20 : 구현 관점에서의 "Convolutional Neural Networks for Sentence Classification" 리뷰 및 모듈 구현 (실습)
	1. [eda.ipynb](https://nbviewer.jupyter.org/github/aisolab/strnlp/blob/master/exercise/eda.ipynb) : 텍스트 데이터에 대한 탐색적 데이터 분석에 대한 실습
	2. [build_vocab.ipynb](https://nbviewer.jupyter.org/github/aisolab/strnlp/blob/master/exercise/build_vocab.ipynb) : 텍스트 데이터 전처리를 해보는 실습
	3. [model.data.ipynb](https://nbviewer.jupyter.org/github/aisolab/strnlp/blob/master/exercise/model.data.ipynb) : 딥러닝 모델의 data pipeline을 구축해보는 실습
	4. [model.ops.ipynb](https://nbviewer.jupyter.org/github/aisolab/strnlp/blob/master/exercise/model.ops.ipynb) : 딥러닝 모델을 구현함에 있어서 각종 operation을 구현해 보는 실습
	5. [model.net.ipynb](https://github.com/aisolab/strnlp/blob/master/exercise/model.net.ipynb) : 전체 딥러닝 모델을 구현한 operation을 바탕으로 구현해보는 실습
+ 12:30 ~ 13:00 : Model Training and Test, QnA

### Preliminary
PyTorch가 처음이거나 예제로 구현하는 논문을 처음 접하시는 분들은 아래의 두 가지를 미리 공부하고 오시면 더 유익할 것 같습니다.

##### PyTorch
+ [What is torch.nn really?](https://pytorch.org/tutorials/beginner/nn_tutorial.html#what-is-torch-nn-really)
+ [Data loading and Processing Tutorial](https://pytorch.org/tutorials/beginner/data_loading_tutorial.html#data-loading-and-processing-tutorial)
+ [Saving and Loading Models](https://pytorch.org/tutorials/beginner/saving_loading_models.html#saving-and-loading-models)

##### Paper 
+ [Convolution Neural Networks for Sentence Classification](https://arxiv.org/abs/1408.5882)

### Tutorial이 유익하실 분들
- 논문 구현을 project template 토대로 구현한 경험이 없으신 분들
- 논문 구현에 관심있으신 분들
- 자기자신만의 project template 구성에 관심있으신 분들
- NLP 논문 구현에 관심있으신 분들

### Tutorial이 유익하지 않으실 분들
- 이미 사용하고 계신 project template이 있으신 분들
- 전문적인 딥러닝 개념을 듣고 싶으신 분들

### Reference
- [nlp_implementation](https://github.com/aisolab/nlp_implementation)
