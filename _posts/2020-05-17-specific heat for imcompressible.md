

### 이어서

우리는 저번에 어디까지 얘기를 했었냐면, 비열이 무엇인가? 를 알아보고 나서 비열을 정의했습니다.

비열을 알아야 한다는 당위성이 주어졌고, 그에 따른 1st law에 기반한 수학적 증명을 했습니다.

그리고 마지막에 실제 세계에서 좀 더 간략하게 계산을 하기 위한 PV=mRT 이상기체 상황에서의 비열의 상태도 보았습니다.

이제 우리가 알아볼 것은 Incompressible material 에서의 비열입니다.



### Incompressible material 

직관적으로 알 수 있듯이 이 친구들은 압축이 안됩니다.

수식적으로는 비체적 *V*=const 인 물질을 말합니다.

특수한 경우를 제외한 고체나 액체가 이러한 물질에 속합니다.

여러분은 온도나 엄청난 압력을 물체에 가했을 때 걔네들이 엄청 많이 쪼그라들거나 늘어나나요?

물론 그런 경우도 있습니다. 고무같은 경우가 그런 예입니다만, 보통 이런 경우는 예외로 칩니다.

계속 유체나 열 또는 고체를 진행해가며 만나는 식들은 incompressible 을 사랑합니다.

왜냐면 식이 어~~~엄청나게 간단해지기 때문입니다.

예를 들면 우리가 어떤 기계를 만들 때 터치형으로 조작되는 기계를 만든다 생각하면 이는 모든 사람에게 적용될 수 없습니다.

손가락이 없는 사람도 고려해야하고, 눈이 안보이는 사람도 고려해야하죠

하지만 공정비를 아끼기 위해서는 그러한 점을 예외로 두고 기본형을 '비장애인'으로 가정하고 만듭니다. 

이러한 예에서와 같이 incompressible material은 물체들의 카테고리 내에서 주류입니다.





### Incompressible material for specific heat

이 친구들에게서 비열은 어떻게 작용할까요?

결론부터 말하자면 
$$
C_p=C_v=C \quad in \ incompressible \ material
$$
이는 수학적으로 책의 후반부에 증명하므로 우선 받아들입니다.

이상기체와 비슷하게도 비압축성 물질의 비열은 온도만의 함수가 됩니다.

그러므로

<br>
$$
du=C(T)dT
$$
<br>

적분하면

<br>
$$
\Delta u=u_2-u_1=\int_1^2C(T)dT
$$
<br>

하지만 T의 변화량이 작다면 C의 변화량도 작게 되므로 평균값이 허용됩니다.

<br>
$$
\Delta u\cong C_{avg}(T_2-T_1)
$$
<br>

내부에너지는 별 변화가 없어 실망하셨다면 엔탈피의 변화는 좀 달라집니다.

h=u+Pv 에서 v=const이므로 이 식을 미분하면

<br>
$$
dh=du+vdP+Pdv
$$
<br>

dv=0이므로

<br>
$$
dh=du+vdP
$$
<br>

적분하면

<br>
$$
\Delta h= \Delta u + v\Delta P \cong C_{avg}\Delta T+v\Delta P
$$
<br>

이때 고체에서는 $v\Delta P$항이 중요치 않아서 $\Delta h=C_{avg}\Delta T$

액체에서는

- $\Delta P=0$ in heater :  $\Delta h=C_{avg}\Delta T$
- $\Delta T=0$ in pumps :  $\Delta h=v\Delta P$





## 정리



1. C는 incompressible 에서 일정하다.<br>
   $$
   C_p=C_v=C \quad in \ incompressible \ material \quad (1)
   $$
   <br>

2. 내부에너지 변화는 다음과 같다.<br>
   $$
   \Delta u\cong C_{avg}(T_2-T_1)
   $$
   <br>

3. 엔탈피 변화는 다음과 같다.

   <br>
   $$
   \Delta h\cong C_{avg}\Delta T+v\Delta P
   $$

   - 고체일때<br> 
     $$
     \Delta h=C_{avg}\Delta T
     $$

   - 액체일때(히터)<br>
     $$
     \Delta h=C_{avg}\Delta T
     $$
     

   - 액체일때(압축기)<br>
     $$
      \Delta h=v\Delta P
     $$
     