# 자바스크립트 동작 순서

[참고자료](https://www.youtube.com/watch?v=v67LloZ1ieI)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/9f4fe495-e2ce-4d7c-b914-e8b439632aaf.png)

그런데 자바스크립트를 해석하는 순서가 조금 생각하는것과 다르다

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/a66a2678-0b22-4355-bed5-f8677d66883a.png)

만약에

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/d66c8a85-9c70-434a-90a6-77b05dd64565.png)


이러한 코드를 작성하고싶다고하면


python 으로 작성한다고 하면

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/6a78eff0-5610-46d3-8fb0-5bb886ff4c1d.png)


위에서부터 한줄한줄 실행하게 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/eaa044f7-5792-43d4-8eae-8d6118de1eb7.png)


이런식으로 실행이 되는데


그래서 자바스크립트로 작성을 해보게 되면

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/193ad94d-b6a3-4db1-9dec-fd201e54f23e.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/7defd01d-79d8-4bf5-805e-f97b9474babb.png)


자바스크립트는 그냥 쉬지않고 바로 실행이 된다.


왜일까 ?? 그럼 어떻게 작성을 해야할까??

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/dfc8f462-6db8-4d88-a498-bcbb8175eff0.png)


이렇게 작성을 해야한다.


그리고 그 밑에 3+3 이란 코드를 작성하게 되면

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/2475a940-b93a-4e85-9d9a-60483b8229d8.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/a948e434-1dcc-4d0c-9796-ca7b940b04b3.png)


3+3 코드가 바로출력이 되고 , 그다음에 1초 쉬고 2+2 가 출력이된다.


여기서 조금 이상한점이 있는데 , 우리가 생각하는 프로그램 동작 하는 원리랑 살짝 다르다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/78a5690a-f409-45d9-9d99-40584b5425d1.png)


이것을 보고 생각이 드는것이 자바스크립트는 병렬처리가 되는 언어인가 ?? 라는 생각이 들 수 있다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/c6aa893d-4d39-44c8-888d-c6264ae0fe94.png)


사실 병렬처리는 아니다 .

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/49817690-d49b-4ff2-a0a1-23b1ee31c5d9.png)


그럼 무엇일까 ??

# 동작원리


우리는 웹 브라우저를 많이 사용한다


웹브라우저는 우리가 자바스크립트로 코드를 짠것을 실행을 해주는 엔진이라고 보시면 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/def85d8d-2353-4990-8b63-29f2d8afe48d.png)


stack 이라는 공간이 있다.


스택이라는 공간안에다가 한줄한줄 실행을 해줘야한다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/8d5bb258-4de5-44b6-ba96-c78aa0d2f508.png)


우리가 작성한 코드를 stack 이라는 공간에 한줄한줄 넣게 된다.


그리고 한줄한줄 실행하게 된다.


그런데 실행을 하다보면 우리는 변수들을 사용하곤하는데 ,

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/c61a76a7-8ef2-435f-98ce-8034c72a5336.png)


stack 실행하는 도중에 변수를 만나게 되면 그 변수를 Heap 이라는공간에서 변수를 찾게된다.


그래서 Heap 이라는 공간에서 i 를 찾아서 가져다가 사용하고 합니다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/1e1ac16a-0179-4d70-9464-cb165e1694a8.png)


이러한 Stack 은 오로지 하나만 존재한다.


그래서 한번에 한줄밖에 코드를 실행하게 된다.


이것을 우리는 싱글스레드라고한다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/8b1d4650-8e05-495a-b509-d1a5defc4207.png)


그런데 우리가 아까봤었던 setTimeout 이라는 코드는 어떻게 되는걸까 ?

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/11e278ec-fc56-46e3-b2a8-3082368ce4d6.png)


바로 실행할 수 없는 코드이다.


이 코드는 1초 후에 실행을 해야하는 코드이다.


그래서 이 코드는 잠깐 대기실로 이동을 한다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/f64fb848-8480-4830-b9ca-d02f5dcad846.png)


그리고 실행을 한줄씩 한다고 보면 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/35243804-a466-4b88-949d-6965478350ce.png)

보통 이렇게 대기실로 가는 코드들은 어떠한 코드들이다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/fd0dbe63-a0b7-4daa-bb0f-6713c9afcd59.png)


보통 백에서 데이터를 받아올때 작성하는 Ajax 코드 와 이벤트 리스너 코드


그래서 대기실에 있다가 이제 이코드가 실행할때가 됬다고 하면 다시 스택으로 가야겠죠 ??

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/bb6c8e4b-6aff-4fab-923a-f2c201e3d108.png)

그런데 이때 바로 스택으로 가지 않는다.

# Queue


바로스택으로 가지않고 , Queue 라는 대기실이 있는데 여기에 처리가 완료된 코드들을 줄 세우게 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/3884547a-9ba3-494d-ba3e-a493b947e088.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/bb41991e-7dba-4d03-9eab-3874d58a4c7c.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/b3feaecd-482a-4cc0-a7ce-119fe4ed63bb.png)


이렇게 하나씩 스택으로 보내게 된다.


