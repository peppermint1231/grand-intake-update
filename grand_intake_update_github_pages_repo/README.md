# 그랜드 초진설문지 업데이트 서버

이 저장소는 GitHub Pages를 이용해 `그랜드 초진설문지` 태블릿 앱 업데이트 파일을 배포하기 위한 저장소입니다.

## 저장소 구조

```text
grand-intake-update/
├─ version.json
├─ index.html
├─ .nojekyll
└─ apk/
   └─ grand-intake-v18.8.apk
```

## 절대 올리면 안 되는 파일

아래 파일은 환자 개인정보가 포함될 수 있으므로 이 저장소에 절대 올리지 마세요.

```text
records.json
CSV
동의서 PNG
backup 파일
logs 중 환자정보가 들어간 파일
```

## 처음 GitHub에 올리는 방법

1. GitHub에서 새 저장소를 만듭니다.

```text
Repository name: grand-intake-update
Visibility: Public
```

2. 이 ZIP 안의 파일을 저장소 루트에 업로드합니다.

```text
version.json
index.html
.nojekyll
apk/
README.md
GITHUB_UPLOAD_GUIDE.md
UPDATE_WORKFLOW.md
```

3. GitHub Pages를 켭니다.

```text
Settings
→ Pages
→ Source: Deploy from a branch
→ Branch: main
→ Folder: /root
→ Save
```

4. 생성된 주소를 확인합니다.

```text
https://YOUR_GITHUB_ID.github.io/grand-intake-update/version.json
```

## 새 APK 업데이트할 때

1. Android Studio에서 release APK를 빌드합니다.
2. APK 파일명을 버전에 맞게 변경합니다.

```text
grand-intake-v18.9.apk
```

3. `apk/` 폴더에 업로드합니다.
4. `version.json`을 수정합니다.

```json
{
  "versionName": "18.9",
  "versionCode": 189,
  "apkFileName": "grand-intake-v18.9.apk",
  "apkUrl": "https://YOUR_GITHUB_ID.github.io/grand-intake-update/apk/grand-intake-v18.9.apk"
}
```

5. Commit changes를 누릅니다.

## 중요

`versionCode`는 반드시 이전보다 커야 합니다.

```text
18.8 = 188
18.9 = 189
19.0 = 190
```

앱 업데이트 기능을 넣을 때는 아래 주소를 앱에 고정하면 됩니다.

```text
https://YOUR_GITHUB_ID.github.io/grand-intake-update/version.json
```
