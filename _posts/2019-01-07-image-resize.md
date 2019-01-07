---
title: 우분투 이미지 리사이즈 (Ubuntu18.04 Ubuntu16.04 image resize)
layout: post
date: '2019-01-07 09:33:36'
excerpt: 마크다운에 이미지를 쉽게 올리자
tag:
- markdown
- image
- github
categories:
- ubuntu
---

## 이미지를 리사이즈하자.

쉽다.. 다음을 따라하자.
필요한 프로그램 설치

	sudo apt-get install imagemagick

사용 예시이다. 
위는 source파일을 50퍼센트로 작게 리사이즈해서 dest에 저장.
아래는 source파일을 1024*768 사이즈의 이미지로 리사이즈해서 dest.jpg에 저장
개인적으로는 %시 사이즈 끝자리가 제어되지 않아서 아래의 방법을 선호한다.
	
	convert  -resize 50% source.png dest.jpg
	convert -resize 1024X768  source.png dest.jpg
