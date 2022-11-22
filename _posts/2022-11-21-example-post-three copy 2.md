---
title: Project 4(Git저장소)
excerpt: |
feature_text: |
  # bitcamp naver cloud 1
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

## <span style="color:gray">_로컬 GIT 저장소를 만들고 GITHUB.COM의 개인 저장소와 연결하라_</span>


과제 목표
작업내용: (host1 리눅스 VM에서 작업을 수행한다.)

1) 다음의 경로에 로컬 깃 저장소를 생성한다.

    ~/git/bitcamp-ncp2/

2) 다음의 테스트 파일을 생성하고 로컬 저장소에 커밋한다.

    ~/git/bitcamp-ncp2/a.txt 

    a.txt 파일의 내용을 아무거나 입력한다.

3) github.com의 개인 계정에 bitcamp-ncp2 이름으로 저장소를 생성한다.

4) 로컬 깃 저장소와 원격 깃 저장소를 연결한다.

5) 로컬 깃 저장소의 내용을 원격 저장소에 push 한다.


-------------------------------------------------------------------------------

해당 리눅스 서버 접속 vagran ssh  
cd git  
git config --global user.name "LeeGunhyoung"  
git config --global user.email "yuby1003@naver.com"  
git config -l  
mkdir bitcamp-ncp3(저장소생성)  
cd bitcamp-ncp3  
sudo yum install nano  
git init  
ls -al  
nano a.txt  
ls -al  
git status --short  
git remote add origin https://github.com/yubylee/bitcamp-ncp4(깃허브에 리퍼지토리 생성후)  
git remote -v  
git remote show origin  
git pull  
git branch  
git branch -m "main"  
git branch  
git add .  
git commit -m ""  
git push --set-upstream origin main  


-------------------------------------------------------------------------------
1. ruby 설치
2. gem install "테마" -v "버젼"
 - 테마는 기본이 jekyll 이고 너가 선택한 테마는
 xxx.gemspec에 있는 보통 spec.name을 넣으면 됨
버젼은 spec.version

3. bundle install 해서 번들 설치

4. bundler exec jekyll serve 실행하면 로컬 서버에 블로그 실행됨

5. html,css,javascript는 static contents이기 때문에 수정이 실시간으로 된다. 만약안되면 강력 새로고침 후 확인한다.

6. yml 같은 파일은 로컬 서버에 빌드할때 컴파일(?)해서 올리므로 실시간으로 수정이 안되므로 서버를 내리고 수정 후 다시 서버를 올려야 한다.

* 그래서 그냥 뭔가 수정이 안되는 느낌이라면 서버를 내렸다가 다시 올려서 확인해본다. ctrl+c 누른 후 4번 실행