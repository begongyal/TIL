우분투에서 sudo 권한 주는법
: sudo su 명령어로 root 계정으로 전환
: visudo /etc/sudoers 명령어로 sudoers 파일을 visudo 편집기로 연다.
: User privilege specification 아래에
계정이름 ALL=(ALL:ALL) ALL
을 입력하고 Ctrl+O, Enter, Ctrl+X로 저장하고 나온다.

특정 디렉토리 권한 주는법
adduser로 처음에 사용자 계정을 만들면
사용자 아이디가 생성되면서 사용자 아이디랑 같은 이름의 그룹이 생기고
그 아이디가 그룹에 속해진다.

groupadd 그룹이름
명령어로 그룹을 일단 만들어주고

usermod -aG 그룹이름 사용자아이디
gpasswd -a 사용자아이디 그룹이름
명령어로 그룹에 사용자를 추가한다.

chown (-R: recursive) 소유자:그룹 폴더or파일이름
명령어로 폴더or파일의 소유자와 그룹을 변경할수있다

groups 사용자아이디
명령어는 사용자가 포함된 그룹들을 모두 보여준다.

groups 명령어만 쳐도 접속된 아이디의 group들을 보여준게 맞는데, 방금 새로 추가한 그룹은 안보이게 된다. 왜냐하면 파일의 소유권이 chown을 통해서 변경되었을때 바로바로 permission이 변경되는것과는 달리 group은 아예 로그아웃을 했다가 다시 들어온다거나(터미널 껐다켜는걸로는안됨) 해야 실제 권한이 변경되기 때문이다.
참고:https://askubuntu.com/questions/455000/group-permissions-allow-but-still-get-permission-denied

그래서 su 사용자아이디
명령어를 입력해주고나면

groups 명령어가 정상적으로 새로 추가한 그룹도 보여준다. 그리고 그 그룹이 가지고있는 모든 권한도 획득한다.
