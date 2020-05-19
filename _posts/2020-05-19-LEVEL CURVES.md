## Calculus - LEVEL CURVES

지난 시간까지 2변수 함수가 무엇인지와 2변수를 이용한 그래프를 그려보았습니다.

2변수 함수를 MATLAB으로 실제로 그려보도록 하겠습니다



### MATLAB을 이용한 2변수 함수 그래프 그리기

우선 MATLAB에서 다변수 함수를 어떻게 입력하는지부터 이해되어야합니다.

출처는 URL: [네이버블로그-AureaGenus][https://m.blog.naver.com/PostView.nhn?blogId=aureagenus&logNo=120101655784&proxyReferer=https:%2F%2Fwww.google.com%2F]

우리가 $ f(x,y)=x^2+y^2 $ 라는 함수를 matlab으로 입력하려고 합니다.

f(x,y)=z라 할 때,

z의 정의역은 x,y가 모든 실수이므로 모든 실수가 됩니다.

이때 z의 입장에서 x,y가 각각 독립적으로 입력되어야 합니다.

2중 for문으로 생각하면 쉽습니다.

예를 들어

```matlab
x=linespace(-5,5,100);
y=linespcae(-5,5,100);
z=x.^2+y.^2
```

이라고 할 때 위의 예는 틀립니다. 

각각 독립적으로 입력되는 경우를 어겼기 때문입니다.

즉 만약 x=1일때 y=-5,-4.9.... 이렇게 입력되어야 하지만

위의 경우는 x와 y가 같을 때를 출력하기에 

x의 size가 100개 y의 size가 100개일때 

z의 순서쌍은 10000개가 나와야 하나, 위의 경우 100개만 나오기 때문입니다.

즉 우리는 x,y의 행렬을 다음과 같이 만들어 주어야 합니다.


$$
x=\begin{pmatrix}
 1 & 2 & 3 & \cdots & 100 \\
 1 & 2 & 3 & \cdots & 100 \\
  1 & 2 & 3 & \cdots & 100 \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
    1 & 2 & 3 & \cdots & 100 \\
 
 \end{pmatrix}
$$

$$
y= \begin{pmatrix}
 1 & 1 & 1 & \cdots & 1 \\
 2 & 2 & 2 & \cdots & 2 \\
  3 & 3 & 3 & \cdots & 3 \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
    100 & 100 & 100 & \cdots & 100 \\
 
 \end{pmatrix}
$$


이렇게 해주어야 x에 하나의 element 에 대해 대응되는 y값이 100개가 될것입니다.

하지만 이렇게 만들면 너무 노가다입니다.

다행스럽게도 matlab에서는 이러한 행렬을 만드는 기능을 지원해줍니다.

meshgrid(x,y)라는 함수입니다.



```matlab
[x y]=meshgrid(1:4,1:4);
z=x.^2+y.^2
```



자, 이제 준비는 끝났으니 그려보도록 합시다.



```
mesh(x,y,z)
```



### 실제 그래프를 그리면서 부각되는 정의역의 중요성

우리는 처음에 다변수함수를 알아가며 다변수함수 f에 정의역 D에 대해 알아갔습니다.

이는 코드를 짤 때 중요성을 다시 인식하게 되는데요. 

우선 교과서 예제 6번을 풀어보도록 합시다.

**Ex 6) Sketch the graph of g(x,y) =** 
$$
\sqrt{9-x^2-y^2}
$$


우선 이 친구를 그리려면 [x y]의 meshgrid를 짜야 하는데 그러려면 x y의 범위를 알아야 합니다.

그러한 범위는 저번시간에 구했던 정의역을 구하는 경로대로 구해야합니다.

양변을 제곱하면


$$
x^2+y^2+z^2=9
$$


가 되며 z는 항상 양수이므로 양의 반구가 됩니다. 

이때 내부의

 
$$
9-x^2-y^2>=0 \ 이므로
$$
​	

x,y의 범위는 3을 반지름으로 하는 원이 되어야 합니다.

실제로 코드를 짜보면



```matlab
[x y]=meshgrid(-10:0.1:10,-10:0.1:10);
z=sqrt(9-x.^2-y.^2)
z1=real(z)
mesh(x,y,z1)
```



여기서 z1은 z가 복소수가 되면 mesh를 그릴 수 없습니다. 그러므로 항상 real num으로 바꿔주는 함수를 넣었습니다.

이에 대한 결과는 다음과 같습니다.

저 같은 경우 일부러 아까의 x,y의 범위가 3을 반지름으로 하고 0,0을 원점으로 하는 범위로 두지 않은 것은

어떻게 출력할 것인가가 궁금해서 입니다. 출력값은 다음과 같았습니다



![이미지](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589865607/200519posting/untitled_psrsvw.jpg)



똑똑하게도 범위를 벗어나는 값에서는 z값을 출력하지 못합니다. 



### LEVEL CUVES

LEVEL CURVE를 통해 그래프를 VISULIZATION할 수 있습니다.

이에 대한 정의는 다음과 같습니다.

**The level curves of a function of two variables are the curves with equations f(x,y) =k ,** 

**where k is a constant (in the range of f).**

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589867495/200519posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_1_cxdacq.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589867495/200519posting/이미지_1_cxdacq.png)

다음과 같이 f(x,y)=k라 할때 z=k라 한다면 각 k값에 대한 x,y값이 x-y 평면에 투사될 것입니다.

그래서 위 그림과 같이 시각화 할 수 있습니다.

만약  투사된 영역의 거리가 서로 가까울수록 더 가파르다고 볼 수 있습니다.

이러한 예가 바로 산등성이 지도입니다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589867495/200519posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_2_nsbfmv.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589867495/200519posting/이미지_2_nsbfmv.png)

다음과 같은 등고선에 의해 같은 z값 델타에 의해 등고선이 그려졌습니다.

같은 델타 값에 비해 산 초입은 등고선 영역의 간격이 머니 완만한걸 알 수 있고,

반대로 산 중간은 등고선 영역의 간격이 가까우니 가파르단걸 알 수 있습니다.

이러한 지도는 다변수함수의 level curve 를 활용한 경우입니다.





### 다음편 내용

이번 편은 매트랩을 활용한다고 내용이 길어졌습니다.

다음은 다변수함수의 극한에 대한 정의가 필요해보입니다.

그러므로 우리는 먼저 하지 않고 넘어간 일변수함수의 극한에 대한 정의를 거친 후

그 다음 내용으로 넘어가도록 하겠습니다.



### 레퍼런스

[1] Calculus - J. Stewart (교과서)

[2] [네이버블로그-AureaGenus][https://m.blog.naver.com/PostView.nhn?blogId=aureagenus&logNo=120101655784&proxyReferer=https:%2F%2Fwww.google.com% - MATLAB 다변수함수 그리는 방법