---
title: Project 6(리눅스명령어 1)
excerpt: |
feature_text: |
  # bitcamp naver cloud 1
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

## <span style="color:gray">_제시된 리눅스 기본 명령어 매뉴얼을 작성하시오._</span>


과제 목표
작업 내용
명령어 - 명렁어에 대한 간단한 설명

$ 명령어의 사용예

출력 결과 일부

 

예)

pwd - 현재 작업 디렉토리를 표시

$ pwd

/home/vagrant

 

1. 파일 시스템 탐색 기본 명령어

pwd, cd, ls, file, less

 

2. 파일과 디렉토리 조작 명령어

cp, mv, mkdir, rm, ln

 

3. 명령어를 다루는 명령어

type, which, man, apropos, info, whatis, alias



-------------------------------------------------------------------------------
1) 파일 시스템 탐색 기본 명령어



1.pwd - 현재 작업 중인 디렉토리의 절대 경로를 출력하는 명령어이다.

[vagrant@host1 ~]$ pwd

/home/vagrant



2.cd - 디렉토리 이동

[vagrant@host1 ~]$ cd git

[vagrant@host1 git]$



3.ls - 현재위치에 파일목록 조회

[vagrant@host1 git]$ ls

bitcamp-ncp bitcamp-ncp2 bitcamp-study bitcamp-test



ls 명령어 -a 옵션 (all)



숨겨진 파일이나 디렉토리도 보여준다.



ls 명령어 -l 옵션 (long)



자세한 내용을 출력한다.



내용> 퍼미션(권한), 포함된 파일수, 소유자, 그룹, 파일크기, 수정일자, 파일이름



ls 명령어 -S 옵션 (size)



파일 크기 순으로 정렬하여 출력한다.



ls 명령어 -r 옵션 (reverse)



거꾸로 출력한다. (ls 명령어의 기본은 알파벳 순서다.)



ls 명령어 -R 옵션 (recursive)



하위 디렉토리까지 출력한다.



ls 명령어 -h 옵션 (human)



K, M, G 단위를 사용하여 파일 크기를 사람이 보기 좋게 표시한다.



ls 명령어 u, c 옵션



ls -l 명령은 기본적으로 mtime(수정시간)을 출력한다.



ls -lu



u 옵션을 사용하면 atime(접근 시간)을 출력한다.



ls -lc



c 옵션을 사용하면 ctime(변경 시간)을 출력한다.





4.file - 파일 종류 확인하기





[vagrant@host1 git]$ file

Usage: file [-bchikLlNnprsvz0] [--apple] [--mime-encoding] [--mime-type]

[-e testname] [-F separator] [-f namefile] [-m magicfiles] file ...

file -C [-m magicfiles]

file [--help]





5.less - 파일의 내용을 한 화면에 보여주는 명령어





[vagrant@host1 git]$ less bitcamp-ncp



total 24

drwxrwxr-x. 3 vagrant vagrant 123 Nov 21 18:22 ./

drwxrwxr-x. 6 vagrant vagrant 86 Nov 21 19:05 ../

-rw-rw-r--. 1 vagrant vagrant 30 Nov 21 17:12 b.txt

-rw-rw-r--. 1 vagrant vagrant 5 Nov 21 17:12 c.txt

-rw-rw-r--. 1 vagrant vagrant 10 Nov 21 18:22 d.txt

drwxrwxr-x. 8 vagrant vagrant 220 Nov 21 18:22 .git/

-rw-rw-r--. 1 vagrant vagrant 3593 Nov 21 05:48 .gitignore

-rw-rw-r--. 1 vagrant vagrant 0 Nov 21 11:06 hello2.txt

-rw-rw-r--. 1 vagrant vagrant 13 Nov 21 08:40 README.md

-rw-rw-r--. 1 vagrant vagrant 10 Nov 21 18:22 x.txt



나가기 q



(2) 파일과 디렉토리 조작 명령어





1.cp - 복사하는 명령어





[vagrant@host1 bitcamp-test]$ dir

a.txt cost.txt dev.txt gun.txt mj3.txt no.txt sgw.txt yes.txt

b.txt c.txt function.txt lee.txt mj4.txt README.md ssl.txt yubylee.txt

[vagrant@host1 bitcamp-test]$ cp yubylee.txt project.txt

[vagrant@host1 bitcamp-test]$ dir

a.txt cost.txt dev.txt gun.txt mj3.txt no.txt README.md ssl.txt





2.mv - 이동하는 명령어





a.txt cost.txt dev.txt gun.txt mj3.txt no.txt README.md ssl.txt yubylee.txt

b.txt c.txt function.txt lee.txt mj4.txt project.txt sgw.txt yes.txt

