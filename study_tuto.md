✅ 1단계: Git 사용 준비 (1회만 하면 됨)

 Git 설치 확인

git --version


 사용자 이름 설정

git config --global user.name "이름" #whgms259 ←개인 아이디


 사용자 이메일 설정

git config --global user.email "이메일" #whgms259@gmail.com  ←개인 메일


 설정 확인

git config --list

✅ 2단계: 로컬 저장소 실습

 새 폴더 생성

 해당 폴더에서 Git 초기화

git init


 상태 확인

git status

✅ 3단계: 파일 관리 기본 흐름

 파일 하나 생성 (예: README.md)

 변경 사항 확인

git status


 스테이징 영역에 추가

git add README.md   # README.md는 보내고 싶은 파일명


 커밋 생성

git commit -m "첫 커밋" #파일 등록할때 어떤 의도로 넣었는지를 적으면 좋음 딱히 중요한 것은 아님


 커밋 로그 확인

git log

✅ 4단계: GitHub 연동 (원격 저장소)

 GitHub에서 새 저장소 생성

 원격 저장소 등록

git remote add origin 저장소주소 #개인 깃허브에 저장소 생성해야함 https://github.com/whgms259/git_study_group ←이건 따로 생성한 저장소


 원격 저장소 확인

git remote -v


 최초 업로드

git push -u origin main #오류가 생기면 git push -u origin master를 입력 master가 기본값임 master도 안되면 저장소의 설정 들어가서 디폴트 브랜치 확인할 것

✅ 5단계: clone 실습 (다른 PC / 폴더)

 저장소 주소 복사

 복제

git clone 저장소주소


 원격 저장소 자동 연결 확인

git remote -v

✅ 6단계: 수정 → 업로드 → 동기화

 파일 수정

 상태 확인

git status


 add → commit

git add .
git commit -m "내용 수정"   #커밋한 내용 수정 코드


 원격 저장소 반영

git push


 다른 환경에서 변경 사항 가져오기

git pull

✅ 7단계: 브랜치 실습 (협업 핵심)

 브랜치 목록 확인

git branch


 새 브랜치 생성

git branch feature-test


 브랜치 이동

git switch feature-test


 작업 후 커밋

 main 브랜치로 이동

git switch main


 병합

git merge feature-test

✅ 8단계: 충돌(conflict) 체험

 같은 파일을 두 브랜치에서 수정

 merge 시 충돌 발생 확인

 충돌 파일 열어 수동 수정

 수정 후 add & commit

✅ 9단계: SSH 설정 (권장)

 SSH 키 생성

ssh-keygen


 공개키 확인

cat ~/.ssh/id_rsa.pub


 GitHub → Settings → SSH Keys 등록

 SSH 주소로 remote 변경

 push 시 비밀번호 미요청 확인

✅ 10단계: 반드시 익혀야 할 명령 요약

 git status

 git add

 git commit

 git push

 git pull

 git branch

 git switch

 git merge

 git log

 git diff

🎯 최종 목표 체크

 로컬에서 작업 → 커밋 가능

 GitHub와 연동 가능

 브랜치 작업 가능

 충돌 해결 경험 있음

 SSH로 인증 문제 없음

 