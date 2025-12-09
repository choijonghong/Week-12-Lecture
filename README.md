# Week-12-Lecture
Week-12-Lecture

### 역전파는 어떻게 AI의 암흑기를 끝내고 딥러닝의 시작을 열었는가?
* 논문명: Learning representations by back-propagating errors”(Rumelhart, Hinton, Williams, 1986)

### 논문배경
* 당시 신경망은 입력과 출력만 연결한 구조에서만 학습이 가능했다.
    * ‘정답만 맞추는 연습’은 할 수 있었지만, ‘생각하는 과정’을 배우는 기능은 없었습니다.
* Hidden Layer가 추가되면 그 내부를 학습시키는 방법이 없었다.
    * 옛 신경망은 ‘정답’은 가르칠 수 있었지만, ‘생각 과정’을 어떻게 고쳐야 할지 알려줄 방법이 없었습니다.
* 기존 학습 규칙(예: 퍼셉트론)은 입력–출력 연결 강도만 조정할 수 있었다.
* 이로 인해 모델이 스스로 중간 개념을 배우는 표현 학습이 불가능했다.
* 본 논문은 Hidden Layer까지 학습 가능한 새로운 학습법 제안을 목표로 출발했다.

### 기존 연구의 한계점
* 당시 신경망은 ‘답만 외우는 학생’과 같아서, 생각하는 과정과 개념 만들기는 불가능했다.
* 중간에 어떤 생각 과정을 거쳤는지 확인할 수 없었다.
* 복잡한 문제를 단순 기준으로만 해결하려 했다.
* 스스로 새로운 아이디어나 특징을 만들지 못했다. 즉 사람이 알려주지 않으면 특징을 발견하지 못했다.

### 논문 목표
* Hidden Layer가 스스로 표현을 구축하도록 하는 학습 방법을 만드는 것이 목표다.
* 단순하면서도 다양한 다층 신경망에 적용 가능한 일반적 알고리즘을 제시하는 것이 목표다.

### 논문내용(주요 혁신 및 방법론)  :출력 오차를 역방향으로 전파하여 각 weight의 기여도를 계산하는 알고리즘
* Forward pass: 한 번 앞으로 계산해서 예측값을 만든다.
 <img width="768" height="190" alt="image" src="https://github.com/user-attachments/assets/4c1d47c1-21b8-4f39-b233-1acfac103f7f" />

* Backward pass: 오차를 뒤로 전달하며, 각 연결이 얼마나 잘못됐는지 미분으로 계산한다.
 <img width="830" height="250" alt="image" src="https://github.com/user-attachments/assets/a3c5a91a-b057-46c7-abd4-cf4be13cbd38" />

* Gradient descent 업데이트: 그 정보를 바탕으로 모든 weight를 오차가 줄어드는 방향으로 조금씩 고친다.
<img width="771" height="469" alt="image" src="https://github.com/user-attachments/assets/1015bcea-7347-4966-9f32-a89cfb6d0fc3" />

### 기여도 및 결과
* VAE 덕분에 AI는 단순히 있는 것을 분류하는 것을 넘어, 없는 것을 만들어내는(Generative) 능력을 갖게 되었습니다.
* 새로운 창작: 세상에 없는 사람 얼굴, 본 적 없는 풍경을 그려냅니다.
* 보간 (Interpolation): 웃는 얼굴과 우는 얼굴 사이의 **'중간 표정'**을 자연스럽게 만들어냅니다. (설계도 상에서 부드럽게 이동)
* 복원: 노이즈가 낀 사진을 보고 깨끗한 원본 설계도를 추측해 복구합니다.


### 참고 파일

* 논문1. Learning representations by back-propagating errors
