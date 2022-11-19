---
title: Project 3
excerpt: |
feature_text: |
  # bitcamp naver cloud 1
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

## 과제3 

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

삭제방법

vagrant halt

vagrant destroy

cd ..

dir

rmdir /s centos5
y

dir
