
### PCB(Process Control Block)
---
- 프로세스 제어 블록.
- 메모리의 별도 공간 (커널 스택의 가장 앞 부분에서 관리).
- 프로세스에 대한 메타데이터(프로세스 정보)를 저장하는 구조체.
- 프로세스 생성과 동시에 운영체제에 의해 생성.
<br>

#### PCB의 구조

<p align="center"><img src="https://github.com/user-attachments/assets/a1550265-4797-4be8-b00f-df8f1c5f4566"></p>

- **Pointer** : 프로세스의 현재 위치 저장하는 포인터 정보.
- **Process State** : 프로세스의 각 상태 정보.
- **Process Number(PID)** : 프로세스의 고유한 식별 ID.
- **Program Counter** : 프로세스가 실행할 다음 명령어의 주소를 저장.
- **Registers** : 프로세스를 실행하기 위해 저장해야 할 레지스터에 대한 정보.
- **Memory Limit** : 운영체제에서 사용하는 메모리 관리 시스템에 대한 정보(페이지 테이블, 세그먼트 테이블).
- **Accounting** : 프로세스 실행에 사용된 CPU 사용량, 실행한 유저에 대한 정보.
- **Open File Lists** : 프로세스를 위해 오픈된 파일 목록.
<br>

### 컨텍스트 스위칭(Context Switching)
---
- **OS의 커널(Kernel)** 에 의해서 실행되는 **프로세스 변경**.
> 커널 모드(Kernel Mode)에서 실행.
- **PCB(Process Control Block)** 에 Process 상태값들을 저장하고, 해당 값을 찾는 방식으로 구현.
<br>

#### 컨텍스트 스위칭 과정
- **요청발생** : 대표적으로 **시스템 콜이나 인터럽트가 호출**될 경우 기존 프로세스(A) 중단.
- **PCB에 프로세스 정보 저장** : 중단된 프로세스(A)와 관련된 정보를 **PCB**에 저장.
- **CPU 할당** : 새롭게 실행할 프로세스(B)를 CPU 레지스터에 적재 및 실행.
- **프로세스 종료 후 기존 프로세스 재실행** : 프로세스(B) 종류 후 기존 프로세스(A) 관련 정보(PCB)를 CPU 할당 후 적재.
<br>
