# 개발자 김재동 랜딩 페이지
#### Dev. Jade Kim Landing Page
##### [>> Git Blog Link <<](https://JadeKim93.github.io) 공사중
---------------------------------------


### 1. 간략 소개
* 1993년 생 남자
* 한양대 에리카 전자시스템 공학 학부 졸업
* 개발 언어: C, C++, C#, python
* 개발 환경: Embedded, Ubuntu, Windows
* 그 외: KiCad, Altium, ROS ... 
* 3 번째 스타트업 재직 중

### 2. 개발 경험
* 회로 설계. BLDC 드라이버 설계 경험 있음. 상품화 X
* 네비게이션 백엔드 프로그램
* 의족 메커니즘 시뮬레이션
* TDOA 기반 위치 추정 알고리즘 디버그 및 시뮬레이션
* 전반적인 코드 최적화

### 3. 참여 프로젝트
* 모바일 로봇 개발 ( 회로, 전장, 펌웨어, 드라이버 )
* 순수 펌웨어로 개발된 CAN 통신 기반 AGV 제어 ( 6 개 모듈, 1 Mbps )
* 지하 주차장 충전 로봇


### 4. 인사이트
#### 4.1 2021년 11월
짧은 개발 인생이었지만, 다수의 프로젝트에서 제가 느껴본 바, 문제점과 원인을 나열하자면 아래와 같습니다

1. 사는 게 바쁩니다. 인생은 짧고, 연애도 해야하고, 일도 해야하고, 공부도 해야합니다.    
일반적으로 4년제 대학을 나온 남자가 현업에 머물면서, 20대에 이 모든 것을 다 이루기는 어렵고,   
특히 이론을 정확하게 알고 있더라도 구현을 하는 방법이 잘못된 경우가 허다합니다.

2. 매번 새로운 프로젝트가 생기고, 사라집니다. 디자인 패턴이 학문적으로 정형화 되어 있다지만, 매번 프로젝트의 요구에 따라 하드코딩 되거나, 재사용이 어려운 경우가 많습니다    
예전에 본인이 개발했던 코드가 어렴풋이 기억나서, 그대로 긁어와 적용해도 제대로 동작하지 않는 문제가 생깁니다.

3. 서로 다른걸 보고 들어온 많은 사람이 하나의 목표를 갖고, 하나의 프로젝트에 투입됩니다.   
코드 컨벤션만으로는 모든것을 통제할 수 없습니다.

4. 매번 효율적인 알고리즘을 생각해 낼 수 없습니다. 그리고 효율과 구현방법을 고민하다 보면, 정작 결과물의 퀄리티가 떨어집니다. 또한 어설프게 알고 만든 알고리즘은 갖은 버그와 최적화 문제에 시달리게 될 수도 있습니다.

	```
	사람이 5명이나 모이면, 반드시 1명은 쓰레기가 있다 - 지보로. 나루토 中 에서
	```
개발하고, 문제에 봉착하고, 다시 개발하는 악순환이 반복되면서, 몇 가지 드는 생각이 있었습니다.
* 프로젝트가 원활히 진행되려면, 모든 코드가 한 사람이 짠 코드 처럼 유기적으로 동작하고, 구성원 중에서 누구라도 코드의 구조를 간파할 수 있어야 한다.
* 하지만 그건 사실상 불가능 하다. 내가 아는 것을 모두 남에게 알려주기엔 물리적인 시간과 노력이 너무 많이 들어가고, 상대방의 나이가 나보다 많으면 그걸 받아들이는 것 또한 자존심이 상할 것이다.
* 내가 라이브러리를 구성해서 환경을 만들어 보는것은 어떨까?
라이브러리를 구성하고 수정 권한을 나만 갖고 있으면, 몇 가지 이점을 확보할 수 있다
    
    * 한 사람이 짜기 때문에 전체적인 코드의 통일성을 유지할 수 있다
    * 내가 기획한 라이브러리의 구조와 의도를 문서화 할 수 있다
    * 나보다 더 고수가 나타나면, 혹은 여러사람이 검토하면서 구조의 문제점에 대해 피드백을 받을 수 있다
    * 완벽하진 않겠지만, 헤더가 함부로 바뀌지 않으니 유지보수가 용이하다
    * 누군가 필요에 의해 라이브러리를 바꾸는 경우를 차단할 수 있다. 이런 하드코딩은 정말 짜증난다!
    * 이 라이브러리를 사용하는 사람 한테는 충분한 문서화를 통한 설명을 제공한다. 그리고 개발자는 마치 레고블럭을 끼워 맞추는 처럼 개발을 할 수 있을 것이다.

이런 동기부여로, 라이브러리를 만들기로 생각했습니다.
