# 싸다 면접
###
1. 희찬이는 모래시계를 좋아한다. 다음 물음에 답하여라. 
   > 자유롭게 모래시계를 구현하여라. 그래픽으로 해도 좋고, 일정 시간이 지나면 알림이 뜨는 프로그램 등을 만들어도 좋고, 뒤 문제를 풀 때 만든 코드의 일부분을 적당히 가져와도 좋다. 
   
   > 모래시계의 시간 2개와 목표 시간이 입력되면 목표에 도달하는 방법을 출력하는 프로그램을 작성하여라. 여러 개의 방법이 있어도 아무거나 하나만 출력하면 된다.  
   >
   > 입력 예시
   > ```agsl
   > 7 9 11
   > ```
   > 출력 예시
   > ```agsl
   > (7, 0) (9, 0)
   > (0, 7) (2, 7)
   > (7, 0) (2, 7)
   > (5, 2) (0, 9)
   > (2, 5) (0, 9)
   > (0, 7) (0, 9)
   > ```
   > 꼭 이 형식에 맞출 필요는 없다. 
###
2. 이 프로젝트 안에는 Calculator 오브젝트 파일이 있다. 이것은 코틀린(Kotlin)으로 이루어진 파일이다. 
   > 미리 만들어둔 Calculator 오브젝트를 이용하여 간단한 사칙연산이 되는 프로그램을 작성하여라. 

   > 이 오브젝트 파일에서```return this```는 무엇을 의미하고 왜 있는 것일까?
###
3. 당신의 친구가 노트북의 잠금을 풀어둔 상태에서 자리를 비웠다. 당신이 가장 먼저 할 행동은?
###  
###  
###  
## 코틀린 문법
1. 입력, 출력
   ```kotlin
   println(readLine())  // 마지막에 개행 있음
   print(readLine())    // 마지막에 개행 없음
   ```
   코틀린은 세미콜론(;)이 필요 없고, 함수, 변수, 클래스의 이름을 짓는 방법이 정해져 있다.  
   함수, 변수의 경우 단어로 모두 쪼개고 첫 번째 단어를 제외하고 모든 단어의 첫 글자를 대문자로 쓴다. 
   클래스(자료형)의 경우 모든 단어의 첫 글자를 대문자로 쓴다. 
####

2. 조건문
   ```kotlin
   if (Boolean){
       //
   } else if (Boolean){
       //
   } else{
       //
   }
   ```
####

3. 반복문
   ```kotlin
   while (Boolean) {
       //
   }
   for (i in 1..10)         // i = 1, 2, 3, ..., 10
   for (i in 1 until 10)    // i = 1, 2, 3, ..., 9
   for (i in List)          // i = List 내부 항목들이 모두 들어가게 됨
   ```
####

4. 변수
   ```kotlin
   val value:Double=3.14
   var variable:Int=123
   // Type은 생략해도 된다. 
   val myValue=10   // value의 형식은 Int로 정해진다. 
   
   variable = 1234  // 가능
   value = 3.141592 // 불가능
   ```
####

5. nullable  
   Type에 ?를 붙이면 nullable 변수가 된다. 
   ```kotlin
   val myVal = readLine().toInt()
   var myVar:String? = when (myVal){
       1 -> "val is 1"
       else -> null
   }
   ```
   null은 다른 자료형에 전혀 포함되지 않고 완전히 독립적으로 작동한다.   
   nullable 변수에 !!를 붙이면 null이 들어가 있지 않는다는 의미이다. 이것을 검사해야 작동하는 상황이 있다. 
####

6. 함수
   ```kotlin
   fun myFunc(a:Int, b:Int):Int{
       return a+b
   }
   ```
####

7. class
   ```kotlin
   class MyClass(val string:String, var integer:Int){
       //
   }
   ```
   클래스를 이용하여 ```MyClass("19기가 저희 동아리의 희망입니다", 1234)```로 겍체 생성 가능  
   ```val```로 선언된 변수는 변경이 불가능하고 외부에서 접근만 할 수 있다.  
   ```var```로 선언된 변수는 변경이 가능하고 외부에서 접근, 수정할 수 있다. 
####

8. static class  
   자바에서 static class는 그 클래스로 객체를 만들지 않는다. 그리고 그 클래스의 이름으로 함수들을 호출할 수 있다. 하지만 코틀린에서는 간단하게 object를 통하여 static class를 대신할 수 있다.
####

9. String 자료형  
   ```String.split()```으로 특정 문자 기준 나누기 가능하고 이 결과물은 ```List<String>``` 타입이다. 
####

10. List 자료형  
   붙이기, 자르기, 추가하기 등이 쉬운 자료형이다. 자세한 내부 함수들은 구글 검색
####