# 프로세스 vs 쓰레드
프로세스는 운영체제로부터 자원을 할당받는 작업의 단위이고
스레드는 프로세스가 할당받은 자원을 이용하는 실행의 단위다.

- 스레드의 장점
    - 별도의 스택 영역을 가지고 Text Data Heap 영역을 공유한다.
    - 프로그램의 응답 시간이 단축되며 시스템의 자원 소모가 줄어든다.
    - 스레드간의 통신 방법이 프로세스 간 통신 방법에 비해 훨씬 간단하다.
- 스레드의 단점
    - 프로세스 밖에서 각각의 스레드를 제어할 수 없다.
    - 미묘한 시간차나 잘못된 변수를 스레드끼리 공유하게 되는 경우에는 오류가 발생할 수 있다.
    - 프로그램 디버깅이 상대적으로 어렵고 단일 프로세서(Single Processor) 시스템에서는 효과를 기대하기 어렵다.