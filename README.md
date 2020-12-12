## Part 0: Getting Started
```
$ mkdir lib
$ cd lib
$ sudo curl https://soot-build.cs.uni-paderborn.de/public/origin/master/soot/soot-master/3.3.0/build/sootclasses-trunk-jar-with-dependencies.jar -o soot-3.3.0.jar
```
## Part 1: Control Flow Analysis - Finding Dominators

## Part 2: Data Flow Analysis - Call Graph Construction

Comparing Different Call Graph Construction Algorithms

points-to analysis (PTA) detect 7 edges.


class hierarchy analysis (CHA) detect 12 edges.

## Part 3: Program Instrumentation with Soot
One run
```
Thread main wrote static field <HelloThread: int x>
Thread main read instance field <HelloThread$TestThread: int y> of object Thread[main,5,main]
Thread main read static field <HelloThread: int x>
Thread Thread-0 wrote static field <HelloThread: int x>
Thread main read static field <java.lang.System: java.io.PrintStream out>
Thread Thread-0 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-0,5,main]
1
Thread Thread-0 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-0,5,main]
```

another run Output 



```
Thread main wrote static field <HelloThread: int x>
Thread main read instance field <HelloThread$TestThread: int y> of object Thread[main,5,main]
Thread Thread-0 wrote static field <HelloThread: int x>
Thread main read static field <HelloThread: int x>
Thread Thread-0 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-0,5,main]
Thread Thread-0 read instance field <HelloThread$TestThread: int y> of object Thread[Thread-0,5,main]
Exception in thread "main" java.lang.ArithmeticException: / by zero
	at HelloThread.main(HelloThread.java)


```
