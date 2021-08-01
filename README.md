# git_pratice

Git Pull Request Pratice

1. github organization과 연습을 위한 repository 생성
2. repository를 각자의 계정으로 fork
3. fork된 자신의 repository를 local에 clone
4. README.md에 팀 멤버를 추가하고 Pull Request 생성
5. 메인테이너는 code base가 일치하는 지 확인하고 불일치하면 rebase 요청
6. contributor는 아래의 명령어를 통해 fetch, rebase를 거쳐 re-pull request
```sh

# 바뀐 upstream 프로젝트의 master 브랜치 commit 가져오기
$ git fetch upstream master

# upstream/master로 rebase 하기
$ git rebase upstream/master

# 충돌 상황 확인하기
$ git status
$ git diff

# 충돌 부분( >>>> 등)을 수동으로 수정해서 정리하고
$ nano README.md

# 다시 멈춘 rebase 진행하기
$ git add README.md
$ git rebase --continue

# Pull-Request 갱신하기 (에시: PR보낸 브랜치가 master일 경우)
# force push 이후에 회색 merge버튼이 초록색으로 변했는지
# upstream 프로젝트 GitHub사이트 pull request게시판에서 확인하기
$ git push origin master -f

```

## Team member

- jae yong Lee 
- Jian Lee 
- seunghyun Lim 
