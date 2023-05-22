# assignment_20233068
assignment_20233068

# top 명령어
*나 _ *나 _ *나 _시스템의 프로세스/메모리 사용 상태를 5초의 간격으로 업데이트하여 출력

* -b : 배치모드로 정보를 출력한다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력한다.
* -d delay : 지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력한다.
* -i idle : 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않는다.
* -n num : 지정한 시간(num)만큼 업데이트 정보를 출력한다.
* -p pid : 지정한 프로세스 ID(pid)의 정보만을 출력한다.
* -q : 시간의 간격 없이 계속하여 업데이트 정보를 출력한다.
* -s : 몇 개의 대화식 명령을 비활성화한다(시큐어 모드).
* -S : 누적된 정보를 출력한다(cumulative 모드).

![image](https://dbscthumb-phinf.pstatic.net/4938_000_1/20170705212456131_V9D3Q4JJL.jpg/ka38_331_i1.jpg?type=w575_fst_n&wm=Y)

# ps 명령어
*나 _ 현재 실행중인 프로세스 목록과 상태를 보여준다.

* -e : 모든 프로세스를 출력
* -f :풀 포맷으로 출력 (uid, pid, ppid, TTY 등 정보를 보여줌)
* -l : 긴 포맷으로 출력 (풀 포맷+F,S,PRI등 정보를 더 보여줌)
* -p 1 : 프로세스 번호가 1인 프로세스를 출력
* -u seek : 계정이 seek인 프로세스들을 출력
* -ef | more : 모든 프로세스를 풀 포맷으로 출력, more 명령어를 이용하여 페이지 단위로 출력
* -ef | grep seek : 모든 프로세스를 풀 포맷으로 출력한 목록에서 grep을 이용해 seek이 포함된 행(ROW)을 출력

# jobs 명령어
*나 _ 작업의 상태를 표시하는 명령어'

-jobs로 출력되는 백그라운드 작업의 상태값
* Runnig :작업이 계속 진행중임
* Done : 작업이 완료되어 0을 반환
* Done(code) : 작업이 종료되었으며 0이 아닌 코드를 반환
* Stopped : 작업이 일시 중단
* Stopped(SIGTSTP) : SIGTSTP 시그널이 작업을 일시중단
* Stopped(SIGSTOP) : SIGSTOP 시그널이 작업을 일시중단
* Stopped(SIGTTIN) : SIGTTIN 시그널이 작업을 일시중단
* Stopped(SIGTTOU) : SIGTTOU 시그널이 작업을 일시중단

-옵션
* -l : 프로세스 그룹 ID를 state 필드 앞에 출력
* -n : 프로세스 그룹 중에 대표 프로세스 ID를 출력
* -p : 각 프로세스 ID에 대해 한 행씩 출력
* command : 지정한 명령어를 실행

# kill 명령어

*나_ 프로세스에 시그널을 보내는 명령이다.(죽일때 사용)

1. kill 시그널 리스트 확인
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99E84B455C6378A109)

2. 주요 시그널


