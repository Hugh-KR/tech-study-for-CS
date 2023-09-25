## 자바 가상 머신(Java Virtual Machine)

자바 프로그램 실행환경을 만들어주는 소프트웨어 입니다. 자바 코드를 컴파일 하여 .class 바이트 코드로 만들면 이 코드가 JVM 환경에서 실행됩니다. JVM은 자바 실행환경 JRE(Java Runtime Environment) 에 포함되어 있습니다. 현재 사용하는 컴퓨터의 운영체제에 맞는 자바 실행환경(JRE)가 설치되어 있다면 자바 가상 머신이 설치되어 있다는 뜻입니다.

![JVM_img_01.png](../Img/JVM_img_01.png)

**이들은 모두 JDK 에 포함 되는데 자세한 정보는 아래 링크 확인 부탁드립니다.**  
[[[[Java] JDK JRE JVM 구성 원리]]]()  

JVM의 목적은 크게 두 가지로 말할 수 있습니다.
1. 자바 프로그램이 어느 기기나 운영체제 상에서도 실행될 수 있도록 하는 것
2. 프로그램 메모리를 관리하고 최적화 하는 것

![](../Img/JVM_img_02.png)

C언어로 작성된 Test.c가 있다고 가정했을때, 윈도우 컴파일러를 사용해서 컴파일하면 Test.exe가 만들어집니다. 윈도우 컴파일러로 컴파일되었기에 Test.exe는 윈도우에서만 실행되는 실행 파일 입니다. 리눅스 운영체제 에서는 실행할 수 없습니다. 즉 C / C++에서는 컴파일 플랫폼과 타겟 플랫폼이 다를 경우 프로그램이 동작하지 않습니다. 만약 Test.exe 파일을 리눅스 운영체제에서 실행하려면 리눅스 환경을 타겟으로 크로스 컴파일 해서 리눅스 운영체제에 맞는 실행 파일을 새로 만들어야 한다는 것 입니다.

그러나 Java의 경우 Test.java를 컴파일 하면 Test.class 파일이 생성됩니다. 그리고 이렇게 생성된 바이트 코드틑 각자의 플랫폼에 설치되어 있는 JVM이 운영체제에 맞는 실행 파일로 바꿔줍니다. 즉 Java에서는 하나의 바이트 코드로 JVM이 설치된 모든 플랫폼에서 동작이 가능하다는 이야기 입니다.

## JVM 동작 방식
![](../Img/JVM_img_03.png)
```
1. 자바로 개발된 프로그램을 실행하면 JVM은 OS로 부터 메모리를 할당 받는다.  
2. 자바 컴파일러(Javac)가 자바 소스코드(.java)를 바이트코드(.class)로 컴파일 한다. 
3. 클래스 로더를 통해 JVM Runtime Data Area로 로딩한다.
4. Runtime Data Area로 로딩된 .class들은 Execution Engine을 통해 해석한다.
5. 해석된 바이트 코드는 Runtime Data Area의 각 영역에 배치되어 수행하며 이 과정에서 Execution Engine에 의해 GC의 작동과 스레드 동기화가 이루어진다.
```

다음 포스팅에서는 JVM의 구조에 대해 조금 더 자세히 알아보겠습니다.  
[[Java] JVM의 구조](https://github.com/devFancy/2023-CS-Study/blob/main/java/java_jvm_architecture.md)

[[Java] JVM의 구조]([Java]%20JVM의%20구조.md)

---

### Reference

[[Java] 자바 가상머신 JVM(Java Virtual Machine) 총정리](https://coding-factory.tistory.com/827)  
[자바 가상 머신(Java Virtual Machine)](https://github.com/gyoogle/tech-interview-for-developer/blob/master/Language/%5Bjava%5D%20%EC%9E%90%EB%B0%94%20%EA%B0%80%EC%83%81%20%EB%A8%B8%EC%8B%A0(Java%20Virtual%20Machine).md#%EC%9E%90%EB%B0%94-%EA%B0%80%EC%83%81-%EB%A8%B8%EC%8B%A0java-virtual-machine)  
[# JDK / JRE / JVM 개념 & 구성 원리 💯 총정리](https://inpa.tistory.com/entry/JAVA-%E2%98%95-JDK-JRE-JVM-%EA%B0%9C%EB%85%90-%EA%B5%AC%EC%84%B1-%EC%9B%90%EB%A6%AC-%F0%9F%92%AF-%EC%99%84%EB%B2%BD-%EC%B4%9D%EC%A0%95%EB%A6%AC)  
[JVM 메모리 구조](https://github.com/devFancy/2023-CS-Study/blob/main/java/java_jvm_architecture.md)