근데 이 Queue 가 왜 필요하지 ?? 바로 Stack 으로 보내면 안되는걸까 ?


원래 Stack 이라는 공간은 바쁜공간이라서 그렇다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/ca5d1693-9344-4573-b142-5727abfc858c.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/e7ff4d9d-9d98-47f6-89c1-0843b847a0e6.png)


그리고 Queue 에서 Stack 으로 무작정 보내지 않고 Stack 에 공간이 비어있을때 Queue 에서 하나씩 올려 보낸다.


그래서 우리가 처음에 봤던 예시를 다시 보게되면 ,

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/133732e3-72d3-4c4d-8e15-96b6767cd6d6.png)


제일 위에있는 코드가 실행된다.


그리고 setTimeout 코드가 대기실로 이동한다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/f82a810b-e59b-48fc-9d37-3a660e5df54a.png)


그리고 밑에줄을 실행하게 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/22f946f5-7270-4749-be36-39bf3fecabd3.png)


그래서 콘솔창을 찍어보게되면 , 1+1 과 3+3 결과값이 먼저 찍히게 된다.


그리고 대기실에 있던 setTimeout 함수는 이제 1초뒤에 Stack 으로이동하는데 그냥 이동하는것이 아니라

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/66eaebb2-769e-4f53-a46f-1788f6bc8d73.png)


Queue 를 거쳐서 Stack 으로 이동하게된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/78ef30ad-88bd-42f6-9d7d-3bd9dc4e15a8.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/35eabaa6-be22-4fe5-99da-4eeb9b83f5ac.png)


그래서 이러한 순서로 동작한다고 보면 된다.


# 문제

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/830d312a-e845-4bc2-9317-8ac623e7a882.png)


만약에 setTimeout 에 0초라고하면 어떻게 될까 ?

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/bae8556b-3080-4476-9bcc-d54d5e0a5a81.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/00bd9d33-7ed9-44ad-b3f7-1717d77f81f6.png)


왜그런갈까?? 조금 이상하다 setTimeout 이긴한데 대기시간을 0 초로 했으면 바로 실행하는것이 아닐까?? 생각이 들수도 있다 하지만 그렇지 않다.


아까 위에서 봤지만 무조건 대기실로 이동하게 된다.


setTimeout 이라던지 Ajax 라던지 이벤트리스너는 무조건 대기실로 이동하게되어있다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/d6072d1a-c095-4a78-af50-4cd9c43bb8f3.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/16d5632e-5223-4557-942a-6a38a963897a.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/a32918f5-beaf-43a6-ab4d-4de1975e33d2.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/307cb93d-6161-4fd3-a9d6-f3c9656792e8.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/06b32f03-eafa-4e1c-b7d8-d07f2a89d1a7.png)


그런데 이러한 원리를 왜 알아야해 ??


그냥 우리가 코드 적은대로 실행이 될텐데 왜 알아야할까 ??


예를들어서


반복문을 우린 자주 사용하게 되는데

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/e02dd0a6-9c94-4ea2-9d36-9de33a86b669.png)


간단한 반복문이라던지 그런것은 자바스크립트로 짜도 별 문제가 없을것이다.


하지만 자바스크립트로 어려운 수학계산을 시키게 되면 안된다.


그러면 우리가 아까 배웠던것처럼

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/abc53d67-1697-4d98-bc84-30a064e9faab.png)


stack 에서10초간 실행이 된다.


그런데 이러한 10초동안 만약에 연산을 하고있는 도중에


ajax 데이터를 받아온다거나 이벤트리스너가 발생하게 되면 어떻게 될까?

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/b327f176-9f9e-418c-a929-43c4caaba453.png)


작동이 안된다.


예를들어서 버튼을 누르게 되면 모달창이 보이는코드가 있다고하면

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/b10d6c56-ea6e-4c82-9561-cd0ebb4e97fd.png)


그런데 모달창이 안보인다. 왜냐면 대기실로있는것은 Queue 로 갔다가 Stack 이 비어진상태에서 Stack 으로이동해서 실행이 될테니깐

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/c9f795fa-8275-4ad7-a11f-4b3581cce5fb.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/413fb8ce-66e3-40db-86bd-4e9deb73db8a.png)

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/5caf98c3-9a5c-4bc0-a5f9-7ac7310b5ed6.png)


실제 이게 브라우저에서 보게되면 ,

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/f2fbef90-4818-4a7e-ae21-e3a88834d070.png)


이렇게 대기버튼이라던지 나오게 된다.


그래서 이번시간에 우리가 가져가야할 요약점은

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/f3910d0a-8b8e-4a0d-b524-17e3ffae7384.png)


그리고 자바스크립트는 동기적이다 비동기적이다 이런 얘기를 많이하는데요.


자바스크립트는 사실 동기적이다.


한번에 한줄 순서대로 코드가 실행하게 된다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/66bf850f-86d6-4e2d-8541-63f493a6d0dd.png)


그런데 자바스크립트는 가끔 비동기적인 처리도 할 수 있습니다.

![자바스크립트 동작원리 image](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/38ffd16e9af04092b387435533958b1a/23bd06e3-bec6-4eae-bb70-9789f7019e22.png)

