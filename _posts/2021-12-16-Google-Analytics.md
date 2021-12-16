---
layout: post
title: Google Analytics
tags: [GA]
comments: true
---

![Captured Image]({{"/assets/img/ga-capture"|relative_url}})


위 사진은 본 사이트에 구글 애널리틱스가 적용되어 실시간 개요를 확인하는 화면을 캡쳐한 것이다.

구글 애널리틱스를 사용하기 위해 우선 [구글 애널리틱스 홈페이지](https://analytics.google.com/analytics/web/provision/#/provision)에 진입했다.

페이지 중앙의 '측정 시작' 버튼을 통해 계정 설정에서는 chanwoow를 입력, 속성 설정에서는 사이트 속성을 입력했다.

그리고 비즈니스 정보에서 업종 카테고리는 '컴퓨터 및 전자제품'을 설정했고, 비즈니스 규모는 '작음 - 직원 1-10명'을 선택했다.

비즈니스에서 Google 애널리틱스를 어떻게 활용할지에 대한 부분은 '내 사이트 또는 앱에 대한 고객 참여도 측정', '내 사이트 또는 앱 환경 최적화', '여러 기기 또는 플랫폼에서 데이터 측정', '콘텐츠 수익성 측정'을 선택했다.

관리자 화면의 데이터 스트림 부분에 [본 사이트의 url](https://chanwoow.github.io/)을 입력하여 스트림을 만들었고 생성된 측정 ID를 `_config.yml`의 `google_analytics` 부분에 입력했고, 쿠키를 받아들일 수 있도록 `cookie-consent`에 true를 입력했다.

적용 결과 정상적으로 구글 애널리틱스에서 데이터가 집계되는 것을 확인할 수 있었다.