---
title: 우분투 이클립스 설치(Install eclipse in ubuntu for c++)
layout: post
date: '2019-01-04 09:33:36'
excerpt: 우분투에서 이클립스를 설치하는 방법
categories:
- Ubuntu
comments: true
tag:
- Ubuntu
- c++
- eclipse
---

### 오늘은 C++ 스터디를 위하여 이클립스를 설치해보려 한다.
원래는 Eclipse가 java에 주로 사용되는 ide로 알고 있었는데 c++ 확장이 가능한 것을 이번에 알게 되었다. 

Eclipse를 설치하기 위해서 [이 블로그](https://agiantmind.tistory.com/182).를 참조하였다.

사실상 거의 복붙이긴 하지만.. 일단 작성해보자
원본이 아주 잘 설명해 주었으니 순서만 정리한다.

### 설치 순서는 다음과 같다.

1. JDK(Java Development Kit) 설치 
2. C/C++ 개발 관련 패키지 설치 
3. Eclipse 설치 
4. Eclipse CDT 설치

> #### JDK 설치

	sudo add-apt-repository ppa:webupd8team/java
	sudo apt-get update
	sudo apt-get install oracle-java8-installer

>#### C/C++ 개발 관련 패키지 설치

	sudo -s
	sudo apt-get install build-essential

>#### Eclipse 설치

운영체제 아키텍쳐 확인
	uname -m

| 32비트 | 64비트 |
|:-------:|:-------:|
| i386, i486, i586, i686, x86   |  amd64, x86_64   |
{: rules="groups"}

해당 정보에 맞춰서 Linux version으로
[Eclipse 공식 사이트](https://www.eclipse.org/).에 접속하여 
"Eclipse IDE for C/C++ Developers" 다운로드

* 다운받은 경로로 이동 후 압축 헤제

		tar xvzf (다운받은파일명)

* Eclipse 폴더를 /opt 폴더로 이동 

		sudo mv eclipse /opt

*  터미널 실행설정


		sudo vi /usr/bin/eclipse

혹은

	sudo gedit /usr/bin/eclipse

여기에 다음을 작성한다.

	#! /bin/sh
	export ECLIPSE_HOME=/opt/eclipse
	$ECLIPSE_HOME/eclipse $*

권한 설정을 한다

	sudo chmod 755 /usr/bin/eclipse

X 윈도우 바로가기 설정을 위해 다음 중 하나로

	sudo vi /usr/share/applications/eclipse.desktop
	sudo gedit /usr/share/applications/eclipse.desktop

아래를 작성한다.

	[Desktop Entry]
	Encoding=UTF-8
	Name=Eclipse
	Comment=Eclipse IDE
	Exec=eclipse
	Icon=/opt/eclipse/icon.xpm
	Terminal=false
	Type=Application
	Categories=Development
	StartupNotif=true
	
	
>  #### Eclipse CDT 설치

지금부터 좀 했갈릴 수 있다.. 여지간하면 직접 이미지 도용은 안하는게 좋겠지만.. 
추후에 문제가 될 것 같으면 이미지 수정하도록 하겠습니다.

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile27.uf.tistory.com%2Fimage%2F245DBB4A5938F77C0BFDDA)

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile29.uf.tistory.com%2Fimage%2F22400F4A5938F77D17E737)

리스트에 없으면 Add 누르고

	#http://download.eclipse.org/tools/cdt/releases/9.2

직접써줘야한다.. 복붙하세요.

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F2279A44E5938F7AD38D4E0)

위에 두가지 다 설치(9.6버전은 한개 더 있는데 잘 모르겠다.)


>  #### 샘플 코드

샘플 프로젝트 만들기는 다음처럼 하면되는데, 

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile4.uf.tistory.com%2Fimage%2F267C7F485938F7F5247A5E)

실제로 프로그램 짤때는 2번째 이미지에서 선택할 때,  **Empty project**를 선택하자

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile3.uf.tistory.com%2Fimage%2F234498485938F7F60BEEDA)

C++은 빌드를 해줘야한다. (최근 python만 쓰다보니 이걸잊었었는데..)

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile30.uf.tistory.com%2Fimage%2F2776814E5938F812260DE2)

Hello world를 consol에서 확인할 수 있다.

![텍스트](https://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile25.uf.tistory.com%2Fimage%2F2563C64D5938F82A0E0C98)
