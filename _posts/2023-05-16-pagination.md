---
layout: single
title: pagination
---


## Pagination 이란?

1.쿼리에 해당되는 데이터를 한번에 불러오지 않고 나눠서 조금씩 가져온다.
2. 쿠팡 같은 경우 수억개의 상품이 데이터베이스에 저장되어있는데 사용자가 화면을 들어갈때마다 모든 상품정보를 서버에서 클라이언트에 전송할 필요가 없다.


## Page based Pagination

1. 페이지 기준으로 데이터를 잘라서 요청 
2. 요청을 보낼때 원하는 데이터 갯수와 몇번째 페이지를 가져올지 명시
3. 페이지 숫자를 누르면 다음 페이지로 넘어가는 형태로 많이 사용
4. Pagination 도중 데이터베이스에 데이터가 추가되거나 삭제될경우 저장되는 데이터가 누락 되거나 중복될 수 있음
5. 매우 간단한 알고리즘

##  Cusor Based Pagination

1. 가장 최근에 가져온 데이터를 기준으로 요청
2. 요청을 보낼때 마지막 데이터의 기준값과 몇개의 데이터를 가져올지 명시
3. 스크롤 형태의 리스트에서 많이 사용
4. 최근 데이터의 기준값을 기반으로 쿼리가 작성되기 때문에 데이터가 누락되거나 중복될 확률이 적음