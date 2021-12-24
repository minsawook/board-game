# Board-Game
<h2>임베디드 시스템을 활용한 인터렉티브 보드게임</h2>

팀원 : 김이영, 남시우, 민사욱, 정세미, 지준, 황민상



https://user-images.githubusercontent.com/92355477/147327299-ceab6d2a-9145-4603-8888-e116b9f87ea5.mp4



<h2>1. 과제의 목적 </h2>
- 보드게임의 게임 말 및 주사위 등을 아두이노의 기능을 통해 게임진행을 자동화함으로서 편리성 및 휴대성을 향상시킴. 
- 기존 보드게임을 진행하며 발생할 수 있는 문제점(점수계산 실수)을 아두이노를 접목함으로써 해결.
- 아두이노와 flutter을 연동하여 편하게 게임을 즐길 수 있게함

<h3>작품 구성도</h3>
아두이노

 ![1](https://user-images.githubusercontent.com/92355477/147326372-fde02bc5-9488-4814-805a-efbe658387cc.JPG)


flutter앱

![2](https://user-images.githubusercontent.com/92355477/147326378-59e257e3-dfaa-4c0e-8d84-c32e621605d1.JPG)

<h3>사용 기술 스택</h3>

frontend: flutter
db : firebase
arduino : 시리얼 통신, esp32,

<h3>결과물에 대한 요약 설명</h3>

arduino(보드판)

- 출발칸으로부터 한바퀴를 먼저 돌아오는 사람이 승리하는 3인용 보드게임.
- 3가지의 LED 색으로 플레이어를 구분함.
- 빨간색, 노란색, 초록색 순으로 플레이어 이동.
- 사용자가 랜덤 주사위 버튼을 누르면, 아두이노 시리얼 모니터 화면에 1~6까지의 숫자가 랜덤으로 출력.
- 구분된 LED 색 순서대로(빨간색-노란색-초록색) 랜덤 숫자만큼 LED가 이동함 
- 스마트폰 어플리케이션을 와이파이 모듈로 연동하여, 현재 게임 진행 상황을 저장함.

flutter(앱)
- 핸드폰과 firebase를 연결
- 플레이어 선택하면 firebase에 파이어베이스에 플레이어 정보를 저장하여 플레이어 중복 선택을 방지
- 주사위 값 1~6사이의 랜덤값을 생성후 플레이어 위치 변동
- 플레이어가 위치가 움직이면 주사위 값과  위치에 맞는 이벤트정보를 화면에띄움
