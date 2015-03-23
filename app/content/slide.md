class: center, middle

# [ 휴봇 ]

당신의 개발친구 ✋

![hubot](img/hubot_no_balloon.png)

---
.left-column[
  ## @김경열
]
.right-column[
  [https://github.com/chitacan](https://github.com/chitacan)

  - 덕후회사 `Riiid` 의 개발자

  - `github`, `android`, `node.js`, `angular.js`, `react.js`, `d3.js`

  - brownbreath

  - 지금은 `ruby on rails` 와 씨름 중 🚀
]

---
background-image: url(img/renote_back_color_none.jpg)
.left-column[
  ## 김경열
  ## 뤼이드??
]

.right-column[

- 오답노트 서비스 [renote](https://play.google.com/store/apps/details?id=co.riiid.renote)를 개발하고 있습니다.

- 안드로이드 : 서비스 중 🙌

- iOS : 준비 중 🙇

.fit[![app-image](img/renote.png)]
]

---
class: center, middle

# 휴봇?

`깃헙` 이 만든 오픈소스 채팅 봇 🙋

[https://github.com/github/hubot](https://github.com/github/hubot)

![hubot](img/hubot_no_balloon.png)

---
.left-column[
  ## 채팅봇?
]

.right-column[
깃헙은 자신들의 채팅 서비스(campfire) 에 채팅봇을 띄워놓고 재미난 일들을 시킵니다.

  - 웃긴사진, 고양이 사진 가져오기

  - 나의 위치를 지도에 표시하기

  - 간단한 단위 변환, 번역 등...

.fit[
![hubot-dangerroom](https://hubot.github.com/images/screenshots/dangerroom-full.png)]
]

---
.left-column[
  ## 채팅봇?
  ## 챗옵스?
]

.right-column[

재미를 위해서만 사용하지 않습니다. 깃헙의 전체 인프라 스트럭쳐(코드, 배포, 테스트, 성능측정등) 를 컨트롤 하는 일들을 시킵니다. 이 모든 일들은 채팅창에서 이루어 집니다. 👍

<iframe width="560" height="315" src="https://www.youtube.com/embed/-LxavzqLHj8?start=150&rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

휴봇을 활용해 공통된 작업을 자동화 하는 패턴을 `ChatOps` 라 부릅니다.
]

---
.left-column[
  ## 채팅봇?
  ## 챗옵스?
  ## 왜?
]

.right-column[

- 무슨일이 벌어지는지 모두가 볼 수 있습니다. (입사 첫날에도!! 💄)

- Teaching by doing, Communicate by doing

- 모바일로 전환하기 쉽습니다.

- 채팅창 인터페이스는 누구에게나 익숙합니다. (`@hubot help`)

.fit[
![chat-interface](img/chat_interface.png)
]
]

---
class: center, middle, inverse1

# 시작하기

`$ npm install -g yo generator-hubot`

.pull-right[![hubot](img/hubot_no_balloon.png)]

---
class: inverse1
.left-column[
  ## 시작하기
]

.right-column[

스캐폴딩 도구 `yo` 를 활용해 새로운 `hubot` 을 생성할 수 있습니다.

```
$ npm install -g yo generator-hubot
$ mkdir wall-e && cd wall-e
$ yo hubot
```

```xml
                     _____________________________
 _____              /                             \
 \    \             |   Self-replication process   |
 |    |    _____    |          complete...         |
 |__\\|   /_____\   \     Good luck with that.    /
   |//+  |[^_/\_]|   /----------------------------
  |   | _|___@@__|__
  +===+/  ///     \_\
   | |_\ /// HUBOT/\\
   |___/\//      /  \\
         \      /   +---+
          \____/    |   |
           | //|    +===+
            \//      |xx|
```

```
$ ./bin/hubot
...
wall-e> wall-e ping
PONG
```
]

---
class: inverse1
.left-column[
  ## 시작하기
  ## 어댑터?
]

.right-column[

다른 채팅 서비스(`hipchat`, `slack` 등) 에 연결하고 싶다면, `adapter` 를 설치해야 합니다.

```xml
$ npm install hubot-slack --save
$ ./bin/hubot --adapter slack
```

[https://github.com/github/hubot/blob/master/docs/adapters.md](https://github.com/github/hubot/blob/master/docs/adapters.md)
.fit[
![adapter](img/adapter.png)
]
]

---
class: inverse1
.left-column[
  ## 시작하기
  ## 어댑터?
  ## 확장하기
]

.right-column[
`scripts` 디렉토리의 `*.js`, `*.coffee` 파일을 자동으로 로드합니다.

```javascript
// scripts/hey.js
module.exports = function(robot) {

  robot.hear(/hey/i, function(msg) {
    msg.send('hey there');
  });

  robot.hear(/YOUR_REGEX/i, function(msg) {
    // YOUR_HACK_RESULT
  });

}
```

```xml
$ ./bin/hubot
...
*wall-e> hey
hey there
```

[https://github.com/github/hubot/blob/master/docs/scripting.md](https://github.com/github/hubot/blob/master/docs/scripting.md)

]

---
class: center, middle, inverse2

# 활용하기

![hubot](img/hubot.png)]

---
class: inverse2
.left-column[
  ## 이미지
]

.right-column[
이미지를 보낼 필요 없습니다. `url` 만 있으면 됩니다. ([hubot-google-images](https://github.com/hubot-scripts/hubot-google-images))

  - 아이돌과 함께 출근 (`@hubot <IDOL> 출근`)

![iu](img/work_with_iu.gif)
]

---
class: inverse2
.left-column[
  ## 이미지
]

.right-column[
이미지를 보낼 필요 없습니다. `url` 만 있으면 됩니다. ([hubot-google-images](https://github.com/hubot-scripts/hubot-google-images))

  - 아이돌과 함께 출근 (`@hubot <IDOL> 출근`)

  - 나의 병맛 기분을 이미지와 함께 (`@hubot img 아오빡쳐`)

![shit](img/shit.png)

  - 차트로 정보 공유하기 ([google image charts](https://developers.google.com/chart/image/), [brown](https://github.com/chitacan/brown))
]

---
class: inverse2
.left-column[
  ## 이미지
]

.right-column[
이미지를 보낼 필요 없습니다. `url` 만 있으면 됩니다. ([hubot-google-images](https://github.com/hubot-scripts/hubot-google-images))

  - 아이돌과 함께 출근 (`@hubot <IDOL> 출근`)

  - 나의 병맛 기분을 이미지와 함께 (`@hubot img 아오빡쳐`)

  - 차트로 정보 공유하기 ([google image charts](https://developers.google.com/chart/image/), [brown](https://github.com/chitacan/brown))

![chart](img/chart.png)
]

---
class: inverse2
.left-column[
  ## 이미지
  ## 도와주기
]

.right-column[
필요한 정보를 휴봇을 통해 얻을 수 있도록 가공하기.

  - 디버깅 정보 (`@hubot debug`)

  - 그룹에 필수 링크들?(`@hubot link`)

  - 지금 사무실에 있는 사람들?(`@hubot slave`)
]

---
class: inverse2
.left-column[
  ## 이미지
  ## 도와주기
  ## 자동화
]

.right-column[
반복되는 모든것을 휴봇으로 자동화하기.

  - 집에있는 컴퓨터 켜기

.fit[![power_ip](img/power_up.png)]

```xml
hubot> hubot power chitacan-pc up
hubot> hubot power chitacan-pc down
```

  - `vagrant` 프로젝트 실행 ([hubot-vagrant](https://github.com/chitacan/hubot-vagrant))
]

---
class: inverse2
.left-column[
  ## 이미지
  ## 도와주기
  ## 자동화
  ## 두뇌이식
]

.right-column[

지식을 갖추고 있거나, 저장할 수 있는 서비스를 연결해 봅시다.

  - `wolfram alpha` : [advanced-wolfram.coffee](https://github.com/RedRibbon/redribbot/blob/master/scripts/advanced-wolfram.coffee)

```xml
*hubot> what is your name
My name is Wolfram|Alpha.

*hubot> hubot what is your age
5 years 10 months 5.851 days
(right now)
```

  - `firebase` : [idols.coffee](https://github.com/RedRibbon/redribbot/blob/master/scripts/idols.coffee), [auto-react.coffee](https://github.com/RedRibbon/redribbot/blob/master/scripts/auto-react.coffee)

```xml
*hubot> hubot 아이유
:mag: 아이유 레전드... I have found the thing.
http://cfile239.uf.daum.net/image/2553513F52CA3F27206045#.png

*hubot> hubot idol add 하니
*hubot> hubot 하니
:mag: 하니 움짤... I have found the thing.
http://t1.daumcdn.net/thumb/R400x0/?fname=http://cfile246.uf.daum.net/image/242DFD4154C8AF7D02ED37#.png
```
]

---
class: center, middle, inverse3

# 휴봇

모든것을 자동화 합시다!!

![hubot](img/hubot_no_balloon.png)

---
class: center, middle

# Q & A

![hubot](img/profile.png)

