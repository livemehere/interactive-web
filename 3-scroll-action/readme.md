# 새로 알게된 지식 & 스킬

## Mark up

- nav 바에서는 흔히 a 태그를 사용한다.(어차피 리액트에서도 Link태그는 a태그로 변형된다)
- Lorem + 숫자적으면 그만큼 나온다.

## Javascript

```javascript
        window.addEventListener('scroll',(e)=>{
            let y = window.scrollY;
            stars.style.top = (y * 0.2 )+ 'px';
            stars.style.left = (y * 0.2 )+ 'px';
            mountains_behind.style.top = (y * 0.2 )+ 'px';
            header.style.top = (y * 0.6 )+ 'px';
            moon.style.top = (y * 0.6 )+ 'px';
            text.style.right = (y*2 -500)+ 'px';
        })
        btn.addEventListener('click',()=>{
            console.log('click')
            post.scrollIntoView({behavior: "smooth"})
        })
```

- 스크롤에 따라서 애니메이션을 넣을거면, window.scrollY 값과 합쳐서 가중치를 적절히 설정하고 새롭게 선언하는 방식을 사용할 수 있다.
- 그리고 최초의 값이 0이 아니라면 코드의 마지막 text부분처럼 최초의 값을 더하고나 뺴주고 시작하자, (최초의 값을 가져왔었는데 콜백함수에서 사용하려니 아마 클로저 문제로 제대로 참조못하는거같다)
- scrollIntoView()를 쓰면 스크롤을 직접 조작하지않아도 element로 이동한다.

## scss

```scss
body{
  min-height: 100vh;
  margin: 0;
}
```

- 항상 height값을 설정한다는건 다른 디자인이 유동적으로 움직이는 걸막고 꺠버렸는데, 그 값을 주지않으면 정렬할 수 없는 경우가 많았는데 그냥 `height:100vh` 말고 `min-height:100vh` 는 정말 개꿀이다
- 폰트사이즈가 들어가는 element의 패딩,마진 값들은 em으로 해주면 자동으로 보정이 다된다 꼭 쓰자.

> ⭐️ position: absolute; 여도 flex 정렬이 다먹힌다.. 머지? 안되는줄 았는데..

```scss
 #moon{
    mix-blend-mode: screen;
  }
```

- css에서도 포토샵처럼 사진의 레이어모드? 를 설정해줘서 이것저것 겹치는 부분을 처리해줄수있다. 특히 빛 같은 사진들에 사용하면 좋다.

```scss
  img{
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
```

- 이미지를 배경으로사용할떄는 위의 4개를 사용하면 아주깔끔하다
- object-fit이 background-size :cover; 과 동일하다. 몰라서이때까지 백그라운드가 최곤줄알았는데..

```scss
background: linear-gradient(to top, $bg-color-dark,transparent);
```

- 그래디언트는 아주 유용하고, 좋은거같다. 단색의 디자인보다 훨신 모던한 느낌을 주고 생각보다 그렇게 어렵지않다
- 위와같이 transparent를 섞어주면, 아주자연스러운 연결이 가능하다.