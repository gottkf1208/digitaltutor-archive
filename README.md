# 디지털튜터 자료실

연수 마지막 날 만든 웹앱, 활동지, 발표자료, 영상 등을 모아 두는 공개 자료실입니다.

사이트: https://gottkf1208.github.io/digitaltutor-archive/

첫 자료는 [갤러리워크 투표 프로그램](https://gottkf1208.github.io/digitaltutorgallery/)입니다. 첫 화면 디자인은 사용자의 [코딩 아카이브](https://gottkf1208.github.io/quoka-archive/)를 참고했습니다.

## 새 자료 등록

1. 사이트에서 **자료 등록**을 누릅니다.
2. 제목, 분류, 만든 모둠, 공개 링크, 소개를 입력합니다. 태그와 미리보기 이미지는 선택입니다.
3. **등록 내용 준비하기**를 누르고 **GitHub에서 저장 완료하기**를 열면 이 저장소에 새 자료 파일을 만드는 화면으로 이동합니다.
4. 저장소에 쓰기 권한이 있는 GitHub 계정으로 로그인하고 **Commit changes**로 `main`에 저장합니다.
5. Actions의 배포가 완료되면 모든 방문자에게 자료가 표시됩니다. 배포 오류는 Actions에서 확인할 수 있습니다. 권한이 없는 이용자는 GitHub의 변경 제안 흐름을 사용하며, 관리자가 병합해야 공개됩니다.

파일 자체를 보관하려면 `files/`에 업로드하여 저장한 뒤 공개 파일 주소를 자료 링크로 등록합니다. 구글 드라이브, Canva 등 외부 자료는 방문자가 열 수 있도록 해당 서비스의 공유 설정도 확인해 주세요. 자료실과 저장소는 공개입니다.

## 관리

- `resources/`의 자료별 JSON을 수정하거나 삭제한 뒤 `main`에 저장하면 자동 반영됩니다. 자료 파일에는 `id`, `title`, `description`, `category`, `group`, `author`, `url`, `tags`, `date`가 필요하며 `image`, `featured`는 선택입니다.
- 이미지 파일은 `src/assets/`에 두고 `image`에 `assets/파일명.webp`처럼 입력하거나 공개 HTTPS 주소를 사용합니다.
- 이름·태그 검색, 자료 종류·모둠 필터, 정렬을 지원합니다. 별표는 **이 브라우저에만** 저장되며 공유되는 즐겨찾기가 아닙니다.
- **목록 내려받기**는 현재 공개된 전체 자료 목록을 JSON으로 내려받습니다.
- 공개 사이트에는 GitHub 토큰이나 비밀번호가 없습니다. 게시 권한은 GitHub 저장소 권한으로 관리합니다.

## 미리보기와 배포

Node.js 22 이상에서 `node scripts/build.mjs`로 자료 검증과 정적 파일 생성을 합니다. `node scripts/preview.mjs`를 실행하면 http://127.0.0.1:5175/digitaltutor-archive/ 에서 확인할 수 있습니다. GitHub Pages는 Actions 배포로 설정합니다.

갤러리워크 화면 이미지는 실제 프로그램에서 촬영했습니다. Pretendard 폰트 라이선스는 `licenses/LICENSE-Pretendard.txt`에 있습니다.
