# CSS 정리
<br><br>
## 💡 CSS란?
<br>
> **CSS (Cascading Style Sheets)**  
> 웹페이지의 **디자인과 레이아웃**을 담당하는 언어로,  
> HTML 요소의 **색상, 글꼴, 배치, 크기, 애니메이션 등**을 제어한다.
<br><br>

---

## 📚 CSS의 기본 문법

```css
선택자 {
  속성: 값;
  속성: 값;
}
```

**예시:**
```css
h1 {
  color: blue;
  font-size: 24px;
  text-align: center;
}
```

<br><br>

| 구분 | 설명 |
|------|------|
| 선택자(Selector) | 어떤 HTML 요소에 스타일을 적용할지 지정 |
| 속성(Property) | 변경하고자 하는 스타일의 종류 |
| 값(Value) | 속성에 적용할 구체적인 값 |

---

## 🎯 CSS 적용 방법 3가지

### 1️⃣ 인라인 스타일
HTML 태그 내부에 직접 작성  
```html
<p style="color:red;">인라인 스타일</p>
```

### 2️⃣ 내부 스타일시트 (Internal)
`<head>` 안에 `<style>` 태그로 작성  
```html
<style>
  p { color: blue; }
</style>
```

### 3️⃣ 외부 스타일시트 (External)
별도 `.css` 파일로 관리 (가장 일반적인 방식)  
```html
<link rel="stylesheet" href="style.css" />
```

---

## 🧱 선택자(Selector) 종류

| 종류 | 예시 | 설명 |
|------|------|------|
| 전체 선택자 | `*` | 모든 요소 선택 |
| 태그 선택자 | `p`, `h1`, `div` | 특정 태그 선택 |
| 클래스 선택자 | `.box` | class 속성이 box인 요소 선택 |
| 아이디 선택자 | `#main` | id 속성이 main인 요소 선택 |
| 그룹 선택자 | `h1, h2, p` | 여러 선택자에 동일 스타일 적용 |
| 자식 선택자 | `div > p` | div의 직계 자식 p만 선택 |
| 자손 선택자 | `div p` | div 내부 모든 p 선택 |
| 형제 선택자 | `h1 + p`, `h1 ~ p` | h1 뒤에 오는 p 선택 |

---

## 🎨 텍스트 관련 속성

```css
p {
  color: #333;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  line-height: 1.6;
  letter-spacing: 1px;
  text-decoration: underline;
}
```

| 속성 | 설명 |
|------|------|
| `color` | 글자 색상 |
| `font-size` | 글자 크기 |
| `font-weight` | 글자 굵기 |
| `text-align` | 정렬 (left, center, right) |
| `line-height` | 줄 간격 |
| `letter-spacing` | 자간 |
| `text-decoration` | 밑줄, 취소선 등 |

---

## 📦 박스 모델(Box Model)

> 모든 HTML 요소는 하나의 “박스”로 구성된다.

```
┌───────────────┐
│   margin      │  (바깥 여백)
│ ┌───────────┐ │
│ │  border   │ │  (테두리)
│ │ ┌───────┐ │ │
│ │ │padding│ │ │  (안쪽 여백)
│ │ │content│ │ │  (내용)
│ │ └───────┘ │ │
│ └───────────┘ │
└───────────────┘
```

```css
div {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
}
```

| 속성 | 설명 |
|------|------|
| `margin` | 요소의 바깥 여백 |
| `padding` | 요소의 안쪽 여백 |
| `border` | 테두리 |
| `width`, `height` | 크기 지정 |

---

## 🎯 display 속성

| 값 | 설명 |
|----|------|
| `block` | 한 줄 전체 차지 (div, p, h1 등) |
| `inline` | 한 줄 안에 배치 (span, a 등) |
| `inline-block` | inline처럼 배치 + 크기 조정 가능 |
| `none` | 화면에서 숨김 (공간도 사라짐) |
| `flex` | 유연한 레이아웃 설정 (정렬, 비율 조정 가능) |
| `grid` | 격자 기반의 정밀한 레이아웃 |

---

## 🧭 position 속성

| 값 | 설명 |
|----|------|
| `static` | 기본 위치 (기본값) |
| `relative` | 자기 자신 기준으로 이동 |
| `absolute` | 부모 기준으로 이동 |
| `fixed` | 화면 고정 |
| `sticky` | 스크롤 중 일정 위치에 고정 |

```css
.box {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

---

## 🌈 색상 표현 방법

| 방법 | 예시 | 설명 |
|------|------|------|
| 색상명 | `red`, `blue` | 단순 이름 지정 |
| HEX 코드 | `#ff0000` | 16진수 색상 코드 |
| RGB | `rgb(255, 0, 0)` | 빨강, 초록, 파랑 값으로 지정 |
| RGBA | `rgba(255, 0, 0, 0.5)` | 투명도 포함 |
| HSL | `hsl(0, 100%, 50%)` | 색상, 채도, 명도로 지정 |

---

## ✨ border, background, shadow

```css
.box {
  border: 2px solid #333;
  border-radius: 8px;
  background-color: #f0f0f0;
  background-image: url("bg.png");
  box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.2);
}
```

---

## 🧩 Flexbox 핵심 속성

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
```

| 속성 | 설명 |
|------|------|
| `display: flex` | 플렉스 컨테이너 지정 |
| `justify-content` | 가로 방향 정렬 |
| `align-items` | 세로 방향 정렬 |
| `gap` | 자식 간 간격 |

---

## 🎬 트랜지션 & 애니메이션

```css
.box {
  transition: all 0.3s ease;
}
.box:hover {
  transform: scale(1.1);
  background-color: coral;
}
```

- `transition` : 변화가 부드럽게 일어나도록 함  
- `transform` : 회전, 크기 조절, 이동 등

---

## 🧠 반응형 디자인 (Responsive)

> 화면 크기에 따라 자동으로 스타일이 바뀌도록 설정

```css
@media (max-width: 768px) {
  body {
    background-color: lightgray;
  }
}
```

📱 모바일, 태블릿, PC 각각에 맞는 스타일 적용 가능

---

## ✅ CSS 정리 요약

- HTML이 뼈대라면, CSS는 **디자인을 입히는 옷**
- 스타일 적용 방법: **인라인 / 내부 / 외부**
- 핵심 개념: **선택자, 박스 모델, display, position**
- **Flex / Grid**로 레이아웃 구성
- 반응형을 위해 **@media** 적극 활용
- 💬 “CSS는 조화의 언어다 — 구조를 꾸미고, 의미를 살린다.”

