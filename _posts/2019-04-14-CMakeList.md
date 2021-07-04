# CMakeLists.txt 간단 작성법
-----
## 간단한 테스트 환경
~~~
mkdir test
cd test
cat main.cpp
~~~

### main.cpp
~~~
  1 #include <iostream>
  2
  3 int main()
  4 {
  5     std::cout << "hello" << std::endl;
  6     return 0;
  7 }
~~~

### 샘플코드 g++ 이용 빌드
~~~
g++ -o main main.cpp
~~~

### CMakeLists.txt 작성
~~~
 PROJECT(main)
 ADD_EXECUTABLE(main main.cpp)
~~~

### build 스크립트 작성
1. 보통 소스 외의 부분에 디렉토리를 만들어준다
2. cmake 명령 입력 시, 해당 경로에서 makefile 관련 파일들이 생성되어 소스코드와 섞일 수 있다
3. 따라서 새로운 디렉토리에서 cmake와 make를 수행하도록 작성한다.

### build.sh 작성 예
~~~
1. #!/bin/bash
2. mkdir build
3. cd build
4. cmake .
5. make
~~~
