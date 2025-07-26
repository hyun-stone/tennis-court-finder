# GitHub 업로드 가이드

## 1. GitHub 저장소 생성

1. GitHub.com에 로그인
2. 우측 상단의 "+" 버튼 클릭 → "New repository" 선택
3. 저장소 이름 입력 (예: `tennis-court-finder`)
4. Public 또는 Private 선택
5. "Create repository" 클릭

## 2. 로컬 Git 설정

### Git 초기화
```bash
git init
```

### 사용자 정보 설정 (처음 사용하는 경우)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 3. 파일 추가 및 커밋

### 모든 파일 추가
```bash
git add .
```

### 첫 번째 커밋
```bash
git commit -m "Initial commit: Tennis Court & Restaurant/Cafe Recommendation"
```

## 4. GitHub 저장소 연결

### 원격 저장소 추가
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
```

### 메인 브랜치 설정 (필요한 경우)
```bash
git branch -M main
```

## 5. GitHub에 업로드

### 푸시
```bash
git push -u origin main
```

## 6. API 키 설정 (중요!)

### 옵션 1: API 키 제거 (권장)
- `index.html`에서 실제 API 키를 `YOUR_KAKAO_JAVASCRIPT_KEY`로 변경
- README.md에 API 키 설정 방법 안내

### 옵션 2: 환경 변수 사용
- GitHub Secrets에 API 키 저장
- GitHub Actions를 통한 자동 배포 설정

## 7. 협업자 초대

1. GitHub 저장소 페이지에서 "Settings" 탭 클릭
2. 좌측 메뉴에서 "Collaborators" 선택
3. "Add people" 클릭
4. 협업자의 GitHub 사용자명 또는 이메일 입력
5. 권한 설정 후 초대

## 8. 추가 설정 (선택사항)

### GitHub Pages 배포
1. 저장소 Settings → Pages
2. Source를 "Deploy from a branch" 선택
3. Branch를 "main" 선택
4. "Save" 클릭

### Issues 및 Projects 설정
- 프로젝트 관리용 Issues 템플릿 생성
- Projects 보드 설정

## 주의사항

⚠️ **API 키 보안**
- 실제 API 키를 GitHub에 직접 업로드하지 마세요
- API 키는 환경 변수나 GitHub Secrets를 사용하세요

⚠️ **민감한 정보**
- 개인정보나 민감한 데이터가 포함된 파일은 제외하세요
- `.gitignore` 파일을 확인하여 불필요한 파일들이 제외되었는지 확인하세요 