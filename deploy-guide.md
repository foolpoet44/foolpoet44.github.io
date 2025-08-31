# 🚀 GitHub Pages 배포 완전 가이드

## 📋 사전 준비사항

### 1. GitHub 계정
- GitHub 계정이 필요합니다
- 없다면 [GitHub](https://github.com)에서 가입

### 2. Git 설치
- Windows: [Git for Windows](https://git-scm.com/download/win)
- Mac: `brew install git`
- Linux: `sudo apt-get install git`

## 🔧 단계별 배포 방법

### 1단계: GitHub 저장소 생성

1. **GitHub 로그인** 후 우측 상단 **+** 버튼 클릭
2. **New repository** 선택
3. 저장소 설정:
   - **Repository name**: `leadership-styles`
   - **Description**: `리더십 스타일 유형별 강점 분석`
   - **Public** 선택 (GitHub Pages 무료 사용)
   - **Add a README file** 체크 해제
   - **Create repository** 클릭

### 2단계: 로컬 파일 준비

```bash
# 프로젝트 폴더로 이동
cd /path/to/your/project

# Git 초기화
git init

# 모든 파일 추가
git add .

# 첫 번째 커밋
git commit -m "Initial commit: 리더십 스타일 분석 페이지"

# GitHub 저장소 연결 (사용자명 변경 필요)
git remote add origin https://github.com/사용자명/leadership-styles.git

# main 브랜치로 설정
git branch -M main

# GitHub에 업로드
git push -u origin main
```

### 3단계: GitHub Pages 활성화

1. **GitHub 저장소 페이지**에서 **Settings** 탭 클릭
2. 왼쪽 메뉴에서 **Pages** 선택
3. **Source** 섹션에서:
   - **Deploy from a branch** 선택
   - **Branch**: `main` 선택
   - **Folder**: `/(root)` 선택
4. **Save** 클릭

### 4단계: 배포 확인

- **5-10분 대기** 후 배포 완료
- 배포 URL: `https://사용자명.github.io/leadership-styles`
- 또는 Settings > Pages에서 URL 확인

## 📁 필수 파일 구조

```
leadership-styles/
├── index.html          # 메인 HTML 파일 (필수)
├── png/                # 이미지 폴더
│   ├── 1.png          # EI 스타일
│   ├── 2.png          # ER 스타일
│   ├── 3.png          # ES 스타일
│   ├── 4.png          # IE 스타일
│   ├── 5.png          # IR 스타일
│   ├── 6.png          # IS 스타일
│   ├── 7.png          # RE 스타일
│   ├── 8.png          # RI 스타일
│   ├── 9.png          # RS 스타일
│   ├── 10.png         # SE 스타일
│   ├── 11.png         # SI 스타일
│   └── 12.png         # SR 스타일
├── README.md           # 프로젝트 설명
└── .gitignore          # Git 무시 파일
```

## 🔍 문제 해결

### 이미지가 보이지 않는 경우
1. **파일명 확인**: `png/1.png` ~ `png/12.png` 정확히 맞는지 확인
2. **대소문자 확인**: GitHub Pages는 대소문자를 구분합니다
3. **파일 경로 확인**: HTML에서 `src="png/1.png"` 경로가 정확한지 확인

### 페이지가 로드되지 않는 경우
1. **index.html 파일명**: 반드시 `index.html`이어야 합니다
2. **브랜치 설정**: main 브랜치에서 배포되는지 확인
3. **배포 상태**: Settings > Pages에서 배포 상태 확인

### 스타일이 적용되지 않는 경우
1. **CSS 경로**: 모든 CSS가 HTML 내부에 포함되어 있는지 확인
2. **브라우저 캐시**: Ctrl+F5로 강제 새로고침
3. **HTTPS 확인**: GitHub Pages는 HTTPS로만 제공됩니다

## 📱 모바일 최적화 확인

1. **반응형 디자인**: 다양한 화면 크기에서 테스트
2. **터치 인터페이스**: 모바일에서 카드 터치 확인
3. **로딩 속도**: 이미지 최적화 상태 확인

## 🔄 업데이트 방법

```bash
# 파일 수정 후
git add .
git commit -m "Update: 내용 수정"
git push origin main

# GitHub Pages는 자동으로 재배포됩니다
```

## 📊 배포 상태 모니터링

- **GitHub Actions**: 자동 배포 로그 확인
- **Settings > Pages**: 배포 상태 및 URL 확인
- **Network 탭**: 이미지 로딩 상태 확인

## 🎯 성공적인 배포 확인 체크리스트

- [ ] GitHub 저장소 생성 완료
- [ ] 모든 파일 업로드 완료
- [ ] GitHub Pages 활성화 완료
- [ ] 배포 URL 접속 가능
- [ ] 모든 이미지 정상 표시
- [ ] 반응형 디자인 작동
- [ ] 호버 효과 정상 작동
- [ ] 모바일에서 정상 표시

## 📞 추가 지원

문제가 발생하면:
1. GitHub 저장소의 Issues 탭에서 문제 보고
2. 브라우저 개발자 도구의 Console 탭 확인
3. Network 탭에서 파일 로딩 상태 확인
