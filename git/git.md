GIT을 사용하다가 헷갈릴 때는
https://backlog.com/git-tutorial/kr/ 로 가면 된다.(22.05.20 도움이 잘 되는지 모르겠음)

rebase에 대해서 아직 잘 모르겠다.

```git clone -b {branch_name} --single-branch {저장소 URL}```  
= ```git init + git remote add origin {URL} + git pull origin {branch이름}```  
이지만 아랫줄은 해당 브랜치를 가져오는건 아니고 그냥 그 브랜치 안에 있는 파일들만 복사해서 가져오는 것.

```git pull``` = ```git fetch``` followed by ```git merge```  
```git fetch```는 git에서 관리하는 버전 관리 정보만 업데이트하기 때문에 작업중인 파일은 건드리지 않음.  
```git merge```를 하면 그때서야 ```fetch```를 통해 가져왔던 업데이트 정보를 반영하면서 합병함.
