
# [데브디] 프론트엔드 개발자 
<a name="readme-top"></a>
> Debounce Function 사용법

Debounce 함수는 특정 함수가 너무 빈번하게 호출되는 것을 방지하기 위해 사용하는 기법입니다. 
즉 유저가 입력할 때마다 코드를 오직 한 번씩만 실행되도록 해주는 함수로,
검색 박스의 제안, 텍스트 필드의 자동 저장, 버튼의 더블 클릭의 제거 등이 debounce를 이용하는 사례입니다.

## 시작 가이드 
<a name="env"></a>

이 프로젝트를 실행하기 위한 환경은 다음과 같습니다. 

- 웹 브라우저: Chrome, Firefox, Safari 등
- JavaScript: ES6 호환 환경

## 설치 및 실행방법
<a name="getting-started"></a>

1. 리포지토리를 클론하세요.
```bash
git clone https://github.com/ome-r/dev_d/
```

2. debounce.html 파일을 웹 브라우저에서 열어주세요.


## 주요 기능

### Debounce

1. 함수의 정의
Debounce 함수는 특정 함수가 너무 빈번하게 호출되는 것을 방지하기 위해 사용하는 기법입니다. 예를 들어 사용자가 스크롤을 하는 동안에는 특정 함수를 호출하지 않고, 사용자가 스크롤을 멈춘 후에 특정 함수를 호출하는 등의 상황에서 활용됩니다.

2. 함수의 매개변수
Debounce 함수는 세 개의 매개변수를 받습니다.

- `func`: debounce 처리를 하고자 하는 함수입니다.
- `wait`: 함수 호출 사이에 대기할 시간을 밀리초 단위로 입력합니다. 기본값은 0입니다.
- `immediate`: 이 값이 true로 설정되면, debounce 함수는 대기 시간이 시작할 때 대상 함수를 호출합니다. 기본값은 false입니다.
- 또한 debounce 함수는 프로미스를 반환하며, 원래 함수의 실행이 완료될 때 프로미스가 해결됩니다.

3. 함수의 사용법
```javascript
const debouncedFunction = debounce(function() {
    // debounce 처리를 원하는 로직
}, 500);
```

위와 같이 debounce 함수를 사용하여 대상 함수를 감쌉니다. 이후에 `debouncedFunction`을 호출하면, 실제 함수는 500밀리초의 딜레이 이후에 호출됩니다.

4. 이벤트 핸들러에 적용하기
```javascript
document.getElementById('search').addEventListener('input', updateSearchResult);
```

위와 같이, debounce 함수를 이용해 만든 함수를 이벤트 핸들러에 바인딩할 수 있습니다. 이 경우, 사용자가 'search' 입력 필드에 입력을 할 때마다 `updateSearchResult` 함수가 호출되지만, 실제로는 500밀리초마다 한 번씩만 호출됩니다.

## 아키텍처
```
├── README.md
├── dev.d
│   ├── assets
│   │   ├── css
│   │   │   ├── debounce.css
│   │   └── img
│   │   │   ├──  devd.png
│   ├── pages
│   │    ├──  debounce.html
```
 
 
