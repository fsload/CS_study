# 1주차 OS structure / Process 정리노트

우와 오에스 정말 재밌네요~~

## 운영체제:

사용자와 컴퓨터 하드웨어 사이에서 동작하는 시스템 소프트웨어

user view : 컴퓨터를 쉽고, 편하게 사용하게 하는 프로그램

system view : 자원의 제어와 할당을 위한 프로그램

## 목적:

사용자가 컴퓨터를 편리하게 사용할 수 있게함

하드웨어 자원들을 효율적으로 관리할 수 있게함

사용자가 프로그램 실행, 문제 해결을 용이하게 함

## 시스템 구성요소

![1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled.png](1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled.png)

## Common OS Structure

### Multiprogramming - CPU Utilization

단일 사용자가 항상 CPU와 I/O 디바이스를 Busy 상태로 유지할 수 없다. (효율적이지 못한 사용)

따라서 멀티 프로그래밍이 작업을 정리하여 CPU가 항상 실행 가능한 상태이도록 한다.

시스템 전체 작업중 일부를 메모리에 저장하고 스케줄링을 통해 작업을 수행한다. (멀티 프로그래밍 이후 스케줄링 도입)

I/O와 같은 대기가 필요한 경우, OS가 다른 작업으로 전환 한다.

![1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%201.png](1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%201.png)

### Timesharing(Multitasking) - 동기화가 필요함

작업의 전환을 매우 빠른 속도로 수행하여 사용자는 작업들이 동시에 수행되는 것처럼 보게된다.(multi task) → 대화형 컴퓨팅

Process : 사용자는 하나 이상의 프로그램을 메모리에서 실행한다.

CPU 스케줄링을 통해 여러 작업들을 동시에 수행

## 올바른 사용을 위한 OS의 보호 기능

Dual-Mode Operation : user mode와 kernel mode로 구분하여 각각 수행 가능한 영역에 대한 권한을 부여

I/O protection, Memory Protection, Timer

## OS가 제공하는 기능

사용자에게 유용한 기능 : UI, program execution, I/O operation, File system manipulation, communications, error detection

시스템의 효율적인 작동을 위한 기능 : resource allocation, accounting, protection and security

![1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%202.png](1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%202.png)

## 프로그램

Passive entity, 디스크에 저장된 instruction 들을 포함한 파일, 실행가능한 파일

## 프로세스

현재 실행 중인 프로그램, Active entity with program counter

프로그램이 메모리에 올라가면 프로세스가 된다. one program → multiple process

Job, Task와 유사하게 사용됨

Code(Text), Data, Stack, Heap 영역과 program counter를 가진다.

![1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%203.png](1%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20OS%20structure%20Process%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%82%E1%85%A9%E1%84%90%E1%85%B3%20e8afbd6e5c3a45a6be597745c9e634d2/Untitled%203.png)

프로세스의 상태는 new, ready, running, waiting, terminated로 구분되어진다.

## Zombie vs. Orphan Processes

좀비 프로세스 : 자식 프로세스가 종료되었지만 부모 프로세스가 이를 회수하지 않은 경우 (종료)

고아 프로세스 : 부모 프로세스가 자식보다 먼저 종료되는 경우, init 프로세스가 부모가된다. (실행중)