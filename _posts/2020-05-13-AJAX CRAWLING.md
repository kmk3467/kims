# AJAX 기반 크롤링 

### 접근성이 엄청난 셀레니움

게임홈페이지 로그인을 해주는 크롤러를 만들고자했다.

처음에는 셀레니움을 이용한 프로그램을 짰다 

```python
from selenium import webdriver
import time
import requests
ide=[]
pw=[]
driver=[] 
ide.append('id')
pw.append('pw')
options = webdriver.ChromeOptions() 
webdriver.Chrome('C:\download\chromedriver_win32\chromedriver.exe',options=options)
driver.implicitly_wait(4)
for i in range(len(ide)):
    driver.get('http://www.GAMEURL.co.kr/login')
    driver.find_element_by_id('user-id').send_keys(ide[i])
    driver.find_element_by_id('pwd').send_keys(pw[i])
    driver.find_element_by_class_name("btn-login").click()
    driver.implicitly_wait(3)
    time.sleep(0.5)
    alert = driver.switch_to.alert
    alert.accept()
    driver.get(http://www.GAMEURL.co.kr/logout')
driver.quit()
```

셀레니움을 임포트해서 아이디와 패스워드를 입력한 후 이 값을 개발자모드에서 찾아낸 HTML id값으로 찾아 

한다. 

또한 셀레니움은 버튼클릭기능이 구현되어있어 굉장히 편하게 로그인 프로그램을 만들 수 있다.

```python
alert = driver.switch_to.alert
alert.accept()
```

구문은 해당 홈페이지가 로그인 시 팝업이 뜨는 사이트여서 팝업으로 전환하여 확인을 눌러주어야 했다.

그렇지 않으면 그 구문에서 멈춰서 오류가 뜨게 된다.



### 부각되는 셀레니움의 단점 

하지만 셀레니움의 단점은 엄청나게 느린 속도이다. 

만약 불가피하게 셀레니움을 사용해야하는 경우가 아니라면, requests 모듈이 훨씬 쾌적해보였다.

물론 셀레니움도 헤드리스가 돌아가긴 하지만, 헤드리스도 덜 무겁지만 무거운편이며 속도에서 개선은 힘들었다.

그런면에서 request모듈로 다시 한번 짜보았다.

```python
import time
import random
import requests
LOGIN_INFO=[]
LOGIN_INFO.append({
    'user_id': 'id',
    'password':'pw',
    'mode':'12003'
    })

print(LOGIN_INFO)
headers = {'User-Agent' : "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_5) AppleWebKit 537.36 (KHTML, like Gecko) Chrome",
           "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8"    }
for i in range(len(LOGIN_INFO)):
    s.append(requests.Session())
    s[i].headers=headers
    first_page.append(s[i].get("http://www.GAMEURL.co.kr/login",headers=headers))
         login_req=s[i].post('http://www.GAMEURL.co.kr/ajax/_member_process',data=LOGIN_INFO[i])
    print(login_req.status_code,i+1,"번째 로그인 완료")
    print(login_req.request.headers)
    time.sleep(random.uniform(1.2,2.1))
    time.sleep(2)
```

셀레니움 헤드리스 모드를 쓸때나 requests 모듈로 사용할때 주의할 점은 서버가 보기에 내가 이름표를 안단 상태라는 것이다. 누가보아도 크롤러봇이므로 차단당하기 일쑤.

그러므로 위의 코드에서처럼 세션을 얻은 후에 헤더를 반드시 입력해주어야 한다. 마치 옷을 안입고 경찰서 앞을 활보하는 것과 같다. 또한 time sleep이 없었다면 requests 모듈의 속도가 매우 빠르기 때문에 1초에 10번도 수행가능하므로 서버에 방해가 될 수 있다. 

### 가장 어려운 점은 로그인 

사실 가장 까탈스러운 부분이며 모든 홈페이지마다 다르다. 내가 로그인 하려고 한 사이트 같은 경우 AJAX기반의 홈페이지로 어떤 페이지로 인증정보를 넘겨주었는데 그 주소를 알려면 크롬 개발자도구를 써야한다.

F12를 눌러 개발자도구에서 네트워크를 누른 후 로그인을 해보면 

![그림3](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589369676/200513posting/%EC%9D%B4%EB%AF%B8%EC%A7%80_3_j83qw3.png)

_member_process 페이지로 mode가 12003 userid,pw값을 넘겨주고 있는 것을 확인했다.

POST방식으로 전송해주었기 때문에 위의 코드에서 POST방식으로 직접 데이터를 넘겨주면 된다.

```python
LOGIN_INFO.append({
    'user_id': 'id',
    'password':'pw',
    'mode':'12003'
    })
login_req=s[i].post('http://www.GAMEURL.co.kr/ajax/_member_process',data=LOGIN_INFO[i])
```

위 코드가 바로 그것이다.  이것은 홈페이지마다 구성이 다르며 내가 크롤링 하고자하는 홈페이지의 특성은 다음과 같았다. 이 포스팅을 보는 독자라면 그 상황에 맞는 홈페이지 분석이 선행되어야 한다.



### 결론 

왠만하면 셀레니움 쓰는게 낫다. 셀레니움이 서버에 차단될 일도 없거니와 (헤드리스모드 제외) 느려서 서버에 부하도 덜준다. 하지만 역으로 느려서 속터지기도 하며, 짧은 시간에  연산을 해야하는 크롤링이나 아주 많은 양을 크롤링 해야 할때 request 모듈을 사용해야 한다.  

request모듈은 빠르지만 홈페이지의 분석이 선행되어야 하고, 혹여나 보안이 좋은 홈페이지라면 정말 답 없을 수도 있다. 또한 동적홈페이지라면 출력이 안된 상태에서 정보를 받아오는 request모듈은 통하지 않는 경우도 존재한다. 하지만 더 본질적으로 크롤링 하는 것은 request모듈이라는 생각이 들었다.(난이도도 높고)

다음에 기회가 된다면 셀레니움으로 세션을 얻어 시작하고 중간 필요한 부분에 request모듈을 사용하는 하이브리드 형식도 사용해보고 싶다.

끗.

