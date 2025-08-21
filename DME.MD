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

## 브랜치 및 충돌 해결 예시clear

```bash
# 2. 브랜치 test-login 생성 후 이동
git checkout -b test-login

# 2.1 login.html 파일 생성 및 커밋
echo "<h2>Login Page</h2>" > login.html
git add login.html
git commit -m "add login page"

# 2.2 main 브랜치로 이동 후 login.html 생성 및 커밋
git checkout main
echo "<h2>Main Login</h2>" > login.html
git add login.html
git commit -m "add main login"

# 2.3 test-login 브랜치를 main에 병합
git merge test-login

# 2.4 충돌 해결 후 커밋
# (충돌 파일 수정 후)
git add login.html
git commit -m "resolve merge conflict in login.html"
```

## 원격 저장소 연결 및 푸시

```bash
# 3. GitHub에 git-test 원격 저장소 생성 후 연결
git remote add origin https://github.com/사용자명/git-test.git

# 3.1 main 브랜치 푸시
git push -u origin main

# 3.2 test-login 브랜치에서 수정 후 원격에 푸시
git checkout test-login
# (수정 작업)
git add .
git commit -m "edit on test-login branch"
git push origin test-login
```

## main1.html 파일 작업 및 커밋 되돌리기

```bash
# 4. main1.html 생성 및 커밋
echo "<p>Main1 Page</p>" > main1.html
git add main1.html
git commit -m "add main1.html"

# 4.1 main1.html 내용 수정 및 커밋
echo "<p>Main1 Git</p>" > main1.html
git add main1.html
git commit -m "update main1.html"

# 4.2 마지막 커밋 삭제 (내용은 그대로)
git reset --soft HEAD~1
```

## 브랜치 히스토리 및 충돌 변경 사항 확인

```bash
# 5. 브랜치 히스토리 시각화
git log --graph --oneline --all

# 5.1 충돌 시 변경 사항 확인
git diff
```
