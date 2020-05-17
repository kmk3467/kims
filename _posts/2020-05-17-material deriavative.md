## Material Derivative

### 저번시간까지의 내용

유체역학의 시스템을 바라보는 관점에 대해 알아보았다.

- Eulerian description
- Lagrangian description



### 서로간의 변환점

만약 우리가 입자를 추적해 나갈 수 있다면 라그랑지안기법을 사용할 것이다.

이를 입자의 방정식으로 나타낼 수 있고, 약간의 수학적 변형을 통해 오일러리안 기법으로 바꿀 수 있다.

우선 입자의 position vector를 정의하면 

<br/>
$$
s(x,y,z,t)=[x_{particle}(t),y_{particle}(t),z_{particle}(t)]
$$
처음 시작은 뉴턴 2법칙으로 부터 시작한다.

<br>
$$
\vec F_{particle}=m_{particle}\vec a_{particle}
$$
항을 이항하면


$$
\vec a_{particle}=\frac{\vec {F}_{particle}}{m_{particle}}
$$

$$
\vec a_{particle}=\frac{d\vec {V}_{particle}}{dt} \quad (1)
$$
<br>

<br/>

속도벡터는 다음과 같이 정의된다.

<br/>
$$
\vec V_{particle}=\vec V(x_{particle}(t),y_{particle}(t),z_{particle}(t),t) \quad (2)
$$
<br/>

(1)식을 (2)식에 적용하여 풀어야한다.

이때 편미분 개념이 들어가는데 이는 추후에 **전미분 포스팅을 통해서 수학 내용을 추가하겠다.**[1]

<br/>
$$
d\vec V=\frac{\partial \vec V}{\partial x}dx+\frac{\partial \vec V}{\partial y}dy+\frac{\partial \vec V}{\partial z}dz+\frac{\partial \vec V}{\partial t}dt
$$
<br/>

그러므로 

<br/>
$$
\frac{d\vec {V}_{particle}}{dt} =\frac{\partial \vec V}{\partial x}\frac{dx}{dt}+\frac{\partial \vec V}{\partial y}\frac{dy}{dt}+\frac{\partial \vec V}{\partial z}\frac{dz}{dt}+\frac{\partial \vec V}{\partial t}\frac{dt}{dt}
$$
여기서 x성분의 속도를 u, y성분의 속도를 v, z성분의 속도를 w, dt/dt=1이라하면

$$
\vec a_{particle}=\frac{d\vec {V}_{particle}}{dt} =\frac{\partial \vec V}{\partial t}+u\frac{\partial \vec V}{\partial x}+v\frac{\partial \vec V}{\partial y}+w\frac{\partial \vec V}{\partial z}
$$
<br>

이 순간에 입자의 가속도는 어떤 컨트롤 볼륨 안에 가속도와 같아야 한다.

왜냐하면 입자는 fluid flow와 함께 가속 받기 때문에  위 항에서 particle을 빼고 확장 할 수 있다.

<br>
$$
\vec a=\frac{\partial \vec V}{\partial t}+u\frac{\partial \vec V}{\partial x}+v\frac{\partial \vec V}{\partial y}+w\frac{\partial \vec V}{\partial z}
$$
<br>

때 gradient operator 을 이용해서 정리하면 **(추후 포스팅예정)**

<br>
$$
\nabla =(\frac{\partial }{\partial x},\frac{\partial }{\partial y},\frac{\partial }{\partial z})
$$
<br> 
$$
\frac{d\vec {V}_{particle}}{dt} =\frac{\partial \vec V}{\partial t}+(\nabla \cdot\vec V)\vec V             \quad (3)
$$
<br><br> 위 식을 정확히 이해하기 위해서는 **아인슈타인 컨벤션에 대한 논의가 있어야 하고 그것도 추후 포스팅이 필요해 보인다.** 

이를 Cartesian coordinates 로 전개하면<br/>
$$
a_x=\frac{\partial  u}{\partial t}+u\frac{\partial u}{\partial x}+v\frac{\partial u}{\partial y}+w\frac{\partial u}{\partial z}
$$
$$
a_y=\frac{\partial  v}{\partial t}+u\frac{\partial v}{\partial x}+v\frac{\partial v}{\partial y}+w\frac{\partial v}{\partial z}
$$
$$
a_z=\frac{\partial  w}{\partial t}+u\frac{\partial w}{\partial x}+v\frac{\partial w}{\partial y}+w\frac{\partial w}{\partial z}
$$
<br>

(3)식에서 좌변항의 왼쪽은 **local acceleration** 이라 부르며 steady flow(시간에 따른 변화량이 없는 흐름)일 경우 항상 0이다.

좌변항의 오른쪽은 **advective acceleration** 또는 **convective acceleration** 하며 steady flow에서 0이 되지 않는다.

예를 들어 노즐을 steady flow라 가정했을 때 Eulerian 영역에서 모든 영역은 시간에 따른 변화가 없다.

그런데 노즐의 출구속도는 입구속도보다 빨라지므로 분명 가속된다.

이러한 입자의 움직임에 따른 효과(convecting or advecting)을 책임지고 있는 것이 (3)식의 두번째 항이다.

### Material Derivative

우리는 3식에서의 전미분에 특별한 이름을 붙이는데 이를 Material Derivative 라 한다.

특별한 표기법 D/Dt 로 표기하며 이는 다음과 같다

<br/>
$$
\frac{D}{Dt}=\frac{d}{dt}=\frac{\partial}{\partial t}+(\vec V \cdot\vec \nabla)
$$

<br>

- 벡터표현<br/>
  $$
  \frac{D\vec V}{Dt}=\frac{d\vec V}{dt}=\frac{\partial \vec V}{\partial t}+(\vec V \cdot\vec \nabla)\vec V
  $$
  <br>

- 스칼라표현 

$$
\frac{DP}{Dt}=\frac{dP}{dt}=\frac{\partial P}{\partial t}+(\vec V \cdot\vec \nabla)P
$$



### 이를 유도함으로써 무엇을 할 수 있는가?

전미분을 유도함으로써 라그랑지안 기법으로 해석하던 유체의 플로우를 오일러리안 방식으로 해석 가능하게 되었다.

이 유도과정은 입자의 위치벡터를 뉴턴 제 2법칙으로부터 전미분하여 얻어진 것이다.

이로써 우리는 유체해석을 위한 오일러리안 기법을 사용할 준비가 된 것이다.



[1] : http://www.sigmapress.co.kr/shop/shop_image/g17812_1405051763.pdf 시그마프레스-전미분

[2] : Fluid Mechanics 3rd edition,  Yunus A.Cengel 외 1명 - 유체역학 교과서

[3] : https://www.continuummechanics.org/materialderivative.html 연속체역학 - Material Derivative

