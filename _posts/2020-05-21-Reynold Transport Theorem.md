# 유체역학

## 레이놀즈수송정리

일상생활에서 유체의 움직임을 분석할때의 두가지 관점에 대해 제시한다.

첫번째는 시스템의 경계가 없어 질량이 이동하면 그 만큼 컨트롤 볼륨도 커지는 것, 질량은 유지된다. (system approach)

둘째는 시스템의 경계가 존재해서 질량이 이동하더라도 컨트롤 볼륨은 그대로인것. (conrol volume approach)



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589972449/200520posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_3_sq6izr.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589972449/200520posting/이미지_3_sq6izr.png)



이는 고체역학을 기반으로 한 대부분의 법칙을 사용하는 유체역학과 (systems) Control volume을 이용하여 표현하는게 편한 유체역학 사이의 연결점을 Reynolds transport theorem(RTT)에서 제공한다.

도대체 RTT를 왜 사용해야 하는 것인가? 위의 그림을 보자

스프레이가 분사됨에 따라 스프레이의 질량이 스프레이캔을 벗어나 분사될것이다.

그렇다면 CV는 분사된 질량의 영역까지 확장되어야하는가? 또는 스프레이 캔인채로 유지되어야하는가?

이러한 시스템 내부의 extensive property의 시간변화량과 control volume의 관계식을 RTT가 제공한다.



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589972889/200520posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_4_sh3ekz.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589972889/200520posting/이미지_4_sh3ekz.png)

간단한 예제를 통해 일반화시켜보도록 하자



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589973031/200520posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_5_agmu5l.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589973031/200520posting/이미지_5_agmu5l.png)



다음과 같은 시스템과 CV가 존재한다.

(1)과 (2)사이에서 CV는 고정된다. 

초기 시간 t에는 시스템과 CV가 같다.000000000-----------------------------------------------------------------------------------------------------------------------------------------------------------------------0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   
$$
\Delta t
$$
가 흐른 후 system은 II의 영역만큼 이동한다.

이는 CV-I+II(단순한 넓이계산) 영역으로 이동하게 된다. 하지만 CV는 공간에 고정되있으므로 항상 유지된다.

extensive property인 B를 고려해보자

B를 무게로 나눠주면 intensive property가 된다.


$$
b=B/m
$$
마찬가지로 아까의 상황처럼 


$$
B_{sys,t}=B_{CV,t} \quad (1)
$$


t일때 CV와 system은 같은 장소에 존재한다.


$$
B_{sys,t+\Delta t}=B_{CV,t+\Delta t}-B_{I,t+\Delta t}+B_{II,t+\Delta t} \quad (2)
$$


$\Delta t$의 시간이 지났을 때는 위 상황과 같다. (위에서 예제를 들었던 상황과 같은 상황이다.)

(2)-(1)을 빼서 $\Delta t$로 나눠주면 변화량 형태가 된다.


$$
\frac{B_{sys,t+\Delta t}-B_{sys,t}}{\Delta t}=\frac{B_{CV,t+\Delta t}-B_{CV,t+\Delta t}}{\Delta t}-\frac{B_{I,t+\Delta t}}{\Delta t}+\frac{B_{II,t+\Delta t}}{{\Delta t}}
$$



이때 유념할 것은 I는 들어오는 질량 II는 나가는 질량이다. 위 그림을 참조하면 이해가 편하다.

이를 
$$
\Delta t - >0
$$
으로 가면

들어오고 나가는 질량에 대해 미소시간으로 측정한다면 미소시간당 출입질량이 될 것이다.


$$
\frac {dB_{sys}}{dt}=\frac {dB_{CV,t+\Delta t}}{dt}-\dot B_{in}+\dot B_{out} \quad (3)
$$


이는 이렇게 정리된다.


$$
\frac {dB_{sys}}{dt}=\frac {dB_{CV,t+\Delta t}}{dt}-\rho_1 b_1A_1V_1+\rho_2 b_2A_2V_2
$$


이를 일반화 하기 위해서는 전 시간에 질량유량이 들어오기 위해 속도벡터와 수직벡터를 내적한 방법을 써야한다.

