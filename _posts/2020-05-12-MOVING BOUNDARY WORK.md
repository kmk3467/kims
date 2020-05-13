```
---
published: true
layout: single
title: "MOVING BOUNDARY WORK"
category: post
tags: Thermal
comments: true
use_math: true
---
```

# 4-1 MOVING BOUNDARY WORK

첫 포스팅은 열역학에 대한 포스팅으로 시작합니다.

### 역학적 일의 정의 

역학적 일은 실질적으로 팽창과 수축에 의해 결정되는 경우가 있는데 이러한 팽창과 수축 일을 **MOVING BOUNDARY WORK**라고 부른다.수식으로는 **P** *dV* 라고 한다.

주로 자동차엔진의 가스폭발에 의해 피스톤이 움직이며 일을 하게 되는데, 이는 열역학적으로 완전히 결정 될 수 없다. 왜냐하면 실제로 매우 빠른 속도로 진행되기 때문에 내부에 가스가 평형상태로 유지된다고 볼 수 없기 때문이다.

이러한 이유로 시스템의 상태를 정확히 묘사할 수 없고, 이는 시스템 경로를 추적할 수 없게된다. 그러므로 일은 Path가 알 수 없는 함수가 되는 것이다. 우리는 이를 알기 위해 Path에 관한 정보가 있어야 한다. 

### 전제조건

우리는 편의상 이동일을 ***quasi-equilibrium process***에서 분석 할 것인데, 이 상태는 모든 시간에서 거의 평형을 유지한다.라고 가정하는 것이다. 이유는 모델링을 단순화 하기 위함이다. 이러한 상태는 실제 엔진에서 피스톤이 느린 속도로 움직이는 것이다.이런 조건에서 일의 output은 최대가 되고 input은 최소가 되는 최대효율 상태가 된다.

여기까지 우리가 알 수 있는 것은 역학적 일에서 팽창과 수축일을 하는 MOVING BOUNDARY WORK가 존재하며 이를 측정하기 위한 전제는 항상 ***quasi-equilibrium process***라고 가정한다. 그렇게 함으로써 최대의 효율을 가지며, 일의 path를 알 수 있기 때문이다.

### 피스톤에서의 일의 정의

$$
\delta W_{b}=Fds=PAds=PdV    \quad\quad\quad\quad\quad\quad\quad                                (4-1)
$$

일에 정의에 의해 미소일은 F*ds 이며 이를 피스톤에 적용할 시 F=P*A 이고, A는 피스톤의 단면적이라 할때 Ads는 피스톤이 움직인 부피로 계산된다. 그러므로 일의 정의에 의해 이동일은 PdV로 4-1처럼 정의된다. 

이때 P는 절대압력이며, 항상 양수이다. 그러므로 부피의 변화량에 따른 일의 부호변화가 생기는데 부피가 커질때는 dV가 양수이므로 피스톤안의 시스템이 외부로 일을  때 양의 일을 하며, 부피가 작아질때 dV가 음수이므로 피스톤안의 시스템이 외부로부터 일을 받을 때 음의 일을 한다.

일의 최종 양은 다음과 같의 정의된다.
$$
W_b=\int_{1}^{2}PdV  \quad \quad \quad \quad \quad \quad(4-2)
$$
이는 4-1의 미소일을 더한것이다.

### P-V다이어그램의 존재의의 - 왜 ?

우리가 이를 계산하기 위해서는 P와 V와의 관계 즉 
$$
P=f(V) \text{가 명확해야 이를 계산해 낼 수 있다.}
$$
<img src="[https://res.cloudinary.com/dbzvbzksw/image/upload/v1589343843/200513posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_1_glq30i.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589343843/200513posting/이미지_1_glq30i.jpg)">

위 그림을 보면 1->2로 상태가 변할 때 P는 미소 V를 변할 때 곡선형태로 변하고 이를 수식적으로 계산하기 위해서는 x축과 y축의 함수관계가 드러나야 한다. 그렇다면 분홍색 영역의 dA가 미소일이 된다.
$$
A=\int_{1}^{2}PdV  \quad \quad \quad \quad \quad \quad(4-2)
$$
P-V 다이어그램안에서 미소일을 모두 적분하면 위 그림에서의 Area A는 일이 된다. 물론 이 결론에는 ***quasi-equilibrium process***라는 전제와 *Closed System* 이라는 전제가 있어야 한다.

### 경로함수로서의 일

<img src=[https://res.cloudinary.com/dbzvbzksw/image/upload/v1589343844/200513posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_2_bzgjjj.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589343844/200513posting/이미지_2_bzgjjj.jpg)>

우리는 위에서 일의 경로를 알기 위해 ***quasi-equilibrium process***이라는 전제를  하였다. 위의 A,B,C 곡선은 모두 4-2에서 정의한 바에 의하면 일이 모두 다르다. 그리고 이 일의 크기는 1->2로 이동할 때 어떻게 이동했냐에 의존한다. 만일 path function이 아니었다면 일을 생성해내는 cyclic device가 생성되지 못했을 것이다. 시작점에서 끝점으로 돌아오는 일련의 행위를 Cycle이라 하는데 적분의 성질에 의해위 그림은 에너지를 소모하고 에너지를 얻는다. 이 얻은 에너지양과 소모한 에너지 양의 차를 net work라 하고 사이클 경로상의 내부 넓이가 된다.

물론 항상 P와 V의 함수가 수식적으로 정의될 수는 없고 실험적으로 정의되기도 한다. 이때 우리는 그 넓이를 계산해 줄 수 있다. (다양한 툴을 통해서)

### 전제를 벗겨내자

4-2의 식을 다시 살펴보자
$$
A=\int_{1}^{2}PdV  \quad \quad \quad \quad \quad \quad(4-2)
$$
여기서 P는 ***quasi-equilibrium process***상태에서 상정된 것이므로 바운더리쪽의 압력은 내부 가스와 압력이 같아진다. 하지만 항상 ***quasi-equilibrium process***을 가정할 순 없다.  매번 달라지기 때문이다. 그러므로  ***nonquasi-equilibrium process***에서 생각해볼때 P는 모든 곳에서의 압력이 다르다.


$$
A=\int_{1}^{2}P_{i}dV \quad\quad\quad\quad\quad\quad\quad (4-3)
$$
그러므로 4-3처럼 정의 되어야 한다. 이 과정은 자동차엔진에서 팽창과정이나 수축과정에서 진행되는 일이고, 에너지는 보존되기 때문에 이를 제외한 일도 반드시 존재한다. 예를 들면 자동차 엔진에서 뜨거운 가스가 팽창할 때 피스톤과 실린더사이의 마찰을 극복해야 하는데 일을 쓰이기도 하고, 대기압을 극복해내는데, 크랭크를 회전시키기 위해 일이 쓰이기도 한다.

그러므로 실제일은
$$
W_{b}=W_{friction}+W_{atm}+W_{crank} = \int_{1}^{2}(F_{friction}+P_{atm}A+F_{crank})dx 
$$
로 바뀔 수 있다. 여기서 중요한 것은 시스템이 실제로 일을 받은 일은 마찰력을 극복하고, 대기압을 극복하고, 크랭크를 회전시키는 일과 같아야 한다는 것이다. (에너지 보존 법칙) 

전제를 벗겨냄으로써 **MOVING BOUNDARY WORK**가 항상 ***quasi-equilibrium process***를 전제하고 있지는 않다는걸 확인 할 수 있다.