[vagrant@host1 bitcamp-test]$ mv yubylee.txt project.txt

[vagrant@host1 bitcamp-test]$ dir

a.txt cost.txt dev.txt gun.txt mj3.txt no.txt README.md ssl.txt

b.txt c.txt function.txt lee.txt mj4.txt project.txt sgw.txt yes.txt





3.mkdir - 디렉토리 생성할 경우 사용되는 명령어





[vagrant@host1 git]$ mkdir yu

[vagrant@host1 git]$ dir

bitcamp-ncp bitcamp-ncp2 bitcamp-study bitcamp-test yu





4.rm - 파일 혹은 디렉토리를 삭제하는 명령어





a.txt cost.txt dev.txt gun.txt mj3.txt no.txt README.md ssl.txt

b.txt c.txt function.txt lee.txt mj4.txt project.txt sgw.txt yes.txt

[vagrant@host1 bitcamp-test]$ rm project.txt

[vagrant@host1 bitcamp-test]$ dir

a.txt cost.txt dev.txt gun.txt mj3.txt no.txt sgw.txt yes.txt

b.txt c.txt function.txt lee.txt mj4.txt README.md ssl.txt





5.ln - 링크를 만드는 명령줄





[vagrant@host1 test123]$ ln aaa.txt ccc.txt

[vagrant@host1 test123]$ ls

aaa.txt bbb.txt ccc.txt t



(3) 명령어를 다루는 명령어





1.type - 명령 유형에 대한 정보를 표시하는 데 사용





[vagrant@host1 test123]$ type wc

wc is /usr/bin/wc





2.which - 특정명령어의 위치를 찾아주는 명령어





[vagrant@host1 test123]$ which fin

