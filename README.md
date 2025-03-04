# Joowon Wordle

Wordle은 하루에 한 번 새로운 단어 퍼즐을 풀 수 있는 단어 추측 게임입니다. 이 프로젝트는 [뉴욕 타임스 Wordle](https://www.nytimes.com/games/wordle/index.html)을 참고하여 몇 가지 규칙을 수정한 버전으로, HTML, CSS, JavaScript를 사용해 제작되었습니다. Netlify를 통해 배포되었으며, 아래 링크에서 확인할 수 있습니다.

**[게임 바로가기](https://joowon-wordle.netlify.app/)**

## 게임 규칙

1. **5글자 단어**: 존재하는 단어가 아니어도 가능합니다.
2. **6번의 시도**: 최대 6번 안에 단어를 맞춰야 합니다.
3. **색상 표시**:
   - 기존에 썼던 글자가 단어에 존재하면 **노란색**.
   - 글자의 위치까지 맞으면 **초록색**.
4. **게임 종료**: 상단에 게임 소요 시간이 표시됩니다.

## 기술 스택

- **HTML/CSS**: 기본 구조와 스타일링.
- **JavaScript**: 동적인 요소 구현 (입력 처리, 색상 피드백, 타이머 등).
- **Netlify**: 배포 플랫폼.

## 이번 Wordle 게임을 통해 배운 것

### DOM 조작
- `document.createElement("div")`: 새로운 `<div>` 요소를 생성합니다.
- `div.innerText = "게임이 종료됐습니다."`: `<div>` 요소의 텍스트 내용을 설정합니다.
- `div.style = ...`: `<div>` 요소의 스타일을 설정합니다.
- `document.body.appendChild(div)`: `<div>` 요소를 `<body>`에 추가합니다.

### 이벤트 처리
- `window.addEventListener("keydown", handleKeydown)`: 키보드 입력을 감지해 `handleKeydown` 함수를 호출합니다.
- `window.removeEventListener("keydown", handleKeydown)`: 이벤트 리스너를 제거합니다.

### 타이머
- `new Date()`: 현재 날짜와 시간을 가져옵니다.
- `setInterval(setTime, 1000)`: 1초 간격으로 `setTime` 함수를 실행합니다.

## Netlify로 배포하기

프로젝트는 Netlify를 통해 배포되었습니다.  
**배포 URL**: [https://joowon-wordle.netlify.app/](https://joowon-wordle.netlify.app/)

### Netlify 배포 방법
1. Netlify 웹사이트에 접속하여 계정을 생성합니다.
2. 배포할 정적 웹사이트 파일을 준비합니다.
3. GitHub 계정을 생성하거나 기존 계정을 사용합니다.
4. GitHub에 새로운 Repository를 생성하고 코드를 업로드합니다.
5. Netlify에서 GitHub과 연결하고, 배포할 Repository와 Branch를 선택합니다.
6. Build Command와 Publish Directory를 설정합니다.
7. "Deploy site" 버튼을 클릭하여 배포를 시작합니다.
8. 배포가 완료되면 제공된 URL로 접속하여 확인합니다.
