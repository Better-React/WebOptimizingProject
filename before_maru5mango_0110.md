# ๐ ์ฑ๋ฅ ๋ถ์ Before Project

๐ `ํํ์ด์ง ์ฃผ์`          
http://52.79.215.72:3000                
๐ป `github ์ฃผ์`                        
https://github.com/maru5mango/BeforeProject_Shopingmall

<br />



### ์ฑ๋ฅ ๊ฐ์  ํ์ด์ง ๋ชฉ๋ก
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




## 1. ์ฑ๋ฅ ๋ถ์ํ
#### 1) WebPageTest ๊ฒฐ๊ณผ
>  3G๋ฑ ๋คํธ์ํฌ ์กฐ์ ๋ ํด๋ณด์์ง๋ง ์น ํ์ด์ง ํ์คํธ์์๋ Cache, Security๋ฅผ ์ ์ธํ๊ณ ๋ ๋ฑํ ๋์ ํ๊ฐ๋ฅผ ๋ฐ์ง ์์์ต๋๋ค. ์๋ง ์ฒซ ๋ ๋๋ง ๊ธฐ์ค์ผ๋ก ํ์ด์ง๋ฅผ ํ๊ฐํ๊ธฐ ๋๋ฌธ์ธ ๊ฒ ๊ฐ์ต๋๋ค.
- ![image](https://user-images.githubusercontent.com/63353110/148783519-ecd980c6-61a5-46cc-a6d6-6c2002f627b6.png)

##### 2) PageSpeed ๊ฒฐ๊ณผ
> div ํฌ๊ธฐ์ ๋ง๋ ์ด๋ฏธ์ง ์ ์ , bundle size ์ค์ด๊ธฐ๊ฐ ๊ณตํต ๊ณผ์ ๋ก ๋์๊ณ , ํนํ ๋ชจ๋ฐ์ผ ์ต์ ํ๊ฐ ์๋์ด ์๋ ๋ชจ์ต์ด ๋ณด์๋๋ค.


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

### ์ฑ๋ฅ ๋ถ์ ์์ฝ
###### `์ฑ๋ฅ`
- load๋๋ ๊ฒฝ์ฐ FPS๊ฐ 60์ด ์๋๋ ๋ฌธ์ ๊ฐ ์๋ค.
- javascript๊ฐ ๋ฉ์ด๋ฆฌ๋ก ์๋ค.
- jpg๊ฐ ์ต์ ํ ๋์ด์์ง ์๊ณ , ํฌ๊ธฐ๊ฐ ์ ๋ฐ์ ์ผ๋ก ํฐ ํธ์ด๋ค.
- ์๋ก ๊ณ ์นจ ์ ๊ณ์ ๋คํธ์ํฌ๋ฅผ ๋ถ๋ฌ์ค๊ฒ ๋๋ค.
- toggle์ ๊ณ์ ๋คํธ์ํฌ์์ ๋ฐ์ดํฐ๋ฅผ ๋ถ๋ฌ์จ๋ค.
- api ์ค๋ณต ํธ์ถ
- unique key ๊ฐ ์๋ component๋ค ์กด์ฌ



###### `UX`
- ์ฌ์ง์ด ๋์ด๋ ๋ถ๋ถ์ด ์๋ค.
- ๋ก๊ทธ์ธ ๋ณด์ ๋ฌธ์  -> UserIdํค๋ฅผ localStorage์ ์ ์ฅ.
- Reply๋ต์ฅ์ UI๊ฐ ๊ฒน์ณ ๋์ค๋ ๊ฒ์ฒ๋ผ ๋ณด์ธ๋ค.
- mobile ๋์ ์๋จ.
- Comments ๋ถ๋ถ์ด ๋ฆ๊ฒ ๋ฌ๋ฆผ, ์ฌ์ฉ์ ์ด๋ฏธ์ง ๋ก๋ฉ์ด ๋๋ฆผ.



###### `/movie ํ์ด์ง(1ํ์ด์ง๊น์ง ๋ก๋)`
- 32 requests
- 11.6MB resources


###### `/movieDetail ํ์ด์ง`
- 22 requests
- 10.1MB resources



## 2. ๊ฐ์  ๊ณํ(์ต์ 2๊ฐ ์ด์ ์์ฑ)
##### 1) API ํธ์ถ ์บ์ฑ
  - ๊ฐ์  ๊ณํ
  - [ ] api ์ค๋ณต ํธ์ถ
  - [ ] ์น ์บ์ฑ
  - [ ] LocalStorage, SessionStorage ์ด์ฉ

##### 2) ์ด๋ฏธ์ง ๋ก๋ ์ต์ ํ
  - ๊ฐ์  ๊ณํ
  - [ ] ์ด๋ฏธ์ง ํฌ๊ธฐ ์กฐ์ 
  - [ ] firstPage ์ฌ์ง priority์ฃผ๊ธฐ
  - [ ] LocalStorage, SessionStorage ์ด์ฉ

##### 3) React Component ์ต์ ํ
  - ๊ฐ์  ๊ณํ
  - [ ] map ์ฌ์ฉ์ ์ ์ ํ key ๊ฐ ์ ๊ณต
  - [ ] handleScroll ํจ์ ์ต์ ํ
  - [ ] bundle ํ์ผ ๋ถ๋ฆฌ
