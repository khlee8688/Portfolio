# 📸 이미지 추가 방법

포트폴리오에 프로젝트 이미지를 추가하는 방법입니다.

## 📁 폴더 구조

```
portfolio/
├── index.html
├── project-detail.html
├── data.json
├── images/              # 이미지 폴더 생성
│   ├── project1-thumb.jpg
│   ├── project1-1.jpg
│   ├── project1-2.jpg
│   ├── project2-thumb.jpg
│   └── ...
└── README.md
```

## 🖼️ 이미지 추가 단계

### 1. images 폴더 만들기
포트폴리오 루트 디렉토리에 `images` 폴더를 생성하세요.

### 2. 이미지 파일 추가
프로젝트 스크린샷을 `images` 폴더에 넣으세요.

**권장 이미지 규격:**
- **썸네일 (thumbnail)**: 800x450px (16:9 비율)
- **상세 이미지**: 1920x1080px 또는 1280x720px
- **파일 형식**: JPG, PNG
- **파일 크기**: 각 이미지 500KB 이하 권장

### 3. data.json 수정

```json
{
  "id": "your-project",
  "number": "01",
  "title": "Your Project",
  "thumbnail": "images/project1-thumb.jpg",  // 썸네일 추가
  "images": [                                 // 상세 이미지 추가
    "images/project1-1.jpg",
    "images/project1-2.jpg",
    "images/project1-3.jpg"
  ]
}
```

## 📝 예시

### 프로젝트 1 이미지 구조
```
images/
├── project1-thumb.jpg     # 메인 페이지 카드에 표시
├── project1-1.jpg         # 상세 페이지 갤러리
├── project1-2.jpg         # 상세 페이지 갤러리
└── project1-3.jpg         # 상세 페이지 갤러리
```

### data.json 예시
```json
{
  "id": "hybrid-puzzle-adventure",
  "number": "01",
  "type": "PROJECT 01",
  "title": "2D/3D Hybrid Puzzle Adventure",
  "thumbnail": "images/project1-thumb.jpg",
  "images": [
    "images/project1-1.jpg",
    "images/project1-2.jpg",
    "images/project1-3.jpg"
  ]
}
```

## ✨ 기능

### 메인 페이지
- 프로젝트 카드에 썸네일 이미지 표시
- 이미지가 없으면 기본 그라데이션 배경

### 상세 페이지
- "Screenshots" 섹션에 이미지 갤러리
- 이미지 클릭 시 라이트박스(전체 화면)로 확대
- ESC 키로 닫기

## 🚨 주의사항

1. **이미지 경로는 정확히!**
   - `images/project1-thumb.jpg` (올바름)
   - `Images/project1-thumb.jpg` (대소문자 구분!)
   - `/images/project1-thumb.jpg` (앞에 / 붙이지 마세요)

2. **파일명 규칙**
   - 공백 사용 금지 → `project 1.jpg` ❌
   - 하이픈이나 언더스코어 사용 → `project-1.jpg` ✅ 또는 `project_1.jpg` ✅

3. **이미지 최적화**
   - 대용량 이미지는 로딩 속도가 느림
   - [TinyPNG](https://tinypng.com/) 등으로 압축 추천

4. **저작권**
   - 본인이 만든 게임 스크린샷만 사용
   - 다른 게임 이미지 사용 금지

## 💡 팁

### 이미지가 아직 없다면?
```json
{
  "thumbnail": "",  // 비워두면 기본 그라데이션
  "images": []      // 빈 배열이면 "No screenshots available" 표시
}
```

### 스크린샷 찍는 법
- **Unity**: Game View에서 오른쪽 클릭 → "Save Screenshot"
- **Unreal**: 콘솔에서 `Shot` 또는 `HighResShot` 명령어
- **일반**: F12 (게임 내 스크린샷 단축키)

### 좋은 스크린샷 만들기
1. 게임의 핵심 메카닉을 보여주는 장면
2. 밝고 선명한 화면
3. UI가 잘 보이는 각도
4. 다양한 상황 (전투, 퍼즐, 탐험 등)

## 🔧 문제 해결

**Q: 이미지가 안 보여요**
A: 
1. 파일 경로 확인 (대소문자, 철자)
2. images 폴더가 index.html과 같은 위치에 있는지 확인
3. 브라우저 콘솔(F12)에서 에러 확인

**Q: 이미지가 찌그러져요**
A: CSS의 `object-fit: cover`가 자동으로 처리하지만, 16:9 비율 권장

**Q: 로딩이 너무 느려요**
A: 이미지 압축하거나 해상도 낮추기 (1920x1080 → 1280x720)

## 📤 GitHub Pages에서 이미지 사용

GitHub Pages에 올릴 때는 images 폴더도 함께 업로드하세요:

```bash
git add images/
git commit -m "Add project images"
git push
```

이미지가 많으면 Git LFS 사용 권장!
