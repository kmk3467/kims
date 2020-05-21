# 열역학 열린계

## steady flow 에서의 에너지 분석

steady flow 에서 Control volume내의 intesive propery와 extensive property의 변화가 존재하지 않는다.

즉 V, m, E = constan이다.


$$
E_{CV}=constant \\ \Delta E_{CV}=0
$$


이 말인 즉 에너지를 구성하는 구성성분들의 출입량이 같다는 뜻이 된다.

이렇게 전제되기 위해서 
$$
\dot m_{in}=\dot m_{out} \quad (1)
$$
이 성립되어야 한다.
$$
에너지 방정식에\ 의해\\
E_{in}-E_{out}=\Delta E_{system}\\\dot E_{in}-\dot E_{out}=\frac{dE_{system}}{dt}\\\frac {dE_{system}}{st}=0 \ 이므로 
 \\ \dot E_{in}=\dot E_{out}
$$


이를 지난시간에 열린계에서의 에너지 방정식으로 풀면


$$
\dot Q_{in}+\dot W_{in}+\sum_{in}\dot m(h+\frac{V^2}{2}+gz)=\dot Q_{out}+\dot W_{out}+\sum_{out} \dot m(h+\frac{V^2}{2}+gz)
$$


K.E와 P.E는 일반적으로 무시된다고 하고, 식을 보기 편하게 하기 위해 입출이 하나씩만 있다고 가정한다.

(1)의 전제에 의해


$$
\dot Q_{in,net}- \dot W_{in,net}=\dot m(h_2-h_1)
$$


양변을 $\dot m$ 으로 나눠주면


$$
q-w=h_2-h_1
$$


## 노즐과 디퓨저

노즐은 압력을 희생해 속도를 높여주는 기계이고, 디퓨저는 그 반대의 역할을 한다.

이들을 흐르는 유체사이의 열전달은 무시해도 좋다. 
$$
\dot Q =0
$$
또한 일과, 위치에너지를 무시한다.
$$
\dot W=0,\\ 
\Delta P.E=0\\
$$
감을 잡기 위해 예제를 풀어보자.



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1590027520/200521posing/%EC%9D%B4%EB%AF%B8%EC%A7%80_7_hopo3z.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1590027520/200521posing/이미지_7_hopo3z.png)



![https://res.cloudinary.com/dbzvbzksw/image/upload/v1590027520/200521posing/%EC%9D%B4%EB%AF%B8%EC%A7%80_8_wwl2vp.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1590027520/200521posing/이미지_8_wwl2vp.png)



![hi](https://res.cloudinary.com/dbzvbzksw/image/upload/v1590028328/200521posing/88E283D3-E0EB-4CBF-9A80-1C9B56BF125D_cwh7jx.jpg)



결론적으로 지난번에 배운 에너지방정식에서 여러가지 가정을 세워 운동에너지를 고려해주면 된다.



### 앞으로의 과제

다음 이 포스팅을 리뷰할때는 직접 이러한 디퓨저를 구하는 프로그래밍을 해보도록 한다.

- 디퓨저, 노즐 프로그래밍하기 



### 레퍼런스

[1] Thermodynamics : An engineering approach - fith edition , YUNUS A. CENGEL - 교과서