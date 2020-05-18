### 열역학 - 열린계에서의 1법칙

## 질량 보존의 법칙과 에너지 보존 법칙

질량은 보존된다는 법칙은 자연계에서 직관적이고 명백해보인다.

아인슈타인의 특수 상대성 이론에 의해 도출된 식
$$
E=mc^2
$$
은 질량과 에너지가 상호 변환 할수 있다는 사실을 의미하며 에너지 보존법칙의 설명을 인용하면

```
기존에 있던 개념의 에너지가 보존되는 것 뿐만이 아니라 질량의 형태로 있는 에너지까지도 보존된다는 것이다. 다시 말해 질량 자체가 곧 에너지고 본질적으로 질량 보존의 법칙과 에너지 보존의 법칙은 같은 불변량에 대한 법칙이었다는 결론을 얻어냈다. 이로 인해 과학의 뿌리를 이루던 두 가지 큰 법칙, 질량보존의 법칙과 에너지보존의 법칙이 하나로 연결되게 되고, 두 뿌리가 하나로 합쳐져 더욱 견고한 토대를 이루게 되었다. 
```

출처 - https://ko.wikipedia.org/wiki/%EC%97%90%EB%84%88%EC%A7%80_%EB%B3%B4%EC%A1%B4_%EB%B2%95%EC%B9%99



그러므로 에너지와 질량은 본질적으로 같고 우리는 closed system이 아닌 물질이 오고가는 열린계에서의 열역학 1법칙을 적용하는 방법을 배울 것이다.

### 물질의 출입

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_14_u9ftv3.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/이미지_14_u9ftv3.png)

위 그림에서 미소 물질량 식을 만들어보자.
$$
\delta \dot V= V_ndA_c \quad (1)
$$
이때 $\delta$ 표시는 불완전미분,  경로를 알아야 하는 저번 시간에 배운 일,열, 질량유량과 같은 상태량을 말하고 d 와 같은 표시는 완전미분, 그냥 처음과 끝의 상태량이 중요한 단면적과 같은 property를 수식한다.
$$
\delta \dot m=\rho V_ndA_c
$$
양변 적분기호를 씌우면
$$
\dot m=\int_{A_c}\rho V_ndA_c \quad  (2)
$$
단면적이 일정한 관을 지난다고 가정할 때 $V_n$은 위치마다 다르다.

하지만 저러한 적분을 간단하게 근사화 시키는 방법은 존재한다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_15_fb8iuj.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/이미지_15_fb8iuj.png)

이 관의 유속의 평균 속도는 다음과 같이 구한다.
$$
V_{avg}=\frac{1}{A_c}(\int_{A_c}V_ndA_c)
$$
모든 단면적의 수직에 대한 통과 유량을 구한다음 단면적으로 나눠준다면 평균 속도가 나오게 된다.

물론 이러한 가정은 그 구간까지의 단면적이 일정해야한다.

또한 비압축성이라 가정하면 밀도도 적분식을 빠져나온다.
$$
\dot m=\rho V_{avg}A_c \quad (3)
$$
이렇게 가정을 통해 (2)식이  (3)식으로 예뻐진다.

또한 (1)식은 적분 시 다음과 같이 바뀐다.
$$
\dot V= V_{avg}A_c 
$$
그러므로
$$
\dot m=\rho \dot V=\frac{\dot V}{\nu}
$$ { }


### 방향성

여기서 방향성을 명확하게 짚고 넘어갈 것은 closed system에서의 열역학 1법칙이 열린계에서도 적용을 시켜서 현실세계에서의 열역학 1법칙을 도출해내는 것이 목적이다.

위에서 개념적인 질량유량에 대해서 알아보았다.

이러한 방식을 이용해 좀 더 일반적으로 적용 할 수 있는 열역학 1법칙을 도출해 나갈 것이다. 

### 질량보존의 법칙

$$
m_{in}-m_{out}=\Delta m_{cv}
$$

이를 시간으로 미분하면
$$
\dot m_{in} - \dot m_{out} = dm_{cv}/dt  \quad (4)
$$
control volume의 질량은 면적*미소비체적을 전체 CV에 적분해서 구할 수 있다.
$$
m_{cv}=\int_{cv} \rho dV
$$
(4)식을 표현하기 위해 위 식을 미분하면
$$
\frac{dm_{cv}}{dt}=\frac{d}{dt}\int_{cv}\rho dV
$$
(4)의 좌변항을 구하기 위해 임의의 Control volume 을 나타내보면

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_17_jfuivk.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/이미지_17_jfuivk.png)

수직 속도벡터를 표현하면
$$
V_n=Vcos\theta = \vec V \cdot \vec n
$$
처음에 구한 미소 질량유량
$$
\delta \dot m=\rho V_ndA = \rho(\vec V \cdot \vec n) dA
$$
이때 cos항의 각이 90도 이하이면 양수, 이상이면 음수이므로 출입을 표현할 수 있다.(조상님들은 위대하다.)

그러므로 질량보존의 법칙은 지금까지 구해온 식을 집어넣으면
$$
\int_{cv}pdV +\int_{cs}\rho(\vec V \cdot \vec n) dA = 0  \quad (5)
$$
**이때 두번째 항의 Control surface도 유념해서 보자! (표면상의 출입이므로)**

이를 다시 두번째 항을 쪼개서 정리하면
$$
\int_{cv}pdV =\sum_{in}\dot m-\sum_{out}\dot m
$$
사실 이 모든 일련의 과정은 (5)를 도출하기 위함이었으니 (5)식을 두번 보도록 하자.



### Stedy flow processes

steady flow란 $m_{cv}=constant$라는 의미이다.

그림으로 본다면 

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_18_hl3znr.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589774239/0518posting/이미지_18_hl3znr.png)

이렇게 $\dot m_{in}=\dot m_{out}$ 인 경우이다. (5)식에서 첫 항이 0이 된 경우이다.

간략하게 표현을 위해 1을 들어오는것, 2를 나가는 상태라 하면
$$
\dot m_{1}=\dot m_{2} \quad
$$
그러므로
$$
\rho_1V_1A_1=\rho_2V_2A_2
$$


### 비압축성 흐름

비압축성은 흐름에 따른 밀도가 변하지 않으므로
$$
V_1A_1=V_2A_2
$$


### 느낀점

우리는 (5)식을 위해 쉼없이 긴 이야기를 달려왔다.

사실 (5)식이 지금까지 한 얘기들과 앞으로 한 얘기들을 포괄한다고 생각한다.

그저 (5)식에 특수한 경우를 학습하거나 또는 전제 조건을 학습하거나인 것 같다.

이런 논리적 흐름에 따라 이론을 전개한 조상님들의 업적에 오늘도 감탄한다.





### 레퍼런스

[1] [https://ko.wikipedia.org/wiki/%EC%97%90%EB%84%88%EC%A7%80_%EB%B3%B4%EC%A1%B4_%EB%B2%95%EC%B9%99](https://ko.wikipedia.org/wiki/에너지_보존_법칙) 위키피디아 에너지 보존법칙

[2] Thermodynamics : An engineering approach - fith edition , YUNUS A. CENGEL - 교과서

