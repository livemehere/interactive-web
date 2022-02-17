# full page scroll trick

## 환경

```bash
npm i sass -g 
```

## 세로 ⭐️

```css
.container{

  scroll-snap-type: y mandatory;
  width: 100%;
  height: 100%;
  overflow-y: scroll;
  scroll-behavior: smooth;
}


section{
  
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  scroll-snap-align: start;
}
```

## 가로

```css
.container{
  display: flex; ➕➕➕➕➕➕
  scroll-snap-type: x mandatory; 🔨🔨🔨🔨
  width: 100%;
  height: 100%;
  overflow-y: scroll;
  scroll-behavior: smooth;
}


section{
  flex:none; ➕➕➕➕➕➕
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  scroll-snap-align: start;
}

```

