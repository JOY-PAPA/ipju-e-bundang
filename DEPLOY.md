# 배포 메모 — 입주 가이드 (e편한세상 분당 퍼스트빌리지)

이 폴더의 파일을 그대로 GitHub Pages(또는 Vercel)에 올리면 됩니다. 빌드 과정 없음.

| 파일 | 용도 |
|---|---|
| `index.html` | 입주 가이드 앱 (단일 파일, 평면도 내장) |
| `manual.html` | 사용법 설명서 — 앱의 「사용법」 버튼이 `manual.html`(상대 경로)로 연결됩니다 |
| `README.md` | 저장소 설명 |
| `vercel.json` | Vercel 전용 보안 헤더. GitHub Pages에서는 무시됩니다 |

## GitHub Pages 순서 (새 Cowork 작업에서 Claude가 하거나, 직접 해도 됩니다)

1. GitHub에서 **공개(Public)** 저장소를 하나 만듭니다. 예: `ipju-bundang`
2. 이 폴더의 `index.html`, `manual.html`, `README.md`, `vercel.json`을 저장소 루트(`main` 브랜치)에 올립니다.
3. 저장소 **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / 폴더 **/(root)** → Save
4. 1~2분 뒤 주소가 생깁니다: `https://<계정>.github.io/<저장소>/`
   - 앱: `https://<계정>.github.io/<저장소>/`
   - 설명서: `https://<계정>.github.io/<저장소>/manual.html`

## 새 Cowork 작업에 붙여 넣을 요청문

> 이 작업에 연결한 GitHub 저장소에, 연결한 폴더 `입주까지_분당퍼스트빌리지`의 index.html · manual.html · README.md · vercel.json을 main 브랜치 루트에 커밋하고, GitHub Pages를 main / root로 켜 주세요. 끝나면 Pages 주소를 알려 주세요.

(새 작업을 만들 때 **저장소**와 **이 폴더**를 함께 연결해야 Claude가 파일을 읽고 푸시할 수 있습니다.)

## 수정이 필요할 때

- 날짜·금액·옵션은 `index.html` 안 `const PROJECT = {` 블록(단지 데이터) 한 곳에만 있습니다.
- 임시로 넣어 둔 값: 입주일 `moveIn: "2029-02-01"`(공고문은 ’29.02월), 추가선택품목(Ⅲ) 계약일 `m11` 의 `d: "2026-12-01"`(공고문은 추후 안내).
