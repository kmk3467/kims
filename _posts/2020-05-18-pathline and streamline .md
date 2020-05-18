## 유체역학

### FLOW PATTERNS AND FLOW VISUALIZATION

유체의 흐름을 분석하기 위해서 일련이 작업을 해야한다.

그러한 정보를 얻는 과정 중 하나가 FLOW VISUALIZATION이다

numerical soulutins 인 CFD(computational fluid dynamics)를 행하기 전에 전체적인 그림을 보기 위해서는 FLOW VISUALIZATION이 필요하다. 

인간은 시각적인 정보를 처리하는데 훨씬 빠르고 정확하기 때문이다.

우선 FLOW VISUALIZION에 필요한 요소들을 익혀나가보자

### Streamlines

```
A streamline is a curve that is everywhere tangent to the instantaneous local velocity vector.
```



즉 어느 순간에서의 속도벡터에 접하는 **곡선**이다.

아주 작은 곡선의 길이 벡터를 정의하면
$$
d\vec r=dx\vec i+dy\vec j +dz\vec k
$$
이때 이 r벡터는 항상 로컬속도벡터 
$$
\vec V = u \vec i + v \vec j +w \vec k
$$
와 정의에 의해 반드시 평행해야 한다. 

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589759416/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_6_gx3skt.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589759416/0518posting/이미지_6_gx3skt.png)

*출처:교과서[1] 141page 참조*

그러므로 삼각형을 그린다면 그 비는 비례한다.
$$
\frac {dr}{V}=\frac {dx}{u}=\frac {dy}{v}=\frac {dz}{w}
$$
xy plane에서의 식은 탄젠트 값의 비로도 나타낼 수 있다.
$$
\frac {dy}{dx}=\frac {v}{u}
$$
실습을 위해 matlab에서 streamline을 그려보겠다.

기본적인 매트랩의 레퍼런스는 [2] 링크를 참조하자.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589760049/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_8_tw9oln.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589760049/0518posting/이미지_8_tw9oln.png)

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589761080/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_10_pd131d.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589761080/0518posting/이미지_10_pd131d.jpg)

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589761195/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_11_xuy1qe.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589761195/0518posting/이미지_11_xuy1qe.png)

예제 4-4의 문제를 풀기 위해 코딩해보도록하자

```matlab
% 1. x,y정의 0.2씩 증가하며 0부터 2까지
[x,y] = meshgrid(-3:0.2:3,-1:0.2:5);
% 2. u,v를 예제 1에 조건에 맞게 설정
u=0.5+0.8*x;
v=1.5-0.8*y;
% 3. 퀴버 플롯을 생성 (화살표 같은거)
figure
quiver(x,y,u,v)
% 4. streamline의 x좌표와 y좌표 행렬의 크기는 같아야 한다.
startx=-1:0.5:1;
starty=ones(size(startx))
starty=starty*(5)
startz=ones(size(startx))*5
streamline(x,y,u,v,startx,starty)
streamline(x,y,u,v,startx,starty/-5)
% 5. x좌표를 바꿔가며 y를 고정했을때 그려지는 플랏을 그렸을때, 한 명령어에서 두개의 y시작점을 가지지 못하는것 같아서 streamline을 두개 만들어서 실행하였다.

```

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589763571/0518posting/untitled_qunl5j.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589763571/0518posting/untitled_qunl5j.jpg)

실제 결과도 비슷하게 그려지는 것을 확인 할 수 있었다.

### Stream tube

Stream tube는 Stream line의 다발로 정의 될 수 있다. 그러므로 로컬 속도벡터와 항상 평행하며 유체의 flow는 stream tube를 가로지를 수 없다. 

```
Streamtube must remain there and cannot cross the boundary of the streamtube.
```

unsteady flow에서 streamline의 양상은 시간에 따라 상당히 변한다. 그럼에도 불구하고 stream tube의 수직한 단면을 가로지르는 유체의 질량유량은 항상 일정하다. 즉 stream tube의 직경이 좁아지거나 늘어남을 통해 유속이 빨라지던 느려지던 항상 그 통과하는 질량유량을 일정하게 유지한다. 

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589764196/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_12_g5yfr4.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589764196/0518posting/이미지_12_g5yfr4.png)

위 그림과 같이 streamtube의 직경은 유동적이다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589764357/0518posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_13_brvi62.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589764357/0518posting/이미지_13_brvi62.png)

다음 그림을 참조하면 이해가 편하다.

### Pathlines

pathlines는 라그랑지안 개념으로 이해하면 편한데 유체입자가 움직인 경로를 한정된 시간동안 사진으로 찰칵 찍어놓은 것이다.

이러한 pathlines은 속도장이 알려져있다면 계산할 수 있다.
$$
\vec x= \vec x_{start}+\int_{t_{start}}^t \vec V dt
$$
만약 속도장이 steady한 상태일 때 입자는 streamlines들을 따라 이동할 것이다.

그러므로 이동한 궤적인 pathlines과 steamlines들은 같을 수 밖에 없다.

### 레퍼런스

[1] Fluid Mechanics 3rd Edition, Yunus A. Cengel

[2] https://kr.mathworks.com/help/matlab/ref/streamline.html KR MATLAB STREAMLINE