/usr/bin/which: no fin in (/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/vagrant/….




man - 프로그램의 사용법(매뉴얼)을 확인



[vagrant@host1 test123]$ man rm



RM(1) User Commands RM(1)



NAME

rm - remove files or directories



SYNOPSIS

rm [OPTION]... FILE...



DESCRIPTION

This manual page documents the GNU version of rm. rm removes each specified file. By default, it does not remove directories.



   If  the  -I or --interactive=once option is given, and there are more than three files or the -r, -R, or --recursive are given, then rm prompts the user for whether to proceed with the entire operation.  If the response is
   not affirmative, the entire command is aborted.

   Otherwise, if a file is unwritable, standard input is a terminal, and the -f or --force option is not given, or the -i or --interactive=always option is given, rm prompts the user for whether to remove the  file.   If  the
   response is not affirmative, the file is skipped.



OPTIONS

Remove (unlink) the FILE(s).



   -f, --force
          ignore nonexistent files and arguments, never prompt

   -i     prompt before every removal

   -I     prompt once before removing more than three files, or when removing recursively; less intrusive than -i, while still giving protection against most mistakes

   --interactive[=WHEN]
          prompt according to WHEN: never, once (-I), or always (-i); without WHEN, prompt always



Manual page rm(1) line 1 (press h for help or q to quit)



q키 - 나가기 (quit)



h키 - man 사용법 확인 (help)



위, 아래 화살표키, 엔터키 - 한줄씩 넘기기



Page Up, Page Down, 스페이스바 - 한 페이지씩 넘기기





3.apropos - 검색어와 관련있는 명령어를 설명과 함께 출력





[vagrant@host1 test123]$ apropos dir

addgnupghome (8) - Create .gnupg home directories

alphasort (3) - scan a directory for matching entries

basename (1) - strip directory and suffix from filenames

basename (1p) - return non-directory portion of a pathname

bdflush (2) - start, flush, or tune buffer-dirty-flush daemon

cacertdir_rehash (8) - simple script to create or update hash links to certificate files in a directory

cd (1p) - change the working directory

chacl (1) - change the access control list of a file or directory

chdir (2) - change working directory

chdir (3p) - change working directory

chroot (1) - run command or interactive shell with special root directory

chroot (2) - change root directory

closedir (3) - close a directory

closedir (3p) - close a directory stream

cp (1) - copy files and directories

Cwd (3pm) - get pathname of current working directory

dbus-cleanup-sockets (1) - clean up leftover sockets in a directory

depmod.d (5) - Configuration directory for depmod

dir (1) - list directory contents

dir_colors (5) - configuration file for dircolors(1)

dircolors (1) - color setup for ls

dirent.h (0p) - format of directory entries

dirfd (3) - get directory stream file descriptor

DirHandle (3pm) - supply object methods for directory handles

dirname (1) - strip last component from file name

dirname (1p) - return the directory portion of a pathname

dirname (3) - parse pathname components

dirname (3p) - report the parent directory name of a file pathname

dirs (1) - bash built-in commands, see bash(1)

faccessat (2) - check user's permissions of a file relative to a directory file descriptor

fchdir (2) - change working directory

fchdir (3p) - change working directory

fchmodat (2) - change permissions of a file relative to a directory file descriptor

fchownat (2) - change ownership of a file relative to a directory file descriptor

fdopendir (3) - open a directory

fegetround (3p) - get and set current rounding direction

fesetround (3p) - get and set current rounding direction

File::Basename (3pm) - Parse file paths into directory, filename and suffix.

File::Find (3pm) - Traverse a directory tree.

File::Path (3pm) - Create or remove directory trees

file_contexts.homedirs (5) - userspace SELinux labeling interface and configuration file format for the file contexts backend

find (1) - search for files in a directory hierarchy

FindBin (3pm) - Locate directory of original perl script

firewalld.direct (5) - firewalld direct configuration file

fstatat (2) - get file status relative to a directory file descriptor

fstatat64 (2) - get file status relative to a directory file descriptor

futimesat (2) - change timestamps of a file relative to a directory file descriptor

genhomedircon (8) - generate SELinux file context configuration entries for user home directories

getcwd (2) - get current working directory

get_current_dir_name (3) - get current working directory

getcwd (3) - get current working directory

getcwd (3p) - get the pathname of the current working directory

getdents (2) - get directory entries

getdents64 (2) - get directory entries

getdirentries (3) - get directory entries in a file system-independent format

getwd (3) - get current working directory

getwd (3p) - get the current working directory pathname (LEGACY)

git-clone (1) - Clone a repository into a new directory

git-mv (1) - Move or rename a file, a directory, or a symlink

git-stash (1) - Stash the changes in a dirty working directory away

gpgconf (1) - Modify .gnupg home directories

grub2-mknetdir (1) - Prepare a GRUB netboot directory.

install-info (1) - update info/dir entries

IO::Dir (3pm) - supply object methods for directory handles

linkat (2) - create a file link relative to directory file descriptors

lio_listio (3p) - list directed I/O (REALTIME)

llrint (3p) - round to the nearest integer value using current rounding direction

llrintf (3p) - round to the nearest integer value using current rounding direction

llrintl (3p) - round to the nearest integer value using current rounding direction

lookup_dcookie (2) - return a directory entry's path

lrint (3p) - round to nearest integer value using current rounding direction

lrintf (3p) - round to nearest integer value using current rounding direction

lrintl (3p) - round to nearest integer value using current rounding direction

ls (1) - list directory contents

ls (1p) - list directory contents

mkdir (1) - make directories

mkdir (1p) - make directories

mkdir (2) - create a directory

mkdir (3p) - make a directory

mkdirat (2) - create a directory relative to a directory file descriptor

mkdtemp (3) - create a unique temporary directory

mkfifoat (3) - make a FIFO (named pipe) relative to a directory file descriptor

mkhomedir_helper (8) - Helper binary that creates home directories

mklost+found (8) - create a lost+found directory on a mounted Linux second extended file system

mknod (3p) - make a directory, a special file, or a regular file

mknodat (2) - create a special or ordinary file relative to a directory file descriptor

mktemp (1) - create a temporary file or directory

modprobe.conf (5) - Configuration directory for modprobe

modprobe.d (5) - Configuration directory for modprobe

mountpoint (1) - see if a directory is a mountpoint

oldfind (1) - search for files in a directory hierarchy

openat (2) - open a file relative to a directory file descriptor

opendir (3) - open a directory

opendir (3p) - open a directory

pam_mkhomedir (8) - PAM module to create users home directory

Pod::Simple::Search (3pm) - find POD documents in directory trees

pwd (1) - print name of current/working directory

pwd (1p) - return working directory name

pwdx (1) - report current working directory of a process

readdir (2) - read directory entry

readdir (3) - read a directory

readdir (3p) - read a directory

readdir_r (3) - read a directory

readdir_r (3p) - read a directory

readlinkat (2) - read value of a symbolic link relative to a directory file descriptor

remove (3) - remove a file or directory

renameat (2) - rename a file relative to directory file descriptors

repomanage (1) - list the newest or oldest RPM packages in a directory

reposync (1) - synchronize yum repositories to a local directory

rewinddir (3) - reset directory stream

rewinddir (3p) - reset the position of a directory stream to the beginning of a directory

rm (1) - remove files or directories

rm (1p) - remove directory entries

rmdir (1) - remove empty directories

rmdir (1p) - remove directories

rmdir (2) - delete a directory

rmdir (3p) - remove a directory

scandir (3) - scan a directory for matching entries

scandirat (3) - scan a directory relative to a directory file descriptor

seekdir (3) - set the position of the next readdir() call in the directory stream.

seekdir (3p) - set the position of a directory stream

symlinkat (2) - create a symbolic link relative to a directory file descriptor

syscall (2) - indirect system call

systemd-socket-proxyd (8) - Bidirectionally proxy local sockets to another (possibly remote) socket.

systemd-system-update-generator (8) - Generator for redirecting boot to offline update mode

systemd-tmpfiles (8) - Creates, deletes and cleans up volatile and temporary files and directories

systemd-tmpfiles-clean.service (8) - Creates, deletes and cleans up volatile and temporary files and directories

systemd-tmpfiles-clean.timer (8) - Creates, deletes and cleans up volatile and temporary files and directories

systemd-tmpfiles-setup-dev.service (8) - Creates, deletes and cleans up volatile and temporary files and directories

systemd-tmpfiles-setup.service (8) - Creates, deletes and cleans up volatile and temporary files and directories

systemd.directives (7) - Index of configuration directives

tc-mirred (8) - mirror/redirect action

telldir (3) - return current location in directory stream

telldir (3p) - current location of a named directory stream

unlink (3p) - remove a directory entry

unlinkat (2) - remove a directory entry relative to a directory file descriptor

vdir (1) - list directory contents

versionsort (3) - scan a directory for matching entries





4.info - 리눅스 명령어 사용방법, 옵션 등을 나타냄





[vagrant@host1 test123]$ info pwd



19.1 'pwd': Print working directory


'pwd' prints the name of the current directory. Synopsis:



 pwd [OPTION]...



The program accepts the following options. Also see *note Common

options::.



'-L'

'--logical'

If the contents of the environment variable 'PWD' provide an

absolute name of the current directory with no '.' or '..'

components, but possibly with symbolic links, then output those

contents. Otherwise, fall back to default '-P' handling.



'-P'

'--physical'

Print a fully resolved name for the current directory. That is,

all components of the printed name will be actual directory

names--none will be symbolic links.



If '-L' and '-P' are both given, the last one takes precedence. If

neither option is given, then this implementation uses '-P' as the

default unless the 'POSIXLY_CORRECT' environment variable is set.

--zz-Info: (coreutils.info.gz)pwd invocation, 37 lines --Top-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------Welcome to Info version 5.1. Type h for help, m for menu item.





5.whatis - 명령어에 대한 기능을 간략하게 나타남





[vagrant@host1 test123]$ whatis pwd

pwd (1) - print name of current/working directory

pwd (1p) - return working directory name





6.alias - 리눅스에서 alias는 사용자가 명령어를 다른 이름으로 바꿔서 사용할 수 있는 쉘 내부 명령어






명령어 alias(별칭)확인



[vagrant@host1 test123]$ alias

alias egrep='egrep --color=auto'

alias fgrep='fgrep --color=auto'

alias grep='grep --color=auto'

alias l.='ls -d .* --color=auto'

alias ll='ls -l --color=auto'

alias ls='ls --color=auto'

alias which='alias | /usr/bin/which --tty-only --read-alias --show-dot --show-tilde'



[vagrant@host1 test123]$ alias flog='cd /log/myservice/info'

[vagrant@host1 test123]$ unalias flog







[vagrant@host1 test123]$ alias psa="ps aux"

[vagrant@host1 test123]$ psa

USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND

root         1  0.0  1.2 127988  6184 ?        Ss   01:32   0:01 /usr/lib/systemd/systemd --switched-root

root         2  0.0  0.0      0     0 ?        S    01:32   0:00 [kthreadd]

root         4  0.0  0.0      0     0 ?        S<   01:32   0:00 [kworker/0:0H]

root         5  0.0  0.0      0     0 ?        S    01:32   0:00 [kworker/u2:0]

root         6  0.0  0.0      0     0 ?        S    01:32   0:00 [ksoftirqd/0]

root         7  0.0  0.0      0     0 ?        S    01:32   0:00 [migration/0]

root         8  0.0  0.0      0     0 ?        S    01:32   0:00 [rcu_bh]

root         9  0.0  0.0      0     0 ?        R    01:32   0:00 [rcu_sched]

root        10  0.0  0.0      0     0 ?        S<   01:32   0:00 [lru-add-drain]

root        11  0.0  0.0      0     0 ?        S    01:32   0:00 [watchdog/0]

root        13  0.0  0.0      0     0 ?        S    01:32   0:00 [kdevtmpfs]

root        14  0.0  0.0      0     0 ?        S<   01:32   0:00 [netns]

root        15  0.0  0.0      0     0 ?        S    01:32   0:00 [khungtaskd]





--------------------------------------------------------------------------------------------------------------------------------------------

