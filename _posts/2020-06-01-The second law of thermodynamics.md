# 열역학 제 2법칙

## 2법칙은 무엇인가

우리는 앞서 1법칙 에너지 보존의 법칙을 배웠다.

이러한 법칙으로 모든 열 현상을 설명하긴 부족하다.

이로 인해 2법칙을 만들 필요가 존재했다.

2법칙이란 다음과 같은 현상으로 설명된다.

뜨거운 커피를 상상해보라

커피가 차가운 방에 놓여있다고 상상하면 그 커피는 시간이 지날 수록 차가워 질것이다.

즉 방으로 열전도가 진행될 것이다.

하지만 그 반대의 상황은 가능한가?

이러한 관찰에서, 열은 특정한 방향으로 흐르고 그 역의 방향으로는 흐르지 않는다.



### RESERVOIR

 열역학 2법칙을 정의하기 위해 RESERVOIR라는 개념을 끌어올 필요가 있다.

이는 거대한 에너지 덩어리이다. 예를 들면 대기나, 거대한 강과 같은 곳이다.

이러한 곳에서의 온도가 20도라고 가정한다면 내가 100도의 공기를 미세하게 넣는다하더라도

이 전체 공기의 온도는 변하지 않는다. 

RESERVOIR의 용량이 압도적으로 크기 때문이다.

이러한 큰 에너지원을 RESERVOIR라고 한다.



### HEAT ENGINE

열을 유용한 에너지로 바꾸어주는 장치를 일컬어 HEAT ENGINE이라고 한다.

열역학 자체도 인간이 유용하게 열을 사용하기 위해 만들어낸 규칙이므로

우리는 이러한 HEAT ENGINE에 집중할 필요성이 있다.

이러한 히트엔진의 공통점들이 존재하는데

1. 높은 열원에서 열을 받는다.
2. 일부를 일로 변환한다.
3. 남은 열을 낮은 열원으로 버린다.
4. 이러한 과정으로 cycle을 운용한다.



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011096/0601posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_2_v4f8at.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011096/0601posting/이미지_2_v4f8at.jpg)
$$
W_{net,out}=W_{out}-W_{in}
$$


이 히트엔진시스템은 우리가 CLOSED SYSTEM으로 배운것과 같이 바뀔 수 있다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011362/0601posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_3_m26bnf.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011362/0601posting/이미지_3_m26bnf.jpg)



이 내부의 CYCLE은 CLOSED SYSTEM으로 해석 가능하다.

이때 
$$
W_{net,out}=Q_{in}-Q_{out}
$$


이러한 기계장치의 효율을 다음과 같이 정의한다.


$$
Thermal\ efficiency=\frac{Net\ workoutput}{Total \ heat \ input}
$$


이는 일반적인 기계장치에서의 정의인 입력대비 출력에 부합하는 정의이다.



### 우리는 왜 Q_{out}을 아끼지 않는가

예를 들어 우리는 100KJ의 열을 받아서 20KJ의 일을 발휘했다고 하자

이후 80KJ의 열을 낮은 열원으로 버리지 않고 아낀다면 100%의 효율을 낼 수 있지않겠는가?

아쉽지만 불가능하다. 왜냐하면 이 80KJ의 열을 20KJ의 일을 발휘하는데 썼으므로 

높은 열원보다 낮아져 있는 온도 상태이므로 이러한 열들은 높은 열원으로 다시 돌아갈 수 없다.

열은 특정방향으로 흐르며 높은온도에서 낮은 온도로 흐르기 때문이다.



### Kelvin-Planck statement



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011973/0601posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_4_leq9fg.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591011973/0601posting/이미지_4_leq9fg.jpg)



이는 다음과 같이 서술된다.

하나의 열원으로부터 열을 받아 넷일을 만들고 사이클을 도는 기계장치는 존재하지 않는다.

이 말은 즉 두개의 열원이 존재해야 하며 하나의 열원으로 열을 버리므로

효율이 100%인 heat engine은 존재할 수 없다.



### 냉동기

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591012229/0601posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_5_wk5fgz.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591012229/0601posting/이미지_5_wk5fgz.jpg)



냉동기는 우리가 생각하는 방향과 반대로 작동한다. 

낮은 열원에서 열을 받아서 높은 열원에서 열을 버린다.

이러한 점은 낮은 열원에서 냉매가 외부온도보다 차갑게, 

그리고 이러한 냉매들이 압축기를 통해 높은 열원보다 뜨겁게 세팅한다면 가능하다.

다만 이러한 기계장치가 작동하려면 일을 공급받아야 하며, 일을 만들어 내지는 못한다.

입력받은 열의 양보다 출력하는 열의 양이 더 크기 때문이다.

이러한 냉동기의 효율을 COR이라하는데 다음과 같이 정의한다.


$$
COR_{R}=\frac{Q_L}{W_{net,in}}
$$


즉 목적에 따라 다르다. 내가 어떤 일을 입력해서 목적한 바 낮은 열원의 열을 얼마나 뺏어갔느냐가

냉동기의 목적이기 때문이다.

이러한 COR은 1보다 크다.



### 히트펌프

히트펌프는 단지 냉동기를 거꾸로 동작시키는 것이라 볼 수 있다.

냉동기가 낮은 열원에서 열을 가져와 높은 열원으로 버리는 것이라면,

반대로 히트펌프는 낮은 열원에서 열을 가져와 높은 열원으로 버리는 것은 맞으나,

목적 자체가 낮은 열원이 아닌 높은 열원의 온도상승을 기대하는 것이다.

즉


$$
COP_{HP}=\frac{desired\ output}{required\ input}=\frac{Q_H}{W_{net,in}}
$$


### Clausius statement

열역학은 두 가지 서술법이 존재한다.

이 중 한가지가 kelvin-plank 서술법이며 나머지 하나가 clausius statement 이다.

이는 다음과 같다.



**사이클에서 작동하는 장치가 아무런 입력 없이 낮은 열원에서 높은 열원으로 열을 전도할 수 없다.**



이는 우리가 앞서 말한 열의 방향성에서 실험적으로 발견된 내용이다.

그리고 또한 입력이 존재한다면, 앞서 말한 냉동기의 방식으로 낮은 열원에서도 높은 열원으로 열을

전도할 수 있는 방법 또한 배울 수 있었다.



### 두 서술법의 관련성

이 둘 중 하나만 어겨도 나머지 하나를 어기는 것과 같은 이 두가지는 동치관계이다.

이게 무슨 말도안되는 소리인가.

전혀 말이 안되보이지만 말이 된다.



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591013150/0601posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_6_b0v7xl.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591013150/0601posting/이미지_6_b0v7xl.jpg)



첫 째로 plank  서술에 의해 하나의 열원에서 넷일을 만들 수 있는 장치가 있다고 가정하자.

이는 plank  서술을 위반하였다. 열을 버리지 않으니 100% 효율을 가질 것이다.

즉 입력이 출력과 같아지며 이는 즉 그림의 왼쪽과 같이 clausius 서술까지 어기는 결과이다.



만약 clausius 서술이 어겨진다면, 굳이 낮은 열원에 열을 버릴 필요가 없으므로 이 또한 plank  

서술을 위반하는 결과이다. 그러므로 이 둘의 관계는 동치이다.





### 레퍼런스

[1] Thermodynamics : An engineering approach - fith edition , YUNUS A. CENGEL - 교과서

