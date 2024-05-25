# openswhomework
오픈소스 sw 과제 

# top 
- top 명령어는 리눅스 계열 서버의 OS 상태를 확인할 수 있는 ***CLI 어플리케이션***이다. 서버의 CPU 사용량, 메모리 사용량 등을 확인할 수 있으며, 서버에서 구동 중인 모든 어플리케이션들을 CPU 사용률이나 메모리 사용률이 많은 순서대로 나열하여 모니터링이 가능한 명령어이다.<br/>

![스크린샷 2024-05-25 170609](https://github.com/ehdgur123/openswhomework/assets/142292721/7435f3e1-9cfb-428f-b1ff-19138d50e81d)


- 리눅스 서버에 top 명령어를 입력하면 서버의 CPU 사용률이나 메모리 사용률들을 대표적으로 볼 수 있으며, CPU 사용이 많은 순서대로 프로세스 목록을 보여주고 있다. <br/>


# ps <br/>
- ps 명령어는 ***Process Status***의 약어로 ps 명령어를 사용하면 현재 구동 중인 프로세스 정보를 확인할 수 있다.<br/>

ps 명령어와 함께 사용되는 옵션<br/>
| 옵션 | 설명 |
|------|------|
| -e   | 현재 사용자뿐만 아니라 다른 사용자들이 구동시킨 모든 프로세스를 보여준다 |
| -f   | 보다 상세한 정보를 보여준다 |
| -l   | -f보다 더 상세한 정보를 보여준다. |





![스크린샷 2024-05-25 170820](https://github.com/ehdgur123/openswhomework/assets/142292721/8bb33c84-bf5e-4a2d-852a-b5138cef3721)


장점: 모든 프로세스 목록을 확인할 수 있고, 자세한 정보를 제공한다. <br/>
단점: 작업 목록을 확인하기 위해서는 옵션을 추가로 지정해야 하며, 백그라운드에서 실행 중인 프로세스를 확인하기 어렵다. <br/>

# jobs<br/>
- jobs 명령어는 작업의 상태를 표시하는 명령어이다. 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업에는 번호가 붙어 있어 kill 명령어 뒤에 '%번호' 등으로 사용할 수 있다.<br/>

jobs 명령어와 함께 사용되는 옵션<br/>
-p: 백그라운드에 있는 프로세스의 프로세스 아이디만 출력한다.<br/>
-l: 백그라운드에 있는 프로세스의 프로세스 아이디와 job 목록을 출력한다.<br/>
-s: 백그라운드에 있는 프로세스 중 멈춰있는 프로세스만 출력한다.<br/>
-r: 백그라운드에 있는 프로세스 중 실행중인 프로세스만 출력한다. <br/>

장점: 현재 쉘 세션에서 실행 중인 작업 목록을 간단하게 확인할 수 있다.<br/>
단점: 백그라운드에서 실행 중인 다른 쉘 세션의 작업 목록을 확인할 수 없으며, 자세한 정보를 제공하지 않는다.<br/>

- 필요에 따라서 ps 명령어와 jobs 명령어를 적절히 사용하여 현재 동작 중인 프로그램을 확인할 수 있다.<br/> 

# kill<br/>
- kill 명령어는 프로세스에 시그널을 보내어 원하는 동작을 수행할 수 있다. 프로세스 종료 외에도 다른 신호를 보내어 프로세스의 동작을 제어할 수 있다.<br/>
- kill 명령어를 사용하기 위해서는 종료하려는 프로세스 ID를 알아야 한다. 일반적으로 ps 명령어를 사용하여 현재 실행 중인 프로세스 목록을 확인한 후, 종료하려는 프로세스의 ***PID***를 찾아야 한다.<br/>

kill [옵션] <PID><br/>

kill 명령어의 옵션 <br/>
-s 특정 시그널을 사용하여 프로세스를 종료한다. 기본적으로 SIGTERM 시그널이 사용된다.<br/>
-l,--list: 지원되는 시그널 목록을 출력한다.<br/>
-a, --all: 현재 사용자에 속한 모든 프로세스를 종료한다.<br/>
-q, --queue: 프로세스에 시그널을 보내는 대신 시그널을 대기열에 추가한다.<br/>

장점<br/>
- 간단한 명령어로 빠르게 프로세스를 종료할 수 있다.<br/>
- 다양한 옵션을 사용하여 프로세스 동작을 제어할 수 있습니다.<br/>

단점<br/>
- 잘못 사용하면 의도치 않은 프로세스 종료가 발생할 수 있다.<br/>
- SIGKILL 시그널을 사용하여 강제 종료할 경우, 프로세스가 올바르게 정리되지 않을 수 있고, 데이터 손실 등의 문제가 발생할 수 있다.<br/>



