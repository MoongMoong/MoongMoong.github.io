---
title: [effective python] 01. 우분투 파이썬 버전 (Ubuntu18.04 Ubuntu16.04 python version)
layout: post
date: '2019-01-08 19:33:36'
excerpt: 마크다운에 이미지를 쉽게 올리자
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

다음은 터미널에서 

	

사용 예시이다.  
위는 source파일을 50퍼센트로 작게 리사이즈해서 dest에 저장.  
아래는 source파일을 1024*768 사이즈의 이미지로 리사이즈해서 dest.jpg에 저장  
개인적으로는 %시 사이즈 끝자리가 제어되지 않아서 아래의 방법을 선호한다.  
	
	convert  -resize 50% source.png dest.jpg
	convert -resize 1024X768  source.png dest.jpg
