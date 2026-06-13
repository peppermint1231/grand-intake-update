# GitHub 업로드 순서

## 1. 저장소 만들기

GitHub 로그인 후:

```text
New repository
Repository name: grand-intake-update
Public 선택
Create repository
```

## 2. 파일 업로드

저장소 첫 화면에서:

```text
uploading an existing file
또는
Add file → Upload files
```

아래 파일/폴더를 전부 올립니다.

```text
version.json
index.html
.nojekyll
README.md
GITHUB_UPLOAD_GUIDE.md
UPDATE_WORKFLOW.md
apk/
```

## 3. APK 넣기

`apk` 폴더 안에 실제 release APK를 넣습니다.

현재 예시 파일명:

```text
apk/grand-intake-v18.8.apk
```

아직 APK가 없다면 `apk/PUT_RELEASE_APK_HERE.txt`만 올려두고, 나중에 release APK를 올리면 됩니다.

## 4. version.json 수정

`YOUR_GITHUB_ID` 부분을 본인 GitHub 아이디로 바꿉니다.

예:

```text
https://YOUR_GITHUB_ID.github.io/grand-intake-update/apk/grand-intake-v18.8.apk
```

을

```text
https://grandclinic.github.io/grand-intake-update/apk/grand-intake-v18.8.apk
```

처럼 변경합니다.

## 5. GitHub Pages 켜기

```text
Settings
→ Pages
→ Build and deployment
→ Source: Deploy from a branch
→ Branch: main
→ Folder: /root
→ Save
```

## 6. 확인 주소

브라우저에서 아래 주소가 열리면 성공입니다.

```text
https://YOUR_GITHUB_ID.github.io/grand-intake-update/
https://YOUR_GITHUB_ID.github.io/grand-intake-update/version.json
```

## 7. 앱에 넣을 업데이트 확인 주소

나중에 앱 업데이트 기능에 넣을 주소:

```text
https://YOUR_GITHUB_ID.github.io/grand-intake-update/version.json
```
