## 비동기화 크롤링 2편 예제



### 이어서

우리는 저번 시간에 동기화는 무엇이고 비동기화는 무엇인지 느낌만 알게되었다.

본인은 비전공자이며 필요에 의해 비동기화 기능을 추가하여 프로그램을 만드려는 사람이므로 본인이 전공자이고, 더 깊은 내용의 지식을 원한다면 이 포스팅을 안 보는걸 추천한다.

또한 예제는 https://sjquant.tistory.com/14?category=797018 이곳에서 그대로 가져왔다.

![img](https://dojang.io/pluginfile.php/14098/mod_page/content/7/047003.png)

### 비동기화란?

위의 그림에서 볼 수 있듯 직관적으로 동기처리는 시간이 더 오래 걸린다.

여기서 비동기화에 필요한 이벤트루프라는 친구를 살펴보자



### 이벤트루프(Event Loop)

사실 이는 좀 로우레벨에서 돌아가는 복잡한 개념이므로 느낌만 잡자면 비동기 처리 방식에서 

1. 작업 1을 실행한다.
2. 작업 1에게 주도권이 넘어간다.
3. 작업 1이 정해진 시간동안 작업을 끝내지 못했다.
4. 다시 이벤트 루프에게 주도권을 넘겨준다
5. 이벤트 루프는 다시 뽈뽈거리며 돌아다닌다.

마치 잠겨진 방안에서 인터뷰어들을 끊임없이 인터뷰하는 기자와 같은 역할이 이벤트 루프이다.

### 코루틴 (coroutine)

이벤트루프가 전체적인 루프라면 코루틴은 어떤 인터뷰어를 만났을때의 함수를 의미한다.

파이썬에서 코루틴이 아닌 일반적인 함수는 서브루틴이라 한다.

![https://res.cloudinary.com/dbzvbzksw/image/upload/v1589705014/200517posting/%EC%9D%B4%EB%AF%B8%EC%A7%8010_byb2v2.jpg](https://res.cloudinary.com/dbzvbzksw/image/upload/v1589705014/200517posting/이미지10_byb2v2.jpg)

### asyncio 모듈

파이썬에서 비동기를 사용할 수 있게해주는 모듈이다.

함수 앞에 **async**를 붙이면 코루틴을 만들 수 있다.

또한, 다시 통제권을 반환 할때 **await** 를 붙인다.



### 기초

```python
import asyncio
import time

# 1. Coroutine 정의
async def sleep():
    await asyncio.sleep(10)
# coroutine sleep 이라는 함수는 sleep이라는 함수를 병목이 발생할 경우 주도권을 넘겨줍니다.

start=time.time()
#2. Event loop 정의
loop=asyncio.get_event_loop()
#3. Event loop를 sleep함수가 완료 될때까지 실행시킵니다.
loop.run_until_complete(sleep())
end=time.time()
print(str(end-start)+'s')
```

### 비동기적 처리 (2개이상의 coroutine)

```python
import asyncio
import time


async def coroutine_1():  # 코루틴 정의 (async를 앞에 붙여준다.)
    print('코루틴 1 시작')
    print('코루틴 1 중단... 5초간 대기')
    # await으로 중단점 설정 (블락킹되는 부분에서 사용)
    await asyncio.sleep(5)
    print('코루틴 1 재개')


async def coroutine_2():
    print('코루틴 2 시작')
    print('코루틴 2중단... 4초간 대기')
    await asyncio.sleep(4)
    print('코루틴 2 재개')

if __name__ == "__main__":
    # 이벤트 루프 정의
    loop = asyncio.get_event_loop()

    start = time.time()

    # 두 개의 코루틴을 이벤트 루프에서 돌린다.
    # 코루틴이 여러개일 경우, asyncio.gather을 먼저 이용 (순서대로 스케쥴링 된다.)
    loop.run_until_complete(asyncio.gather(coroutine_1(), coroutine_2()))
    end = time.time()

    print(f'time taken: {end-start}')
```

### asyncio.sleep을 활용한 비동기

```python
import asyncio
import sqlite3
import time


async def sleep():
    await asyncio.sleep(1)


async def main():
    # asyncio.sleep은 아무리 많아져도 비동기적으로 잘 돌아간다.
    futures = [
        asyncio.ensure_future(sleep()) for i in range(10000)
    ]
    await asyncio.gather(*futures)


if __name__ == "__main__":
    start = time.time()
    asyncio.run(main())
    end = time.time()
    print(f'{end-start}')
```







### 레퍼런스

[1]: https://sjquant.tistory.com/14?category=797018 파이썬과 비동기 프로그래밍

[2]: https://dojang.io/mod/page/view.php?id=2469 파이썬 코딩도장

