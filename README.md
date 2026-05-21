# 다붓다붓 협동조합 홈페이지

충주 기반 문화기획·브랜딩·콘텐츠 전문가 그룹, 다붓다붓 협동조합의 공식 홈페이지입니다.

---

## 📁 폴더 구조

```
dabutdabut/
├── index.html                          ← 메인 페이지
├── projects.json                       ← 프로젝트 정보 (사진 추가할 때 수정)
├── dabutdabut-company-profile.pdf      ← 회사소개서 (다운로드 버튼용)
├── README.md
└── images/
    ├── logo-hand.png                   ← 다붓다붓 로고 (녹색)
    ├── logo-hand-mustard.png           ← 머스타드 컬러 로고
    ├── logo-hand-cream.png             ← 크림 컬러 로고
    ├── leaflet-page-1.png              ← About 섹션 (회사 소개)
    ├── leaflet-page-2.png              ← Process 참고 이미지
    ├── leaflet-page-3.png              ← Partners 비누방울 이미지
    ├── leaflet-page-4.png              ← 검증된 실적 이미지
    └── portfolio/
        ├── ureuk-festival/             ← 우륵문화제
        ├── dive-festival/              ← 다이브페스티벌
        ├── chungju-seollem/            ← 충주에설렘
        ├── neighborhood-rebrand/       ← 우리동네 리브랜딩
        ├── chungcheong-gamyeong/       ← 충청감영
        └── happiness-village/          ← 행복마을 아카이브
```

---

## 🚀 GitHub에 업데이트하는 법

기존 dabutdabut 저장소에 새 파일들을 올리면 됩니다.

### 1. 메인 파일 교체
- `index.html` → 기존 파일 삭제 후 새 파일 업로드 (또는 편집 → 전체 교체)
- `dabutdabut-company-profile.pdf` → 새로 업로드

### 2. (이미 있다면 건너뛰기) 이미지 파일들
다음 파일들이 `images/` 폴더에 있어야 합니다:
- logo-hand.png, logo-hand-mustard.png, logo-hand-cream.png
- leaflet-page-1.png ~ leaflet-page-4.png

### 3. portfolio 폴더 (사진 추가용)
사진 추가 전이라도 `projects.json`을 통해 자동으로 카드가 생성됩니다.

---

## 📧 사업 문의 폼 (Formspree)

### 작동 방식
1. 방문자가 폼 작성 후 "문의 보내기" 클릭
2. Formspree가 자동으로 처리
3. **aspooncj@naver.com** 으로 메일 발송
4. 메일에서 바로 답장 가능

### 한도
- 무료 플랜: **월 50건**
- 50건 초과시 다음 달까지 대기 또는 유료 업그레이드

### 설정 확인
- Form Endpoint: `https://formspree.io/f/xnjrpklj`
- 첫 문의 받을 때 Formspree에서 인증 메일이 옵니다 (한 번만 클릭)

---

## 📸 프로젝트 사진 추가하는 법

### 1단계: 사진 준비
- 파일명: `1.jpg`, `2.jpg`, `3.jpg`... 순서대로
- 썸네일: `thumb.jpg` (카드에 표시)
- 권장 크기: 가로 1600px 이하

### 2단계: GitHub 업로드
1. GitHub 저장소 → `images/portfolio/ureuk-festival/` 등 해당 폴더 들어가기
2. `Add file` → `Upload files`
3. 사진들 드래그앤드롭 → `Commit changes`

### 3단계: projects.json 수정
1. `projects.json` 클릭 → 연필(편집)
2. 해당 프로젝트의 `"image_count": 0` 을 사진 개수로 변경:
   ```json
   "image_count": 5   ← 사진 5장 올렸으면 5
   ```
3. `Commit changes`

### 4단계: 확인
1~2분 후 사이트 새로고침 → 카드가 사진으로 바뀌고, 클릭하면 슬라이드!

---

## 🆕 새 프로젝트 추가하는 법

### 1단계: 새 폴더 만들기
`images/portfolio/` 안에 새 폴더 (예: `cultural-2026`)

### 2단계: 사진 업로드
위 방법대로 `thumb.jpg`, `1.jpg`, `2.jpg`... 업로드

### 3단계: projects.json에 추가
```json
{
  "id": "cultural-2026",
  "title": "프로젝트명",
  "category": "문화·축제",
  "year": "2026",
  "tags": ["태그1", "태그2"],
  "description": "프로젝트 설명",
  "image_count": 5,
  "color": "green"
}
```

**color 옵션** (사진 없을 때 카드 배경):
- `green` / `mustard` / `brown` / `darkgreen` / `mustarddark` / `greendark`

---

## ✏️ 텍스트 수정하는 법

`index.html` 파일에서 Ctrl+F로 검색해서 수정:
- 연락처: `010-9407-8186`, `aspooncj@naver.com`
- 주소: `충청북도 충주시 관아4길 16, 2층`
- 회사 소개 문구
- Stats 숫자 (5+ 파트너사, 6대 사업영역 등)

---

## 💡 자주 묻는 질문

**Q. 사이트 주소가 뭐예요?**
A. `https://sinyh1035-beep.github.io/dabutdabut/`

**Q. 폼 전송이 안 돼요.**
A. Formspree 첫 사용 시 형의 이메일로 인증 메일이 옵니다. 인증 후 정상 작동합니다.

**Q. 회사소개서 PDF가 안 다운로드돼요.**
A. `dabutdabut-company-profile.pdf` 파일이 저장소 루트(index.html과 같은 위치)에 있는지 확인하세요.

**Q. 도메인을 바꾸고 싶어요.**
A. 도메인 구입 후 Settings → Pages → Custom domain 입력. DNS A 레코드 설정 필요.

---

© 2026 다붓다붓 협동조합 (DABUTDABUT COOPERATIVE)
