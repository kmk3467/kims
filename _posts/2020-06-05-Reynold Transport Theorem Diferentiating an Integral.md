# 유체역학

## Diferentiating an Integral

RTT를 이해하기 위해선 적분을 미분하는 방법을 알아야 한다.

이를 라이프니츠 룰이라고 하며 결론부터 말하자면 다음과 같다.
$$
if \quad \phi (t)=\int_{a(t)}^{b(t)}f(z,t)dz , \ then \\
\frac{d\phi}{dt}=\int _{a(t)}^{b(t)}\frac{\partial f(z,t)}{\partial t}dz + f(b(t),t) \frac{db}{dt}-f(a(t),t)\frac{da}{dt}
$$


쉬운 변수로 예를 들자

f는 매끄러운 함수이다. 


$$
\phi(x)=\int_c^x f(z)dz
$$


then


$$
\frac{d\phi(x)}{dx}=f(x) \quad (1)
$$


우리는 이 phi 함수가 f의 지정된 범위까지의 넓이임을 안다.


$$
\phi(x)=\int_x^c f(z)dz
$$


then 


$$
\frac{d\phi(x)}{dx}=-f(x) \quad (2)
$$


이제 시간에 영향을 받는 이변수함수를 정의해보자


$$
\phi(t)=\int_a^bf(z,t)dz
$$


a,b가 상수라면


$$
\frac{d\phi(t)}{dt}=\int_a^b \frac{\partial f(z,t)}{\partial t}dz \quad(3)
$$


3변수 함수를 예로 들면


$$
\phi(t,a,b)
$$


가정할 때 a와 b는 t에 대해 영향받는다고 가정하자,

그렇다면 a=a(t), b=b(t)


$$
\Phi(t)= \phi (t,a(t),b(t))=\int_{a(t)}^{b(t)}f(z,t)dz
$$


목표는 phi함수의 미분 값을 구하는 것이므로


$$
\frac{\Phi(t)}{dt}=\frac{\partial \phi}{\partial t}\frac{dt}{dt}+\frac{\partial \phi}{\partial a}\frac{da}{dt}+\frac{\partial \phi}{\partial b}\frac{db}{dt} \quad(4)
$$


(1),(2),(3) 식을 사용하면


$$
\frac{d\Phi(t)}{dt}=\int_{a(t)}^{b(t)}\frac{\partial f(z,t)}{\partial t}dz-f(a(t),t)\frac{da}{dt}+f(b(t),t)\frac{db}{dt}
$$


이 식이 라이프니츠 정리이다.

이를 3차원으로 확장하면


$$
\frac{d}{dt}\int_{V(t)}G(x,y,z,t)dV=\int_{V(t)}\frac{\partial G}{\partial t}dV+\int_{A(t)}G\vec V_{A}\cdot\vec n dA
$$


V(t)가 움직일 때 A(t)는 이의 표면이다. 

$V_A$는 이의 절대 속도이다.

우리는 이 G를 pb로 치환하여 fluid flow에 적용할 수 있다.


$$
\frac{d}{dt}\int_{V(t)}\rho b dV=\int_{V(t)}\frac{\partial (\rho b)}{\partial t}dV+\int_{A(t)}(pb)\vec V_{A}\cdot\vec n dA
$$


이를 system이 고정되있고 fluid flow가 움직인다고 하면 $V_A=V$이다.

이러한 특수한 케이스를 material volume이라 한다.


$$
\frac{d}{dt}\int_{V(t)}\rho b dV=\int_{V(t)}\frac{\partial (\rho b)}{\partial t}dV+\int_{A(t)}(pb)\vec V\cdot\vec n dA
$$


이러한 식은 system과 control volume이 따로 움직이므로 일치하지 못한다.

즉 $t+\Delta t$에서는 성립되지 않는다. 

하지만 중요한 것은 at time t에서 이들은 동일하다는 것이다.

그러므로

General RTT, nonfixed CV:


$$
\frac {dB_{sys}}{dt}=\int_{CV}\frac{\partial}{\partial t}(\rho b)dV+\int_{CS}\rho b \vec V\cdot \vec ndA
$$


이 최종식은 어떻게 생겨먹었든, 움직이는, 변형하든 time t에 대해서 항상 성립한다.

또한 이 V는 상대속도 V가 아닌 유체의 절대 속도이다.

또한 위 식을 이용해서 상대속도 RTT를 유도할 수도 있다.



### RTT를 왜 쓰는데??

우리는 이를 이용해 라그랑지안 관점을 오일러리안 관점으로 해석할 수 있다.

이는 챕터 5와 6에서 질량,에너지,운동량 그리고 각운동량 보존식을 RTT를 이용해

관찰해 볼 수 있다고 한다.(나도 안해봐서 모른다.)



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1591366730/200605posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_3_huc6x9.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1591366730/200605posting/이미지_3_huc6x9.jpg)



위 그림은 물질미분과 RTT의 유사성이다. 

이는 추후에 진도를 진행해가며 보완해가도록 하겠다.



### 레퍼런스

[1] Fluid Mechanics 3rd Edition, Yunus A. Cengel

[2]Diferentiating an Integral P. Haile, February 2020