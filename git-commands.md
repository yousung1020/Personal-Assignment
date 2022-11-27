# Git 명령어 정리

## 1. add

* Git 에서 add 커맨드는 워킹 디렉토리(Working Directory) 상의 변경 내용을 스테이징 영역에 추가하는 명령어 입니다.

```git
$ git add [디렉토리 or 파일 이름]
```
> add 사용법

* 먼저 echo 메세지를 리다이렉션하여 hi.py에 적용시켰습니다.  
![image](https://user-images.githubusercontent.com/65354879/204133470-a1920135-186b-46e6-8669-3d98d396ecd0.png)

* 이를 add 한 후 status 명령어를 통해 파일이 트랙(추적)된 상태임을 알 수 있습니다.

![image](https://user-images.githubusercontent.com/65354879/204133648-73f2c233-fea1-4054-8fd6-5ab4ce484ac2.png)





## 2. commit

* Git에서 커밋은 의미 있는 변경 작업들을 저장소에 기록하는 명령어 입니다.

```git
$ git commit -m "commit message"
```
> commit 사용법

* add 파트에서 add한 파일을 commit 하고 status 명령어를 통해 상태를 확인하여 봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134214-55352374-14b3-41b4-8ad7-359327fcd4fe.png)

* 정상적으로 커밋이 된 것을 확인할 수 있습니다.

## 3. log

* Git에서 log는 커밋된 내역을 확인하는 명령어 입니다.

```git
$ git log [options]
```
> log 사용법

* 위에서 커밋한 내역을 출력하여 봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134372-aa930758-8919-4892-9d72-b1766b8e107d.png)

* 커밋이 정상적으로 되었음을 한 번더 알 수 있고, 커밋 메시지와 해시 값까지 알 수 있습니다.


## 4. show

* Git에서 show는 태그나 커밋 정보를 보고 싶을 때 사용하는 명령어 입니다.

```git
$ git show [options]
```
> show 사용법

* 위에서 커밋한 내역을 자세히 알아봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134658-501243a8-ce1d-4302-aeb7-94732da7ae9f.png)

* 기존 0줄(없음)에서 1줄(생김)이 추가된 것을 확인할 수 있습니다.

## 5. clone 

* Git에서 clone은 원격 저장소에 있는 레포지토리의 파일를 복제하는 명령어 입니다.

```git
$ git clone [url]
```
> clone 사용법

* 저의 python 레포지토리를 클론하여 보겠습니다.

<img src=https://user-images.githubusercontent.com/65354879/204135900-70520ade-171a-459f-82d4-4889e0205a77.png weight=400 height=400>

* 다음 명령어를 실행한 후 로컬 저장소에 잘 반영되었는지 확인하겠습니다.

![image](https://user-images.githubusercontent.com/65354879/204136024-84534843-1cb7-498a-aeea-a6c4e0f5eba3.png)

![image](https://user-images.githubusercontent.com/65354879/204136084-abf64ec4-1573-43e7-a5d2-2e4c810aaab0.png)

* 로컬 저장소에 잘 반영된 것을 확인할 수 있습니다.

## 6. push

* Git에서 push는 로컬 저장소에 커밋된 파일을 원격 저장소로 등록하는 명령어 입니다.

```git
$ git remote add [원격 저장소 별칭] [등록 할 레포지토리 url]
$ git push [원격 저장소 별칭] [등록 할 브랜치 이름]
```
> remote 및 push 사용법

* 아까 커밋하였던 hi.py를 제 github 레포지토리에 업로드 하겠습니다.

* 먼저 원격 저장소를 등록합시다.

![image](https://user-images.githubusercontent.com/65354879/204136472-c7693af3-eab7-4b64-8ff0-c0ff9f60752e.png)

* 그 후 push를 통해 업로드하고 원격 저장소에 잘 반영되었는지 확인해보겠습니다.

![image](https://user-images.githubusercontent.com/65354879/204136899-0b4d5925-1da4-412b-9a57-48e67c339583.png)

![image](https://user-images.githubusercontent.com/65354879/204137079-fa3d2cb0-c5b7-4021-afb4-3ea5929915c8.png)

* 기존에 있던 Readme 파일을 제외하면, hi.py가 잘 등록된 것을 확인할 수 있습니다.

## 7. pull

## 8. fetch

## 9. branch

## 10. merge

## 11. rebase

## 12. reset
