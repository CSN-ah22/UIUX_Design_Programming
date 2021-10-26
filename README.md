# UI-UX_Programming

### 10-15
<img src="https://user-images.githubusercontent.com/70833455/138897202-6acc8c8e-1774-4422-9542-881d348774ca.png">

### 문자 앞에 도형 넣는 기능 ::before

[참고 링크 W3 School](https://www.w3schools.com/cssref/sel_before.asp)

### 위에 기능의 도형을 문자 뒤로 보내고 싶을때(레이아웃을 밑으로 내리는것처럼)

- **mix-blend-mode Property**

[참고 링크 W3 School](https://www.w3schools.com/cssref/pr_mix-blend-mode.asp)

### 결과물

![image](https://user-images.githubusercontent.com/70833455/135623711-5d9c4b80-9456-453f-a5f5-0495560d5b04.png)

```jsx
.sub-txt-grp dt{margin:15px 0 10px;position: relative;} //Title1이란 글자를 가리킴, relative 꼭 필요
.sub-txt-grp dt::before{content:"";display: inline-block;width: 80px;height:20px;background-color: yellow;position: absolute;top: 20px; mix-blend-mode: multiply;}
//형광펜을 가리킴, content가 빈값이라도 꼭 필요함
//inline-block도 필요함, width는 굵기가 아니라 가로길이! height가 굵기!
//position을 absolute로 지정해서 relative를 부여한 곳을 기준으로 top값에따라 위치가 달라짐
```

### 말줄임표 나타내기

**1번 방법**

```jsx
.related-cont h5 a{display: block;/*말줄임시 block필수*/
overflow: hidden;
text-overflow: ellipsis; 
white-space: nowrap;
color: #222;
text-decoration: none;}
```

**2번 방법**

```jsx
.related-cont h5 a{display: inline-block;/*inline-block사용시 width 100% 필수*/
width: 100%;
overflow: hidden;
text-overflow: ellipsis; 
white-space: nowrap;
color: #222;
text-decoration: none;}
```

- **전부 공식**이나 마찬가지이니 외우기
- **노란줄도** 하나로 **정해서 외워야** 한다

### 사진이 찌그러지거나 늘어나지 않게, 중앙에 배치하는 코드

- `center/cover`

```css
.sub-visual, .sub-img, .thumb-img 
{background: url(/*이미지 경로*/) no-repeat center/cover;}
```
