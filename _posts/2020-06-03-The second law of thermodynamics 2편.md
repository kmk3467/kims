# 열역학 제 2법칙

## REVERSIBLE AND IRREVERSIBLE PROCESS

REVERSIBLE PROCESS는 원래 상태로 돌아올 수 있는 상태를 의미한다.

시스템과 주위가 어떤 과정을 거쳤을 경우 그 처음의 상태대로 돌아올 수 있다면 이를 REVERSIBLE PROCESS라 한다.

이는 시스템과 주위의 열교환과 일교환이 합쳤을 때 0이 되는 상태이다.

이러한 과정은 자연계에서 존재하지 않는다.

그렇다면 왜 우리는 그러한 과정을 정의해야 하는가?

<u>첫째로 분석하기가 쉽고, 둘째로 실제 과정과 비교가능한 이상화된 모델을 제공하기 때문이다.</u>



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591163870/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_1_ggiqbu.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591163870/0603posting/이미지_1_ggiqbu.jpg)

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591163870/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_2_ig8pvj.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591163870/0603posting/이미지_2_ig8pvj.jpg)



위 그림과 같이 평형이 유지되며 천천히 변화해야 REVERSIBLE PROCESS라 할 수 있다.



### Irreversibilities



비가역성에는 가장 대표적인 예로 **마찰**이 존재한다. 상대속도를 극복하기 위해 필요한 마찰력은 일을 소모해서

열을 만들어내는데 이렇게 소모된 열은 표면을 뜨겁게 달군다. 하지만 원래 상태로 돌아갈 때 이 표면은 차가워지는가?

그렇지 않다. 여전히 뜨겁고 또 마찰을 극복하기에 더 뜨거워진다.

그리고 열은 일로 완전히 변환되지 않는다.(열역학 2법칙)

그렇기에 과정이 진행된 후 원래 상태로 돌아 갈 수 없다.



**또 다른 예로는 Unstrained expansion of a gas 이다.**

**위의 사진 6-33 (c)에 나와있듯이 가스가 분출되며 팽창할 것이다.**

**이때 1->2 과정에서 가스는 일을 했고 압력이 낮아졌기에 온도는 내려갔을 것이다.**

**이러한 상태를 2->1로 돌리기 위해 압축을 한다면 가스에는 일을 입력받아야 하고 에너지 평형에 따라**

**가스는 주위에 열을 방출해야한다.** 

**즉 주위 입장에서는 열을 일로 완전하게 변환해야 하므로 이는 열역학 2법칙을 위반한다.**



### 카르노 사이클

우리가 가역,비가역을 정의한 이유는 이상적인 모델을 만들기 위해서이다.

그 모델이 바로 카르노 사이클이다. 앞서 말했듯 가장 효율적인 사이클은 reversible cycle이다.

이는 실제 사이클에서의 최대 한계를 보여준다.

이러한 카르노 사이클의 과정은 다음과 같다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591168429/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_3_aavkkw.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591168429/0603posting/이미지_3_aavkkw.jpg)



첫째로 1-2과정에서 높은 열원에서 열을 전달받을 때 dT가 매우 작다. 그러므로 온도변화는 없는 **등온**이다.

그렇다면 이는 REVERSIBLE PROCESS이다.

둘째로 2-3과정에서 팽창을 할 때 외부로부터의 열교환을 차단한 단열로 진행된다.

또한 매우 천천히 진행된다고 가정하면 온도는 
$$
T_H로부터 \ T_L로 \ 떨어질\ 것이다.
$$
마찬가지로 3-4과정은 낮은 열원으로 열을 버릴 때 dT가 매우 작으므로 **등온**

4-1과정은 열교환을 차단하며 압축을 함으로써
$$
T_L로부터 \ T_H로 \ 올라간다.
$$
![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169206/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_4_naboxi.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169206/0603posting/이미지_4_naboxi.jpg)



여기서 분홍색의 넓이가 Net work가 된다.

만약 3-4로 가지 않고 3-2로 가려했다면 (Q를 save하려 했다면)

이는 Net work를 만들지 못하고 원래 상태로 돌아오는 뻘짓을 했을 것이다.

