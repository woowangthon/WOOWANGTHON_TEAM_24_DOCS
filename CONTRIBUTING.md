# 협업 규칙

최소한의 형식적 규칙

## 1. main 브랜치에 직접 push 금지
항상 브랜치를 따서 작업하고 PR로 합친다.

```bash
git checkout main
git pull                          # 최신 상태로
git checkout -b feat/login-page   # 내 작업 브랜치 만들기
# ... 작업 ...
git add .
git commit -m "feat: 로그인 화면 추가"
git push -u origin feat/login-page
```
그 다음 GitHub에서 **Pull Request** 만들고, 팀원 1명이 확인 후 merge.

## 2. 브랜치 이름
| 접두어 | 용도 | 예시 |
|---|---|---|
| `feat/` | 새 기능 | `feat/chat-api` |
| `fix/` | 버그 수정 | `fix/login-error` |
| `docs/` | 문서 | `docs/readme` |

## 3. 커밋 메시지
`종류: 무엇을 했는지` 형식으로 한국어로 작성 가능.
- `feat: 추천 API 연결`
- `fix: 빈 입력 시 에러 수정`
- `docs: 실행 방법 추가`

## 4. 절대 올리면 안 되는 것
- **API 키, 비밀번호** → `.env` 파일에만 넣기 (`.env`는 git에 안 올라가게 설정돼 있음)
- `node_modules/`, 가상환경 폴더
- 실수로 키를 올렸다면 **바로 팀장에게 말하고 키 재발급** (커밋 지워도 기록에 남음)

## 5. 막히면
혼자 2시간 이상 막히면 무조건 채널에 공유하기. 질문은 민폐가 아님.

## 6. merge 충돌이 나면
당황하지 말고 그대로 두고 팀장이나 git 익숙한 사람 부르기.
