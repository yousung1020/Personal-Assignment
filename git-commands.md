# Git 명령어 정리

## 1. add

* Git 에서 add 커맨드는 워킹 디렉토리(Working Directory) 상의 변경 내용을 스테이징 영역에 추가하는 명령어입니다.

```git
$ git add [디렉토리 or 파일 이름]
```
> add 사용법

* 먼저 echo 메세지를 리다이렉션하여 hi.py에 적용시켰습니다.  
![image](https://user-images.githubusercontent.com/65354879/204133470-a1920135-186b-46e6-8669-3d98d396ecd0.png)

* 이를 add 한 후 status 명령어를 통해 파일이 트랙(추적)된 상태임을 알 수 있습니다.

![image](https://user-images.githubusercontent.com/65354879/204133648-73f2c233-fea1-4054-8fd6-5ab4ce484ac2.png)





## 2. commit

* Git에서 커밋은 의미 있는 변경 작업들을 저장소에 기록하는 명령어입니다.

```git
$ git commit -m "commit message"
```
> commit 사용법

* add 파트에서 add한 파일을 commit 하고 status 명령어를 통해 상태를 확인하여 봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134214-55352374-14b3-41b4-8ad7-359327fcd4fe.png)

* 정상적으로 커밋이 된 것을 확인할 수 있습니다.

## 3. log

* Git에서 log는 커밋된 내역을 확인하는 명령어입니다.

```git
$ git log [options]
```
> log 사용법

* 위에서 커밋한 내역을 출력하여 봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134372-aa930758-8919-4892-9d72-b1766b8e107d.png)

* 커밋이 정상적으로 되었음을 한 번더 알 수 있고, 커밋 메시지와 해시 값까지 알 수 있습니다.


## 4. show

* Git에서 show는 태그나 커밋 정보를 보고 싶을 때 사용하는 명령어입니다.

```git
$ git show [options]
```
> show 사용법

* 위에서 커밋한 내역을 자세히 알아봅시다.

![image](https://user-images.githubusercontent.com/65354879/204134658-501243a8-ce1d-4302-aeb7-94732da7ae9f.png)

* 기존 0줄(없음)에서 1줄(생김)이 추가된 것을 확인할 수 있습니다.

## 5. clone 

* Git에서 clone은 원격 저장소에 있는 레포지토리의 파일를 복제하는 명령어입니다.

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

* Git에서 push는 로컬 저장소에 커밋된 파일을 원격 저장소로 등록하는 명령어입니다.

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

* Git에서 pull은 원격 저장소에 있던 수정 내역을 로컬 저장소로 불러오는 명령어입니다.

```git
$ git pull [원격 저장소 별칭] [불러들일 브랜치 이름]
```
> pull 사용법

* 원격 저장소에서 파일을 하나 만들고 그것을 pull 하여 보겠습니다.

![image](https://user-images.githubusercontent.com/65354879/204137722-a4281dc8-d876-4f1d-86e9-bab588c58232.png)

* 원격 저장소에서 bye.py 파일을 생성하였습니다. 이것을 pull 한 후 로컬 저장소에 잘 반영되었는지 확인하겠습니다.

![image](https://user-images.githubusercontent.com/65354879/204137767-b418304b-e883-4980-8313-9d0265a0ea88.png)

![image](https://user-images.githubusercontent.com/65354879/204137795-b6a0874f-d648-4089-83c7-31eab3f4c30e.png)

* bye.py 가 로컬 저장소에 잘 반영된 것을 확인할 수 있습니다.


## 8. fetch

* Git에서 fetch는 원격 저장소에서 코드를 수동으로 내려받는 작업을 하는 명령어입니다. pull과 달리 fetch는 내려받은 후 현재 브랜치와 자동 병합하지 않습니다.

```git
$ git fetch [원격 저장소 url] [불러들일 브랜치 이름]
```
> fetch 사용법

* 원격 저장소에서 파일을 하나 더 만들고 fetch 하겠습니다.

![image](https://user-images.githubusercontent.com/65354879/204139140-acd80680-a997-4516-9f8e-b65918cb72db.png)

* fetch.py 파일을 생성하였습니다. 이를 fetch 하고 log를 해보겠습니다.

<img src=https://user-images.githubusercontent.com/65354879/204139253-6ece388a-9151-461a-a900-b9cc7790b87b.png height=500 weight=500>

* pull과 달리 fetch는 자동으로 브랜치 병합을 하지 않아 커밋된 이력이 남지 않는 것을 확인할 수 있습니다. 이는 merge를 통해 수동 병합할 수 있습니다.

## 9. branch

* Git에서 branch는 독립적으로 어떤 작업을 진행하기 위한 개념입니다. 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있습니다.

```git
$ git checkout [options] [브랜치 이름]
$ git branch [options] [브랜치 이름]
$ git switch [options] [브랜치 이름]
...etc
```

* Git에서 브랜치에 관련한 명령어는 매우 많습니다. checkout, branch, switch 정도가 있습니다.

## 10. merge

* Git에서 merge는 브랜치에 대해 병합을 하는 명령어입니다. Fast-Forward 병합과 3-way 병합 알고리즘이 있습니다.

```git
$ git merge [options] [브랜치 이름]
```
> merge 사용 방법

* 아까 전 fetch 하였던 파일 내역을 merge를 통해 커밋 이력에 추가해봅시다.

<img src=https://user-images.githubusercontent.com/65354879/204139977-5a235f78-6906-47cd-98b0-56194c2665ea.png weight=500 height=500>

* merge를 한 후 log를 통해 확인해본 결과 커밋 이력에 fetch.py가 생겼음을 확인할 수 있습니다.
## 11. rebase


## 12. reset