카르노 냉동 사이클은 다음과 같다.



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169206/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_5_u4vvpe.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169206/0603posting/이미지_5_u4vvpe.jpg)



### 카르노 원칙

카르노기관에는 원칙이 두 가지 존재한다.

1. 같은 열원 사이에서 작동하는 가역적 heat 엔진이 비가역적 heat 엔진보다 효율이 크다.
2. 같은 열원 사이에서 작동하는 가역적 heat 엔진 두개의 효율은 같다.



이를 증명하기 위해 다음과 같은 모델을 보자.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169611/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_6_avynat.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591169611/0603posting/이미지_6_avynat.jpg)

여기서 비가역적 HE의 효율이 더 높다고 가정한다면 (CARNO 1원칙 위반)

비가역 HE에서 낮은 열원으로의 열방출량보다 가역 HE에서 낮은 열원으로의 열 방출량이 클 것이다.

가역 HE을 냉동으로 바꾸고 이 둘을 합쳐보자

그렇다면 $Q_H$는 소거되고 낮은 열원으로부터 열을 받아서 net일을 만드는 

Kelvin-Planck statement서술을 어긴다.

마찬가지로 CARNO 2법칙을 위반하는 경우를 위에 경우에 적용하여 상상해보자

같은 열원에서 하나가 더 높게 동작한다면 위의 경우에서 반례는 발생하므로 CARNO 2원칙 위반은 열역학 2법칙을 어기게 된다.



### 열역학적 온도 스케일



CARNO기관에서 같은 열원에서 작동하는 가역과정은 모두 효율이 같다고 하였다.

즉 효율이라는 함수의 변수는 두 열원의 온도라고 추정할 수 있고 작동하는 유체의 종류나 property에 독립적일 것이다.


$$
\eta_{th,rev}=g(T_{H},T_L)
$$


효율은 


$$
\eta_{th,rev}=1-\frac{Q_H}{Q_L}
$$


그러므로
$$
\frac{Q_H}{Q_L}=f(T_H,T_L)
$$


![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591171224/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_7_c65j2z.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591171224/0603posting/이미지_7_c65j2z.jpg)

위 그림에서 다음과 같이 정리 할 수 있다.


$$
\frac{Q_1}{Q_2}=f(T_1,T_2)
$$

$$
\frac{Q_2}{Q_3}=f(T_2,T_3)
$$

$$
\frac{Q_1}{Q_3}=f(T_1,T_3)
$$


위의 식에서


$$
\frac{Q_1}{Q_2}\cdot \frac{Q_2}{Q_3}=\frac {Q_1}{Q_3}
$$


이므로


$$
f(T_1,T_3)=f(T_1,T_2) f(T_2,T_3)
$$


그러므로


$$
f(T_1,T_3)=\frac{\phi (T_1)}{\phi(T_3)}
$$


$T_2$에 독립적이다.

이때 $\phi (T)=T 라는 열역학적 온도 scale이 등장한다.

그러므로써 


$$
(\frac{Q_H}{Q_L})_{rev}=\frac{T_H}{T_L}
$$


이는 카르노엔진 2원칙에 의해 유도되었으므로 REVERSIBLE PROCESS에서만 적용된다.

여기에서의 T를 Kevin scale이라 부르며, 이는 우리가 알고 있는 절대온도이다.

이는 절대영도와 물의 삼중점의 차이를 1/273.1등분 한 것을 1 kelvin 의 크기로 정의한다.



### 카르노 히트엔진

그러므로 효율은 다음과 같이 바뀐다.
$$
\eta_{th,rev}=1-\frac{T_L}{T_H}
$$

### Quality of energy 

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591172287/0603posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_8_iwzyua.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591172287/0603posting/이미지_8_iwzyua.jpg)



위 그림과 같이 높은 열원의 온도가 높아질수록 효율은 높아진다. 

즉 더 많은 양의 에너지를 일로 변환하므로 높은 온도일수록 더 높은 퀄리티의 에너지이다.

또한 일은 열보다 퀄리티가 더 높은데 왜냐하면 열은 100% 일로 변환이 불가하지만

일은 열로 100%변환이 가능하기 때문이다.



### 레퍼런스

[1] Thermodynamics : An engineering approach - fith edition , YUNUS A. CENGEL - 교과서 296p-313p

