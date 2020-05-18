## CALCULUS - FUNCTIONS OF TWO VARIABLES
역학공부를 하다보면 자주 다변수 함수에 대한 얘기가 나온다.

프로그래밍도 기본적으로 다변수함수를 전제로 이야기가 전개된다.

다변수 함수란 뭔가?

### FUNTIONS OF TWO VARIABLES

두개의 변수를 가진 함수를 본적이 있는가?

우리는 구글어스를 보고있다고 가정하자

어떤 지점의 T를 알고 싶어서 그 지점의 점을 찍었다고 생각한다면, 그 지점의 온도를 나타내는 프로그램을 제작한다고 생각해보자.

그렇다면 입력 변수는 좌표 값일 것이다. (위도,경도)

출력변수는 온도일 것이다 

이를 수학적으로 표현하면 다음과 같다.

T=f(x,y)

이에 대한 교과서의 정의는 다음과 같다.

* Domain은 정의역, range는 치역이라 한다.

**DEFINITION A function of two variables is a rule that assigns to each ordered**
**pair of real numbers in a set a unique real number denoted by . The**
**set is the domain of and its range is the set of values that takes on, that is,**

$\{f(x,y) \mid (x,y) \in D\}$

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_20_l7saas.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/이미지_20_l7saas.png)

다음과 같이 어떤 값을 입력받아서 z라는 함수의 ragne에 맵핑시켜준다.

이때 x,y는 independent variables, z는 dependent variables이다.

x,y는 독립적으로 결정되고 이에 따라 z는 결정된다.

일변수함수에 비해서 독립변수가 1개 늘어난 모습을 관찰 할 수 있다.

**예제4)**
$$
g=\sqrt{9-x^2-y^2} 
$$
위 식의 정의역과 치역을 찾아라.


$$
D=\{(x,y)\mid x^2+y^2\le9\}
$$
이때 D의 기하학적 모양은 다음과 같은 원이다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782864/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_d24_da1fo3.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782864/0518posting/이미지_d24_da1fo3.png)
$$
\{z\mid z=\sqrt{9-x^2-y^2}\}
$$

$$
z\ge0 \ 이므로 \ 9-x^2-y^2\ge0
$$

또한 정의역에 의해 $x^2+y^2\ge 0$ 이어야 하므로
$$
9\ge 9-x^2-y^2
$$
그러므로 위 두 경우를 조합하면
$$
\{z\mid 0 \le z \le 3 \} = [0,3]
$$


### 그래프

이변수함수의 그래프를 그려보도록 하자.

f=(x,y,z)라 할 때 z=f(x,y) 라하면

f=(x,y,f(x,y)) 이며 실질적으로 이를 그리는 변수는 2개이다.

f의 개형은 두변수함수에서 z가 x,y에 의해 결정나므로 이는 f의 xy plane 에 정의역인 D에 위나 아래에서

전체적인 그래프 S가 그려진다.

그림으로 나타내면 다음과 같다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_23_pde9dq.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/이미지_23_pde9dq.png)



**예제 5) f(x,y) = 6-3x-2y의 그래프를 그려라**

이는 또한 이변수 함수이므로 x,y의 정의역 위에 그려질 것이다.

x가 모든 실수, y가 모든 실수이므로 f의 정의역인 모든 실수 위에 그려진다.

이때는 기술적으로 절편을 구하면  그래프의 최대 범위를 알 수 있다.

f(x,y)=z 라하면 z=6-3x-2y

두 변수를 각각 0으로 해서 구하면 x=2 y=3 z=6이 된다.

이를 서로 연결해주면 3차원 그래프가 그려진다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_24_rh1bop.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589782216/0518posting/이미지_24_rh1bop.png)



### 느낀점 

이 포스팅을 작성하며 새롭게 느낀 게 많았다.

다변수 함수는 실제로도 많이 쓰이면서도 깊게 고찰 안해봤던 주제였다.

이 주제를 진행해가며 역학에 대한 이해도 다시금 깊어질 것 같다.

그리고 코딩에서의 함수도 필연적인 다변수 함수이므로 이에 대한 이해도가 높아질 것 같다.

이를 진행해가며 매트랩으로 직접 그래프를 그려가며 진행 할 예정이다.