# Git Test

## Git 명령어 예시

```bash
# 1. 새 폴더 생성 및 이동
mkdir git-test
cd git-test

# 2. Git 저장소 초기화
git init

# 3. README.md 작성 및 첫 커밋
echo "Git Test" > README.md
git add README.md
git commit -m "init README"

# 4. index.html 생성 및 커밋
echo "<h1>Git Test</h1>" > index.html
git add index.html
git commit -m "add index.html"

# 5. index.html 수정 및 커밋
echo "<h1>Git Test Updated</h1>" > index.html
git add index.html
git commit -m "update index.html"

# 6. git log로 커밋 ID 확인
git log --oneline

# 7. 2번째 커밋으로 되돌리기 (커밋 ID를 [커밋ID]로 대체)
git reset --hard [커밋ID]
```