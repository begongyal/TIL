GIT을 사용하다가 헷갈릴 때는
https://backlog.com/git-tutorial/kr/ 로 가면 된다.(22.05.20 도움이 잘 되는지 모르겠음)

rebase에 대해서 아직 잘 모르겠다.
<br/>
<br/>
---
<br/>
<br/>

```git clone -b {branch_name} --single-branch {저장소 URL}```  
= ```git init + git remote add origin {URL} + git pull origin {branch이름}```  
이지만 아랫줄은 해당 브랜치를 가져오는건 아니고 그냥 그 브랜치 안에 있는 파일들만 복사해서 가져오는 것.

```git clone {URL}```
으로만 해도 일단 origin을 {URL}로 설정함.

```git remote -v```
를 하면 원격 저장소를 볼 수 있음

<br/>
<br/>

```git branch```
하면 현재 branch들의 리스트를 보여줌.

```git branch {branch_name}```
하면 branch_name을 이름으로 하는 branch를 만듦.

```git checkout {branch_name}```
하면 branch_name으로 전환함.

```git branch -b {branch_name}```
하면 branch_name을 이름으로 하는 branch를 만들면서 전환함.

<br/>
<br/>

```git add {filename}```
을 통해서 파일들을 tracked되게 만들고,
```git status```
를 통해 상태를 확인할 수 있다.
```git commit -m {commit message}```
를 통해서 tracked된 파일들을 로컬 저장소에 commit할 수 있고, 이제부터
```git push origin {로컬저장소의 branch_name}```
을 통해서 로컬 저장소에서 원격 저장소로 옮길 수 있다.

<br/>
<br/>

```git pull``` = ```git fetch``` followed by ```git merge```  
```git fetch```는 git에서 관리하는 버전 관리 정보만 업데이트하기 때문에 작업중인 파일은 건드리지 않음.  
```git merge```를 하면 그때서야 ```fetch```를 통해 가져왔던 업데이트 정보를 반영하면서 합병함.

<br/>
<br/>

```git push origin {로컬 저장소의 branch 이름}```을 하면 origin에 해당 branch이름과 같은 branch가 있는지 없는지 보고,  
있으면 그 branch에 push를 하고, 없으면 branch를 새로 만들어서 업데이트한다.

그래서 꼭 git clone으로 모든 파일을 tracking 하고 있는 그 정보들을 가져와야되는건 아니고(물론 이러면 branch를 통째로 가져오기 때문에 편하긴 하지만)  
pull 로 가져오든, 아니면 그냥 복사 붙여넣기를 하든지 하고 로컬에서 작업하고 있는 branch 이름만 원격 저장소랑 똑같이 맞춰주면 git push 가 됨.

<br/>
<br/>

원격 저장소에 있는 A라는 branch, B라는 branch를 둘다 Main이라는 branch에 merge하고 싶으면,  
Main이라는 branch를 일단 내 로컬 저장소로 가져오고, A와 B도 로컬 저장소로 가져온다.  
그다음에 로컬 저장소에서 A와 B를 Main에 합병하고 나서, 합병된 Main을 원격저장소에 push 하는 방식으로 하게됨.
