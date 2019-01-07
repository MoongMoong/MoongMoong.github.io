---
title: 우분투 PNG파일 ico파일로 변환 (Ubuntu18.04 Ubuntu16.04 PNG image convert to ico file)
layout: post
date: '2019-01-07 09:33:36'
excerpt: PNG파일을 ico 파일로 바꾸자
tag:
- markdown
- image
- github
categories:
- ubuntu
---

## 이미지의 형식을 바꿔보자.

쉽다.. 다음을 따라하자.\
필요한 프로그램 설치\

	apt-get install icoutils


사용 예시이다. \
	
	icotool -c -o output.ico input.png