또한 실제 inlet과 outlet은 여러 군데이므로 단위면적으로  해주어야 한다.

기본적으로 이 포스팅에서는 나가는 방향을 n벡터의 전제로 한다.


$$
\int_{CS}\rho_i b_iA_i(\vec V_i\cdot\vec n)dA =\sum_{out}\dot B-\sum_{in}\dot B
$$


이때 각이 90도 아래이면 양수이므로 나가는 것이고 90도 위이면 들어오는 것이므로 위의 식이 자동 계산된다.

위 식 (3)에서 해결안된 항 CV에 대해 알아보자


$$
B_{CV}=\int_{CV}\rho b dV
$$


컨트롤 볼륨내의 B의 양은 다음과 같다.

이를 시간에 대해 미분하면


$$
\frac {dB_{CV}}{dt}=\frac{d}{dt}\int_{CV}\rho b dV
$$


다시  (3)식을 정리하면


$$
\frac {dB_{sys}}{dt}=\frac{d}{dt}\int_{CV}\rho b dV +\int_{CS}\rho_i b_iA_i(\vec V_i\cdot\vec n)dA \quad (4)
$$


이는 위에서 개념화 한것과 같이 CV가 고정되 있을 때의 RTT 관계식이다.

CV는 시간에 따라 변형되거나 이동하지 않으므로 오른쪽 식의 첫번째 항은 미분을 먼저해도, 또는 적분을 먼저 해도 관계가 없다.

시간에 전혀 무관하기 때문이다.

그러므로 미분식을 넣을 수 있다.

하지만 주의할 점은 미분을 넣으면서 밀도와 b는 위치에 따라 상태량이 변할 수 있으므로 t에 대한 함수만은 아니다.

그러므로 편미분으로 바뀌어야한다. 결론적으로


$$
\frac {dB_{sys}}{dt}=\int_{CV}\frac{\partial (\rho b) }{\partial t}dV +\int_{CS}\rho_i b_iA_i(\vec V_i\cdot\vec n)dA
$$


### CV가 이동한다면



하지만 CV이 이동하는 기계도 존재한다. 예를들면 터빈이나, 프로펠러 등이다. 

이러한 기계는 이동하는 CV의 CS를 고려해주어야한다.

이러한 식을 표현해주기 위해서 상대속도를 도입 할 수 있다.

이러한 상대속도로 표현해 주지 않는다면 CS의 이동속도가 물질이 나가는 속도보다 빠르다면

위 식은 완전히 틀린 식이 된다.

그러므로 상대속도를 정의해주면


$$
\vec V_r =\vec V - \vec V_{CS}
$$


![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589986160/200520posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_6_qlusaj.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589986160/200520posting/이미지_6_qlusaj.png)





이 식으로서 이동하는 CS를 고려하는 일반식을 도출해낼 수 있다.


$$
\frac {dB_{sys}}{dt}=\frac{d}{dt}\int_{CV}\rho b dV +\int_{CS}\rho_i b_iA_i(\vec V_r\cdot\vec n)dA
$$


<u>이 또한 CV의 적분식이 미분항과 관계가 없게 만든다면 순서를 바꾸어도 성립한다.</u> 

<u>어떻게? 바로 움직이는 CV자체를 fixed frame으로 보면 된다.</u>

<u>그렇다면 적분과 미분사이의 관계성이 없어진다</u>

(**다시 확인 할 것)**
$$
CV가 \ 이동할때의 \ RTT
\\
\frac {dB_{sys}}{dt}=\int_{CV}\frac{\partial (\rho b) }{\partial t}dV+\int_{CS}\rho_i b_iA_i(\vec V\cdot\vec n)dA
$$


이때 CS의 상대좌표 개념이 없어진다는 점이다.

왜냐하면 우리는 이동하는 CV를 절대좌표로 인식하고 있기 때문이다.



### Steady flow일때

B라는 property가 dt라는 시간동 변화가 없다면 다음과 같이 간략화된다.


$$
\frac {dB_{sys}}{dt}=\int_{CS}\rho_i b_iA_i(\vec V_r\cdot\vec n)dA
$$








### 레퍼런스

[1] Fluid Mechanics 3rd Edition, Yunus A. Cengel