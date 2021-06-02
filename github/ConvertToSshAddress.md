GitHub에 이미 ssh 키가 등록되어 있다고 가정한다.

## [1] 기존 GitHub 저장소를 https에서 ssh로 전환하는 방법
1. GitHub에서 Code / Clone / SSH를 눌러 SSH 주소를 복사
2. Local repository에서 아래와 같이 입력 후 enter
<code> (local_repository)$ git config remote.origin.url 위에서_복사한_SSH_주소 </code>
3. 확인
<code> (local_repository)$ git remote -v 

