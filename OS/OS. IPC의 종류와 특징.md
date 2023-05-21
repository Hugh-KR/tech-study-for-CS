## IPC의 종류와 특징
**IPC(Inter Process Communication)**  
프로세스는 독립적으로 실행된다. 이런 독립적 구조를 가진 프로세스 간의 통신을 해야하는 상황이 있을 것이다. 이를 가능하도록 해주는 것이 IPC 통신이다.  
프로세스는 커널이 제공하는 IPC 설비를 이용해 프로세스간 통신을 할 수 있다.

**커널(Kernel)**: `운영체제의 핵심적인 부분, 다른 모든 부분에 시스템 내부적인 서비스를 제공해준다.`  
[OS. 커널 구조와 유형](OS.%20커널%20구조와%20유형.md)  

IPC 설비의 종류는 다양하고 필요에 따라 선택해서 사용해야 한다.

<br>

### IPC 종류


#### ↳익명 PIPE

#### ↳Named PIPE(FIFO)

#### ↳Message Queue

#### ↳공유 메모리

#### ↳메모리 맵

#### ↳소켓


---

### Reference

[IPC(Inter Process Communication)](https://github.com/gyoogle/tech-interview-for-developer/blob/master/Computer%20Science/Operating%20System/IPC(Inter%20Process%20Communication).md)  
