# 다붓다붓 협동조합 홈페이지

충주청년상인협동조합 다붓다붓의 공식 홈페이지입니다.

---

## 📁 폴더 구조

```
다붓다붓-홈페이지/
├── index.html              ← 메인 페이지
├── projects.json           ← 프로젝트 정보 (사진 추가할 때 수정!)
├── README.md               ← 이 파일
└── images/
    ├── logo-hand.png       ← 다붓다붓 로고
    ├── leaflet-page-1.png  ← About 섹션 (회사 소개)
    ├── leaflet-page-2.png  ← Process 섹션 (3 STEP)
    ├── leaflet-page-3.png  ← Partners 섹션 (비누방울)
    ├── leaflet-page-4.png  ← 검증된 실적
    └── portfolio/
        ├── ureuk-festival/         ← 우륵문화제
        ├── dive-festival/          ← 다이브페스티벌
        ├── chungju-seollem/        ← 충주에설렘
        ├── neighborhood-rebrand/   ← 우리동네 리브랜딩
        ├── chungcheong-gamyeong/   ← 충청감영
        └── happiness-village/      ← 행복마을 아카이브
```

---

## 🚀 GitHub에 올리는 법 (처음 한 번만)

### 1단계: GitHub 계정 만들기

1. https://github.com 가입
2. 이메일 인증

### 2단계: 새 저장소(Repository) 만들기

1. 우측 상단 `+` 클릭 → `New repository`
2. **Repository name**: `dabutdabut` (또는 원하는 이름)
3. **Public** 선택 (무료 호스팅은 Public만 가능)
4. ✅ **Add a README file** 체크 안 함
5. `Create repository` 클릭

### 3단계: 파일 업로드

1. 만들어진 저장소 페이지에서 `uploading an existing file` 클릭
2. **이 폴더 안의 모든 파일/폴더를 그대로 드래그앤드롭**
   - `index.html`
   - `projects.json`
   - `README.md`
   - `images/` 폴더 통째로
3. 아래쪽 `Commit changes` 클릭

### 4단계: GitHub Pages 활성화

1. 저장소 페이지 상단의 `Settings` 클릭
2. 왼쪽 메뉴에서 `Pages` 클릭
3. **Source** → `Deploy from a branch` 선택
4. **Branch** → `main` + `/ (root)` 선택 → `Save`
5. 1~2분 기다리면 위쪽에 사이트 주소가 뜸:
   ```
   https://[내아이디].github.io/dabutdabut/
   ```

### 5단계: QR 코드 만들기

1. 위 사이트 주소를 네이버 단축 URL(https://me2.do)로 줄임
2. https://qr.naver.com 에서 줄인 주소로 QR 생성
3. 명함·제안서에 인쇄!

---

## 📸 프로젝트 사진 추가하는 법

### 한 프로젝트(예: 우륵문화제) 사진 추가

**1단계: 사진 준비**
- 사진 파일명을 `1.jpg`, `2.jpg`, `3.jpg`... 순서대로 바꿈
- 카드에 보일 대표 사진은 `thumb.jpg`로 저장
- 권장 사이즈: 가로 1600px 이하

**2단계: GitHub에 업로드**
1. GitHub 저장소 → `images/portfolio/ureuk-festival/` 폴더 들어가기
2. `Add file` → `Upload files`
3. 사진들 (`thumb.jpg`, `1.jpg`, `2.jpg`...) 드래그
4. `Commit changes`

**3단계: projects.json 수정**
1. `projects.json` 파일 클릭 → 연필 아이콘(편집)
2. 해당 프로젝트의 `"image_count": 0` 을 사진 개수로 변경
   ```json
   {
     "id": "ureuk-festival",
     "title": "우륵문화제",
     ...
     "image_count": 5   ← 사진 5장 올렸으면 5로 변경
   }
   ```
3. `Commit changes`

**4단계: 확인**
- 1~2분 후 사이트 새로고침
- 카드가 사진으로 바뀜 + 클릭하면 모달에 사진 슬라이드!

---

## 🆕 새 프로젝트 추가하는 법

### 1단계: 폴더 만들기

GitHub에서 `images/portfolio/` 안에 새 폴더 생성:
- 예: `cultural-event-2026/` (영문, 띄어쓰기 X, 소문자 추천)

### 2단계: 사진 업로드

위와 동일하게 `thumb.jpg`, `1.jpg`, `2.jpg`... 업로드

### 3단계: projects.json에 추가

기존 프로젝트 항목 아래에 새로 추가 (콤마 주의!):
```json
{
  "id": "cultural-event-2026",
  "title": "프로젝트 이름",
  "category": "문화·축제",
  "year": "2026",
  "tags": ["태그1", "태그2", "태그3"],
  "description": "프로젝트 설명 한두 문장.",
  "image_count": 5,
  "color": "green"
}
```

**color 옵션** (사진 없을 때 카드 배경색):
- `green` / `mustard` / `brown` / `darkgreen` / `mustarddark` / `greendark`

---

## ✏️ 텍스트 수정하는 법

### 연락처·주소 수정
`index.html` 파일에서 다음 부분 찾아서 수정:
- `(주소 추가 예정)` → 실제 주소
- `000-0000-0000` → 실제 전화번호
- `contact@dabutdabut.kr` → 실제 이메일

### 회사 소개·문구 수정
`index.html` 파일 검색 (Ctrl+F)으로 해당 텍스트 찾아서 수정

---

## 💡 자주 묻는 질문

**Q. 사진을 잘못 올렸어요. 삭제 어떻게 해요?**
A. GitHub 저장소에서 해당 파일 클릭 → 휴지통 아이콘 → Commit

**Q. 사이트가 안 보여요!**
A. Settings → Pages에서 활성화됐는지 확인. 활성화 후 1~2분 기다려야 함.

**Q. 이미지가 깨져 보여요.**
A. 파일명 대소문자 확인. `Thumb.JPG` ❌ / `thumb.jpg` ✅

**Q. 도메인을 다붓다붓.kr 같은 걸로 바꾸고 싶어요.**
A. 도메인 구입 후 Settings → Pages → Custom domain에 입력. DNS 설정 필요.

---

## 🎨 디자인 정보

- **메인 컬러**: 머스타드 옐로우 + 딥 그린 + 크림 베이지
- **폰트**: Pretendard (본문) + Gowun Batang (강조) + Cormorant Garamond (영문)
- **반응형**: 모바일·태블릿·데스크탑 모두 지원

---

© 2026 다붓다붓 협동조합
