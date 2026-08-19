# kt cloud TECH UP 정적 사이트

[ktcloud-techup.com](https://ktcloud-techup.com/) 을 최대한 동일하게 정적 HTML/CSS/JS로 구현한 사이트입니다.

## 로컬 실행

```bash
# Python 3
python -m http.server 8000

# 또는 Node.js (npx)
npx serve .
```

브라우저에서 `http://localhost:8000` 으로 접속하세요.

## 배포 (GitHub Pages)

1. `main` 브랜치에 변경사항 반영
2. Repository Settings → Pages
3. Source: `Deploy from a branch`
4. Branch: `main`, Folder: `/ (root)` 선택 후 저장
5. 약 1~2분 후 `https://<username>.github.io/<repo>/` 에서 확인

### 커스텀 도메인 적용 시

1. DNS에서 `yourdomain.com` CNAME 레코드를 `<username>.github.io` 로 지정
2. 레포 루트에 `CNAME` 파일 생성 (내용: 도메인명만)
3. Pages 설정에서 Custom domain 입력 후 저장

## 수정 프로세스

1. 기능별 브랜치 생성: `git checkout -b feature/변경내용`
2. 파일 수정 후 커밋: `git add -A && git commit -m "설명"`
3. 원격 push: `git push -u origin 브랜치명`
4. GitHub에서 Pull Request 생성 (base: `main`)
5. 리뷰 후 Merge → Pages 자동 재배포

## 페이지 구성

| URL | 파일 |
|---|---|
| `/` | `index.html` |
| `/frontend/` | `frontend/index.html` |
| `/backend/` | `backend/index.html` |
| `/fullstack/` | `fullstack/index.html` |
| `/gen-ai/` | `gen-ai/index.html` |
| `/cybersecurity/` | `cybersecurity/index.html` |
| `/cloud-native/` | `cloud-native/index.html` |
| `/cloud-infra/` | `cloud-infra/index.html` |
| `/product-design/` | `product-design/index.html` |
| `/product-management/` | `product-management/index.html` |

## 변경 이력 (Changelog)

### v2 (2026-08-20)
- 원본 사이트 구조/디자인 전면 재작성
- Vimeo 히어로 영상 + 원본 히어로 카드 2종 복원
- 3그룹 드롭다운 네비게이션 (원본 동일)
- 과정 카드 레이아웃: 웹개발 3열 / 인프라 4열 / 프로덕트 2열
- 9개 과정 상세 페이지: 스티키 서브 내비, FAQ 아코디언(3탭), 커리큘럼 다운로드
- 원본 CDN 이미지 및 로고 재사용

### v1 (초기 구축)
- 전역 떠다니는 채널 버튼 제거
- 인스타그램 연결 및 이미지 제거
- 메인 "지원 확인" 버튼 제거
- 모든 지원 CTA → `https://forms.gle/zZFbDgqRrS6WZeDd9` 통일
- 하위 과정 페이지 직접 URL 접근 지원 (`/frontend/` 등)

## 배포 URL

- **메인**: https://kpiiorkr.github.io/ktcloudKDT_202608/
