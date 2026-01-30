# Game Developer Portfolio

A clean, interactive portfolio website for game developers.

## 🚀 Quick Start

### GitHub Pages 호스팅 방법

1. **GitHub 저장소 생성**
   ```bash
   # 새 저장소를 만들고 (예: portfolio)
   # 이 파일들을 업로드
   ```

2. **파일 구조**
   ```
   portfolio/
   ├── index.html
   ├── data.json
   └── README.md
   ```

3. **GitHub Pages 설정**
   - 저장소 Settings → Pages
   - Source: Deploy from a branch
   - Branch: main → / (root) → Save
   - 5분 후 `https://yourusername.github.io/portfolio` 에서 확인 가능!

### 프로젝트 수정 방법

**모든 내용은 `data.json` 파일만 수정하면 됩니다!**

#### 개인 정보 수정
```json
"personal": {
  "name": "당신의 이름",
  "title": "Game Developer & Creative Coder",
  "tagline": "당신의 한줄 소개",
  "email": "your.email@example.com"
}
```

#### 스킬 추가/수정
```json
"skills": [
  {
    "icon": "🎮",
    "name": "Unity",
    "description": "설명",
    "progress": 90  // 0-100 숫자
  }
]
```

#### 프로젝트 추가
```json
"projects": [
  {
    "number": "04",
    "type": "PROJECT 04",
    "title": "새 프로젝트 제목",
    "description": "프로젝트 설명",
    "tags": ["Unity", "C#"],
    "link": "https://github.com/yourproject"  // 클릭 시 이동할 링크
  }
]
```

#### 소셜 링크 수정
```json
"social": [
  {
    "name": "GitHub",
    "label": "G",
    "url": "https://github.com/yourusername"
  }
]
```

## 📝 로컬에서 테스트

1. **Python 서버 (가장 쉬움)**
   ```bash
   # 파일이 있는 폴더에서
   python -m http.server 8000
   # 브라우저에서 http://localhost:8000 접속
   ```

2. **VS Code Live Server**
   - VS Code 확장 프로그램 "Live Server" 설치
   - index.html 우클릭 → "Open with Live Server"

## ✨ 기능

- ✅ 커스텀 인터랙티브 커서
- ✅ 스크롤 프로그레스 바
- ✅ 3D 프로젝트 카드 틸트 효과
- ✅ 스킬 프로그레스 바 애니메이션
- ✅ 부드러운 스크롤 애니메이션
- ✅ 반응형 디자인 (모바일 지원)
- ✅ JSON 기반 컨텐츠 관리

## 🛠 커스터마이징

### 색상 변경
`index.html`의 `:root` 섹션에서 색상 변경:
```css
:root {
    --blue: #0066ff;  /* 원하는 색상으로 변경 */
}
```

### 폰트 변경
`<link>` 태그에서 Google Fonts 변경

## 📱 반응형
자동으로 모바일, 태블릿, 데스크탑에 최적화됩니다.

## 🐛 문제 해결

**Q: 프로젝트가 표시되지 않아요**
A: 브라우저 개발자 도구 (F12) → Console 탭에서 에러 확인. data.json 파일 경로가 맞는지 확인하세요.

**Q: 로컬에서 작동하지 않아요**
A: CORS 에러일 수 있습니다. 반드시 로컬 서버를 사용해야 합니다. (Python 서버 또는 Live Server)

**Q: GitHub Pages에서 안 보여요**
A: Settings → Pages에서 제대로 설정되었는지 확인. 5-10분 정도 기다려야 할 수 있습니다.

## 📄 라이선스
자유롭게 사용하세요!
