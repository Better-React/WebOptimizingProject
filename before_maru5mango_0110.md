# 📑 성능 분석 Before Project

📌 `홈페이지 주소`          
http://52.79.215.72:3000                
💻 `github 주소`                        
https://github.com/maru5mango/BeforeProject_Shopingmall

<br />



### 성능 개선 페이지 목록
- /movie
- /movie/:id


<br />


#### `/movie'
![image](https://user-images.githubusercontent.com/63353110/148930080-1048f88a-0654-4326-8b97-94c3ffc1562c.png)
![image](https://user-images.githubusercontent.com/63353110/148948763-b10a797d-a4a7-4c35-b256-adecf36001a2.png)
![image](https://user-images.githubusercontent.com/63353110/148952396-0d59d889-f031-470e-85eb-901b4e33bbbe.png)
![image](https://user-images.githubusercontent.com/63353110/148955601-76e98542-18c8-4c70-99b7-331ad813f60e.png)
![image](https://user-images.githubusercontent.com/63353110/148955678-fb4d8e2e-3a77-4260-a565-ddec46a731c6.png)



#### `/movie/:id`
![image](https://user-images.githubusercontent.com/63353110/148951197-ce250743-a2f3-4d69-a9bf-ff02ba7a4408.png)
![image](https://user-images.githubusercontent.com/63353110/148953292-78d1605c-fb74-4818-bd17-35192cc934a1.png)
![image](https://user-images.githubusercontent.com/63353110/148954685-5ef0827e-6612-464c-acf1-13acaec0d924.png)
![image](https://user-images.githubusercontent.com/63353110/148955899-0f7948bf-bc76-46cb-9789-2c00951a90bd.png)




## 1. 성능 분석표
#### 1) WebPageTest 결과
>  3G등 네트워크 조절도 해보았지만 웹 페이지 테스트에서는 Cache, Security를 제외하고는 딱히 나쁜 평가를 받지 않았습니다. 아마 첫 렌더링 기준으로 페이지를 평가하기 때문인 것 같습니다.
- ![image](https://user-images.githubusercontent.com/63353110/148783519-ecd980c6-61a5-46cc-a6d6-6c2002f627b6.png)

##### 2) PageSpeed 결과
> div 크기에 맞는 이미지 선정, bundle size 줄이기가 공통 과제로 나왔고, 특히 모바일 최적화가 안되어 있는 모습이 보입니다.


##### 1. `/movie`
- web           
![image](https://user-images.githubusercontent.com/63353110/148783358-7c73a6b2-4670-41f5-bb18-e60c090c6f3b.png)

- mobile          
![image](https://user-images.githubusercontent.com/63353110/148784356-07843bd2-9a25-46aa-908b-cc6be8ca5b16.png)

##### 2. `/movie/:id`
- web      
![image](https://user-images.githubusercontent.com/63353110/148784774-34d8f887-44aa-4f7c-b6ec-fe8dafc1eb6c.png)

- mobile            
![image](https://user-images.githubusercontent.com/63353110/148784712-afdc7f7b-943e-4849-8165-5a15db152fc5.png)




<br />

### 성능 분석 요약
###### `성능`
- load되는 경우 FPS가 60이 안되는 문제가 있다.
- javascript가 덩어리로 있다.
- jpg가 최적화 되어있지 않고, 크기가 전반적으로 큰 편이다.
- 새로 고침 시 계속 네트워크를 불러오게 된다.
- toggle시 계속 네트워크에서 데이터를 불러온다.
- api 중복 호출
- unique key 가 없는 component들 존재



###### `UX`
- 사진이 늘어난 부분이 있다.
- 로그인 보안 문제 -> UserId키를 localStorage에 저장.
- Reply답장시 UI가 겹쳐 나오는 것처럼 보인다.
- mobile 대응 안됨.
- Comments 부분이 늦게 달림, 사용자 이미지 로딩이 느림.



###### `/movie 페이지(1페이지까지 로드)`
- 32 requests
- 11.6MB resources


###### `/movieDetail 페이지`
- 22 requests
- 10.1MB resources



## 2. 개선 계획(최소 2개 이상 작성)
##### 1) API 호출 캐싱
  - 개선 계획
  - [ ] api 중복 호출
  - [ ] 웹 캐싱
  - [ ] LocalStorage, SessionStorage 이용

##### 2) 이미지 로드 최적화
  - 개선 계획
  - [ ] 이미지 크기 조절
  - [ ] firstPage 사진 priority주기
  - [ ] LocalStorage, SessionStorage 이용

##### 3) React Component 최적화
  - 개선 계획
  - [ ] map 사용시 적절한 key 값 제공
  - [ ] handleScroll 함수 최적화
  - [ ] bundle 파일 분리
