#  HTML 정리 노트

---

## 📘 HTML이란?
> **HTML (HyperText Markup Language)**  
> 웹페이지의 **구조와 내용을 정의**하는 언어로, 브라우저가 이를 해석해 사용자에게 시각적으로 보여준다.

<br>

- HTML = 웹의 **뼈대(Structure)**  
- CSS = **디자인(Style)**  
- JavaScript = **동작(Behavior)**

<br>

**💡 TIP:**  
크롬에서 `F12` → **개발자 도구(DevTools)** 를 열면 웹 구조를 실시간으로 확인하고 수정할 수 있다.

<br>

---

<br>

## HTML 문서의 기본 구조
<br>

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>HTML 예시</title>
  </head>
  <body>
    <h1>안녕하세요!</h1>
    <p>이곳은 본문 내용이 들어가는 영역입니다.</p>
  </body>
</html>
```

<br><br>

| 태그 | 설명 |
|------|------|
| `<!DOCTYPE html>` | 문서가 HTML5 문법을 사용함을 선언 |
| `<html>` | 문서의 최상위(root) 요소 |
| `<head>` | 메타데이터(검색엔진/브라우저용 정보) |
| `<body>` | 실제 화면에 표시되는 콘텐츠 영역 |

---


<br><br>



## 🧩 기본 태그 종류

<br>

### 1️⃣ 텍스트 관련 태그
- 제목: `<h1> ~ <h6>`  
- 단락: `<p>`  
- 줄바꿈: `<br>`  
- 수평선: `<hr>`  
- 강조: `<strong>`, `<em>`

<br>

```html
<h1>큰 제목</h1>
<p>한 줄 문단입니다.</p>
<strong>중요</strong> <em>기울임</em>
```

---

### 2️⃣ 링크 & 이미지

```html
<a href="https://velog.io" target="_blank" rel="noopener">벨로그로 이동</a>
<img src="image.jpg" alt="대체 텍스트" width="400" />
```

- `alt`는 접근성과 SEO 때문에 항상 작성하자.

---

### 3️⃣ 목록

```html
<ul>
  <li>사과</li>
  <li>바나나</li>
</ul>

<ol>
  <li>HTML</li>
  <li>CSS</li>
</ol>
```

---

### 4️⃣ 표

```html
<table>
  <thead>
    <tr><th>이름</th><th>나이</th></tr>
  </thead>
  <tbody>
    <tr><td>혜린</td><td>20</td></tr>
  </tbody>
</table>
```

| 이름 | 나이 |
|------|------|
| 혜린 | 20   |

---

## ✨ 폼(Form) 관련 태그

```html
<form action="/submit" method="post">
  <label>이름: <input type="text" name="username" /></label><br>
  <label>비밀번호: <input type="password" name="password" /></label><br>
  <button type="submit">전송</button>
</form>
```

- 주요 속성: `action`, `method(get|post)`, `name`, `placeholder`, `maxlength`

---

## 🎬 멀티미디어

```html
<img src="cat.jpg" alt="고양이">
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
<audio controls>
  <source src="music.mp3" type="audio/mp3">
</audio>
```

---

## 🧠 시맨틱 태그 (Semantic Tags)

> 의미를 가진 태그로 문서 구조를 명확히 한다.

### 💎 장점
1. **의미 전달 명확** — 코드만 봐도 역할 파악 가능  
2. **SEO 향상** — 검색엔진이 구조를 잘 파악함  
3. **가독성/유지보수성 향상**

| 태그 | 역할 |
|------|------|
| `<header>` | 페이지 또는 섹션의 머리글 |
| `<nav>` | 네비게이션(메뉴) |
| `<main>` | 주요 콘텐츠 |
| `<article>` | 독립 콘텐츠(기사, 블로그 글 등) |
| `<aside>` | 보조 정보(사이드바 등) |
| `<footer>` | 바닥글(저작권, 연락처 등) |

**예시:**
```html
<body>
  <header><h1>사이트 제목</h1></header>
  <nav>...메뉴...</nav>
  <main>
    <article>...글 내용...</article>
    <aside>...참고자료...</aside>
  </main>
  <footer>© 2025 혜린</footer>
</body>
```

---

## 🔧 그 외 유용한 태그/속성
- `<meta charset="UTF-8">` — 문자 인코딩(한글 깨짐 방지)  
- `<link rel="stylesheet" href="style.css">` — 외부 CSS 연결  
- `<script src="app.js"></script>` — 외부 JS 연결  
- 속성: `id` (고유), `class` (재사용/그룹), `data-*` (임의 데이터 저장)

---

## ✅ 정리 요약

- HTML = 콘텐츠의 **구조**  
- CSS = **스타일**  
- JS = **동작**  
- 시맨틱 태그는 **의미를 부여**해 이해도와 SEO를 높여준다.  
- 벨로그에 쓸 때는 **Markdown 헤딩(`#`, `##`)**과 **코드블록(````html``` )**을 적절히 사용하면 미리보기에서 깔끔하게 보인다.
