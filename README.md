# top 명령어
***시스템의 프로세스/메모리 사용 상태를 5초의 간격으로 업데이트하여 출력***

* top[옵션]
* -b : 배치모드로 정보를 출력한다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력
* -d delay : 지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력
* -i idle : 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않음
* -n num : 지정한 시간(num)만큼 업데이트 정보를 출력
* -p pid : 지정한 프로세스 ID(pid)의 정보만을 출력
* -q : 시간의 간격 없이 계속하여 업데이트 정보를 출력
* -s : 몇 개의 대화식 명령을 비활성화(시큐어 모드)
* -S : 누적된 정보를 출력(cumulative 모드)

![image](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705212456131_V9D3Q4JJL.jpg/ka38_331_i1.jpg?type=w575_fst_n&wm=Y)

# ps 명령어
***현재 실행중인 프로세스 목록과 상태를 보여줌***

**전체 프로세스와 관련된 옵션**
* -A : 모든 프로세스를 출력
* -N : -A 옵션과 비슷하나 ps 프로세스를 제외하고 출력
* -a : 세션 리더 및 터미널에 속하지 않는 프로세스를 제외하고 출력
* -d : 세션 리더를 제외한 모든 프로세스를 출력
* -e : 커널 프로세스를 제외한 모든 프로세스를 출력
* T : 현재 터미널에서의 모든 프로세스를 출력
* a : 현재 터미널의 사용자 고유 프로세스를 출력
* r : 현재 실행 중인 프로세스를 출력
* x : 터미널이 없는 프로세스를 출력
* --deselect : -N 옵션과 같음음

**항목 & 내용**
* UID	프로세스를 실행한 사람 (User ID)
* PID	프로세스를 구분하기 위해 만들어진 프로세스 ID (Process ID)
* PPID	부모 프로세스 ID (Parent Process ID)
* C	스케쥴링을 위한 CPU 사용량
* STIME	프로세스 시작 시간
* TTY	장치 번호, 해당 프로세스의 입출력 담당 터미널
* TIME	CPU 점유 시간
* CMD	command

# jobs 명령어
***작업의 상태를 표시하는 명령어***
* 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력/ 각 작업에는 번호가 붙어있어 kilㅣ 명령어 뒤에 '%번호' 등으로 사용
* jobs[옵션][작업번호]

**jobs로 출력되는 백그라운드 작업의 상태값**
* Runnig :작업이 계속 진행중임
* Done : 작업이 완료되어 0을 반환
* Done(code) : 작업이 종료되었으며 0이 아닌 코드를 반환
* Stopped : 작업이 일시 중단
* Stopped(SIGTSTP) : SIGTSTP 시그널이 작업을 일시중단
* Stopped(SIGSTOP) : SIGSTOP 시그널이 작업을 일시중단
* Stopped(SIGTTIN) : SIGTTIN 시그널이 작업을 일시중단
* Stopped(SIGTTOU) : SIGTTOU 시그널이 작업을 일시중단

**옵션**
* -l : 프로세스 그룹 ID를 state 필드 앞에 출력
* -n : 프로세스 그룹 중에 대표 프로세스 ID를 출력
* -p : 각 프로세스 ID에 대해 한 행씩 출력
* command : 지정한 명령어를 실행

# kill 명령어

***프로세스에 시그널을 보내는 명령(죽일때 사용)***

**1. kill 시그널 리스트 확인**
* kill -l 
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99E84B455C6378A109)

**2. 주요 시그널**

시그널| 영어| 설명
--|--|--
 1)SIGHUP |	Hang Up|	세션이 종료될 때 시스템이 내리는 시그널
 2)SIGINT |	Interrupt|	Ctrl + C, 종료 요청 시그널
 9)SIGKILL	|Kill	|강제 종료 시그널
 11)SIGSEGV |	Segment Violation|	메모리 침범이 일어날 때 시스템이 보내는 시그널
 15)SIGTERM |	Terminate|	기본 값, 종료 요청 시그널
 20)SIGTSTP |	Temporary Stop|	Ctrl + Z 일시 중지 요청 시그널



