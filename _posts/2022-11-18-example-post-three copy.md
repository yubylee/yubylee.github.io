---
title: Project 3
excerpt: |
feature_text: |
  # bitcamp naver cloud 1
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

## <span style="color:gray">_과제3 vm 생성 및 git 개인페이지 변경하기_</span>


 centos 5 생성

    -  project directory 생성

    - vegrantfile 준비

    - VM을 실행

 CENTOS5 VM 접속

    - vm ssh 접속

 git개인홈페이지 변경 

    1) yum git 설치

    2) nano 설치

    3) git config 의 email 과 name 설정

    4) git 개인페이지 저장소 복제

    5) [READ.ME](http://READ.ME) 편집

    6) git commit & push

mkdir centos3

cd centos3

vagrant init

→ 파일 만들어진곳가서 ex) vscode centos5 들어가서

[config.vm.box](http://config.vm.box) = “centos/7” -> base? box? 대신에 centos/7 기입

다른방법으로는 vagrant init centos/7           cmd에입력

config.vm.hostname = “myhost1.bitcamp”

vagrant up

vagrant ssh

hostname

-------------------------------------------
sudo yum install git

git --version

pwd

cd git

git clone https://github.com/yubylee.github.io       <- 자기 주소입력

sudo yum install nano

cd yubylee.github.io/

nano README.md                            <- 창뜨는데 이건형에 대하여 안녕하세요 이런식으로입력
내용입력 -> 컨트롤 o -> enter -> 컨트롤 x
git config --global user.email "yuby1003@naver.com"
git config --global user.name "LeeGunhyoung"

git add .
git commit -m "opera"
git push

네임 , 비번 입력

자기 깃허브 들어가서 리버지토리 들어가서 io들어가서 만들어진거 확인하면 끝

-------------------------------------------

삭제방법

vagrant halt

vagrant destroy

cd ..

dir

rmdir /s centos5


dir


----------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------

cd : 다른 디렉토리로 이동할 수 있습니다.  
dir : 디렉토리에 있는 파일과 하위 디렉토리 목록을 보여줍니다.  
mkdir : 디렉토리를 만듭니다.  
rmdir : 디렉토리를 지웁니다.  
git add : 작업 디렉토리 상의 변경 내용을 스테이징 영역에 추가하기 위해서 사용하는 gut 명령어  

git commit vs. git add
git add 명령어는 다음 변경(commit)을 기록할 때까지 변경분을 모아놓기 위해서 사용합니다. 따라서, git commit 명령어를 통해 명시적으로 기록을 남기기 전까지는 아무리 git add 명령어를 많이 실행해도 Git 저장소의 변경 이력에는 어떤 영향도 주지 않습니다.  

pwd : 현재 디렉토리 경로 보기  
git config --global user.name "자신의 닉네임"
git config --global user.email "자신의 이메일"    
: 버전에 포함될 정보를 설정. 이 설정은 ~/.gitconfig 파일에 저장되고 최초 1번만 설정해주면 된다.    
git clone https://github.com/git/git.git .
: url의 git 프로젝트를 현재 디렉토리(.)에 clone 한다.  

git push : 원격저장소로 푸쉬한다.  
git pull : 원격저장소의 내용을 로컬저장소르 내려받는다.  