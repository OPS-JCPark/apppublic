# apppublic

여러 앱의 공개 웹 페이지(앱 소개 · 개인정보처리방침)를 모아 두는 저장소입니다. GitHub Pages로 게시됩니다.
주소: https://ops-jcpark.github.io/apppublic/

## 구조

```
index.html                 앱 목록 (허브)
myfridge/                  냉장고콕 (com.tory.myfridge)
  index.html               앱 소개
  icon.png                 앱 아이콘 (512px)
  privacy/index.html       개인정보처리방침 ← Play Console에 등록하는 URL
privacy/index.html         예전 주소. myfridge/privacy/로 자동 이동 (지우지 말 것)
```

- 앱 폴더 이름은 **패키지명 끝부분**으로 정합니다. 앱 이름이 바뀌어도 주소가 바뀌지 않게 하기 위해서입니다.
- 냉장고콕 개인정보처리방침 URL: https://ops-jcpark.github.io/apppublic/myfridge/privacy/

## 냉장고콕 개인정보처리방침 고치기

원본은 앱 저장소의 `fridge-app/src/data/privacyPolicy.json`입니다.
JSON을 고친 뒤 `node fridge-app/tools/build-privacy-html.js`를 실행하면 앱 화면과 이 폴더의 `myfridge/privacy/index.html`이 함께 맞춰집니다. HTML을 직접 고치지 마세요.

## 새 앱 추가하기

1. 패키지명 끝부분으로 폴더를 만듭니다. 예: `com.tory.mynote` → `mynote/`
2. `mynote/index.html`(소개), `mynote/icon.png`, `mynote/privacy/index.html`(개인정보처리방침)을 넣습니다.
3. 최상위 `index.html`의 앱 목록에 블록을 하나 추가합니다.
4. Play Console의 개인정보처리방침 URL: `https://ops-jcpark.github.io/apppublic/mynote/privacy/`
