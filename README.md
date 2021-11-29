https://github.com/user/repository.git

https://user@bitbucket.org/group-name/repository.git

cd ~/dev/evan # 원하는 작업 디렉토리로 이동

git clone https://github.com/evan-moon/test-repo.git

git pull # 현재 내 로컬 브랜치와 같은 이름을 가진 리모트 서버 브랜치가 타겟

git pull origin master # origin 리모트 서버의 master 브랜치가 타겟

git fetch

#!/bin/bash

git fetch --all -p; git branch -vv | grep ": gone]" | awk '{ print $1 }' | xargs -n 1 git branch -d

git branch -vv

* master fa0cec5 [origin/master] 마스터 브랜치에욤
  test   1f3578f [origin/test: gone] 리모트에선 죽은 브랜치
  test2  fa0cec5 로컬에서 만들어지고 리모트에 업데이트는 안된 브랜치
git add . # 현재 디렉토리의 모든 변경사항을 스테이지에 올린다
git add ./src/components # components 디렉토리의 모든 변경사항을 스테이지에 올린다
git add ./src/components/Test.vue # 특정 파일의 변경사항만 스테이지에 올린다
git add -p # 변경된 사항을 하나하나 살펴보면서 스테이지에 올린다

$ git add ./soruce

$ git status

On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   source/_drafts/git-tutorial.md
  $ git log --graph

* commit 20f1ea9 (HEAD -> master, origin/master, origin/HEAD)
| Author: Evan Moon <bboydart91@gmail.com>
|
|     회원가입 기능 개발 끝!
|
* commit ca693fd
| Author: Evan Moon <coghcjf2@gmail.com>
|
|     회원가입 비밀번호 입력 폼 추가
|
* commit f9b6e2d
| Author: Evan Moon <coghcjf2@gmail.com>
|
|     회원가입 이메일 입력 폼 추가
|

$ git push origin master # origin 리모트 서버의 master 브랜치로 푸쉬해줘!
$ git push --set-upstream origin master

