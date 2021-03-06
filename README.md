## 리눅스 명령어와 vim 에디터에서 매크로 사용방법에 대하여

***1. 리눅스 명령어 ps, top, jobs, kill***

!) ps : 현재 실행중인 프로세스를 보여주는 명령어 

|명령어|설명|
|:----|:---------------------------|
|R|Running 프로세스가 실행중이거나 실행 준비가 되었음을 의미|
|S|Slepping 프로세스가 실행되고 있지 않고 대기중|
|D|Uninterruptible Sleep 입출력 대기중|
|T|Stopped 프로세스 중지|
|Z|A defunct or "zombie"process 종료되었지만 상위 프로세스가 정리되지 않음|
|N|A low priority process 낮은 우선 순위를 가진 프로세스|

2) top : 시스템 프로세스/메모리 사용 현황을 실시간으로 출력

3) jobs : 작업이 중지된 상태나 백그라운드로 진행 중인 상태를 표시

4) kill : 프로세스에 종료 시그널을 보냄

***2. vim 에디터에서 매크로 사용방법***

_매크로 지정 방법_
1) vim의 중립모드에서 q를 누른 다음 매크로 이름으로 사용할 알파벳을 지정 
2) 밑에 **-- recording --** 이라고 뜰 때 메크로로 지정할 명령어 기록
3) 기록이 끝났으면 다시 중립모드에서 q를 입력

_매크로 재생 방법_
1) 중립모드에서 @(매크로 이름) (ex @a) 라고 누르면 매크로 재생
2) @@를 누르면 가장 마지막으로 재생한 매크로가 실행됨

_매크로를 파일로 저장하는 방법_
1) **~/.vimrc** 파일 열기
2) 예를들어 a라는 매크로를 저장할 시
3) (_insert 모드에서_) **let @a='Ctrl-R Ctrl-R a'** 입력시 저장됨
