## 졸업작품을 위한 라즈베리파이 설치

라즈베리파이를 이용하여 구상중인 시스템이 존재한다. 

이는 포스팅을 해가며 자세한 과정을 서술할 예정이다.

우선 라즈베이파이를 설치해야한다.

## 라즈비안 

라즈베리파이의 운영체제는 메이저하게는 3개라고한다.

우분투, 라즈비안, 윈도우 10 IoT care

우선 초보자인 필자로서는 라즈베리파이 재단에서 공식적으로 권장 및 제공하는 운영체제인

라즈비안을 쓰는게 합리적으로 보였다.

#### 다운로드

우선 https://www.raspberrypi.org/downloads/raspbian/

에서 라즈비안 버스터를 다운로드 받는다. 2.5GB라고 하니 여유공간을 남겨두자

오래걸리니 다른거 할걸 마련해두고 다운로드 받도록하자

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589500698/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_6_x9s83b.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589500698/200515posting/이미지_6_x9s83b.jpg)

또한 Rufus라는 프로그램을 구글에서 검색하여 다운로드 받도록하자

이 프로그램은 위에서 받은 이미지를 부팅가능하도록 구워주는 프로그램이다.

다운이 완료되었다면 이미지 파일을 rufus프로그램을 이용해 구동한다.

물론 이를 위해 Micro SD card와 reader은 미리 구매했어야 한다.

#### Rufus 프로그램을 이용한 드라이브 세팅

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527189/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_8_prymwq.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527189/200515posting/이미지_8_prymwq.jpg)

위 그림과 같이 이미지 파일을 선택 후 라즈베리 파이가 설치된 드라이브에 이미지를 만들어주자

여기까지는 다른 사용자와 똑같이 진행했으나, 본인은 모니터와 여분의 키보드가 없는 관계로

SSH를 이용한 설치를 진행하도록 한다.

쉽게 말해 라즈베리파이 자체에서 부팅시켜서 설치가 아닌, 내 노트북에서 와이파이를 연결하여 원격 설치를 한다는 뜻이다. 

이를 위해 사전 작업이 필요한데 라즈베리파이를 켜자마자 wifi가 접속이 되도록 wifi설정파일을 만들어주고 SSH 기본설정을 Enable로 변경하여야 한다.

#### wifi 설정파일 만들기

D:\ (SD카드 드라이브)에서 text파일을 만들어 wpa_supplicant.conf 라는 이름으로 변경해준다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589498871/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_4_odjyql.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589498871/200515posting/이미지_4_odjyql.jpg)

이 파일을 메모장으로 열어서 아래와 같이 입력해준다.

```
country=GB

ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev

update_config=1

network={

  ssid="SSID"

  psk="PSK"

  key_mgmt=WPA-PSK

}
```

이때 SSID에는 와이파이의 이름을, Psk에는 비밀번호를 적어주어야 한다.



### SSH를 Enable 시키자

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589499178/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_5_cqrqvg.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589499178/200515posting/이미지_5_cqrqvg.png)

간단하다. 그냥 SSH파일을 만들어서 넣어두자 

확장자는 없다.

이제 라즈베리파이를 켜보자. 물론 SD카드는 붙인채로



### 라즈베리파이의 ip 확인

필자같은 경우 ip를 iptime 관리자 모드에서 확인하였다.

본인이 iptime을 사용하고있고 기본값에서 변경하지 않았다면 웹주소창에 192.168.0.1로 들어가면 관리자 모드에 접속할 수 있다.

이를 통해 새롭게 추가된 ip를 확인하도록 하자.



### PUTTY 설치

뭐 이렇게 해야하는게 많는가 싶겠지만 이제 마무리단계이다

PUTTY를 설치하자 

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

해당 URL에서 본인의 운영체제에 맞는 걸 설치해주도록하자

설치 후 putty를 실행시켜 아까 알아낸 ip를 입력 후 open을 눌러준다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527330/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_9_myc1bi.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527330/200515posting/이미지_9_myc1bi.png)

login as 라고 뜰때의 초기 설정값은

```
ID : pi
PW : raspberry
```

이다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527546/200515posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_10_os7zrs.png](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589527546/200515posting/이미지_10_os7zrs.png)

위 화면이 떴다면 성공이다.