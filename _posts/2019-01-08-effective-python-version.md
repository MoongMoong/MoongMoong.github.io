---
title: [effective python] 01. 우분투 파이썬 버전 (Ubuntu18.04 Ubuntu16.04 python version)
layout: post
date: '2019-01-08 19:33:36'
excerpt: 마크다운에 이미지를 쉽게 올리자
comments: true
tag:
- python
- ubuntu
- effective python
categories:
- effective python
---

## 파이썬의 버전을 찾는법.

파이썬은 버전에 따라서 조금씩 함수가 달라질 수 있다.  
특히 Python2와 Python3은 큰 차이를 갖는데 실수하지 않도록 버전을 항상 확인하자.  
특히 모듈을 잘못 설치할 수 있으니 조심하자.  

다음은 터미널에서 사용가능한 명령어이다.  
각각 python2, 3용 명령어이다.  

	python --version
	python3 --version

다음은 파이썬 코드 내에서 버전을 얻는 방법이다.
sys모듈을 이용한다.

	
	import sys
	print(sys.version_info)
	print(sys.version)
