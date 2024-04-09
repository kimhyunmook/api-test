# Lostark One Depth 캐릭터 간단 검색

## 사이트 설명

로아와 같은 통계 사이트와 달리 depth를 줄여 보다 간편히 캐릭터 검색을 할 수 있는 기능.
파티를 구할 때 좀 더 편하고 쉽게 체크 할 수 있는 사이트 제작.
스팩 검사 기준은 제작자의 주관적인 기준 (베히모스 전까지 클리어함) 검사 기준은 클리어 할 정도의 스팩.
유저들이 많이 보는 부분들을 점수화 시켜 클릭 한번으로 보여줌.
팔찌 특옵은 계산에 포함 안됨.
세트 레벨은 현재 계산에 포함 안됨.
카드 추가피해 계산에 포함 안됨. (Lostark Api에서 지원 안함)

## 제작 이유

Lostark 는 여러 스팩업 요소가 존재하며 해당 스팩들을 전부 검사하는데 꽤 시간이 걸리며 놓치는 부분도 존재합니다. 로아와, 클로아 등 유저의 스팩등을 한눈에 보도록 검사하는 사이트는 존재하지만 해당 사이트에서도 그 유저의 스팩을 보고 실제 파티원을 구하는 유저가 판다해야된다는 점이 있습니다. 다른 점이라고 하면 유저 검색과 동시에 클릭 한번만으로 원하는 레이드의 그 유저가 적합한지 판단하여 점수화 시켜 보여 주어 좀 더 빠르게 파티원을 모집할 수 있지 않을까하는 생각에 제작하게 되었습니다. 

## 미흡한 점

UI 및 편의 기능 개선 필요

## 제작 tool

Lostark 공식 api, vanilla Javascript, [module] axios, tailwind

## 참고 및 출처

Lostark 공식 홈페이지 및 개발자의 Brain

### User 검사 schema

userSpec = {
name: "",
level: 0,
itemlevel: 0,
legendAvatar: 0,
status: {
sum: 0,
value: [],
},
skillpoint: 0,
title: "",
elixir: {
lv: 0,
special: true,
},
wepon: {
stage: 0,
itemlevel: 0,
quality: 0,
transcendence: 0,
},
armor: {
stage: 0, //평균치
itemlevel: 0, //평균치
quality: 0, //평균치
transcendence: 0,
},
gem: {
attk: 0, //평균치
cool: 0, //평균치
},
card: [],
};
