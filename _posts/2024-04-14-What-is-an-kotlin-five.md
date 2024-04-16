# Functions

#### Functions

- fun name(parameters): return Type { body }
- 각 파라미터는 default 값을 가질 수 있으며
- 함수를 호출할 때 파라미터 이름을 명시하면 선언 순서와 상관없이 전달할 수 있다

```kotlin
fun message(name:String, message:String="Hello", age:Int):String {
    return "Age:$age, $message, $name"
}

fun main() {
    println(message(age=22, name"User"))
}
```

- overriding 된 함수는 base 함수의 default 값을 동일하게 사용한다
- default 값이 있는 파라미터와 없는 파라미터를 동시에 사용하는 경우 기본값 보다 뒤쪽에 있는 파라미터는 이름을 지정해야 한다

```kotlin
open class A{
    open fun foo(i:Int = 10){
        println(i)
    }
}

class B:A() {
    override fun foo(i:Int) {
        println(i)
    }
}

fun main(){
    val a = A()
    a.foo()
    val b = B()
    b.foo()
    b.foo(1000)
}
```

```kotlin
fun foo(bar:Int = 0, baz:Int) {
    println("$bar, $baz")
}

fun bar(foo:Int, baz:Int=0){
    println("$foo, $baz")
}

fun main() {
    foo(baz=1)
    bar(1)
    bar(1, 2)
}
```

- 람다식을 파라미터로 받을 수 있으며 람다식이 마지막 파라미터인 경우 괄호 밖에 적을 수 있다

```kotlin
fun foo(name:String, ex:()->Unit){
    println(name)
    ex()
}

fun bar(param:Int=1, ex:()->Unit) {
    println(param)
    ex()
}

fun main() {
    foo("abc") { println("Hello") }
    bar(2) { println("World") }
    bar { println("Kotlin") }
}
```

- varargs 키워드를 이용해 가변 개수의 파라미터를 받을 수 있다

```kotlin
fun foo(vararg items: Int) {
    for(i in items)
    	print("$i ")
}

fun main() {
    foo()
    foo(1)
    foo(1, 2, 3)
}
```

- spread 연산자 (*)를 이용해 가변 파라미터 함수를 사용할 수 있다

```kotlin
fun foo(vararg items:Int){
	for(i in items)
    	print("$i ")
}

fun main() {
    val arr = intArrayOf(1, 2, 3)
    foo(*arr)
}
```

<br />

#### infix 함수 만들기

- Member 함수 또는 Extension은 Infix 형태로 정의 가능
- 파라미터는 하나만 받아야 하고 기본값이 없어야 함

```kotlin
infix fun Int.diff(other:Int) = if(this > other) this-other else other-this

fun main() {
    var diff = 3 diff 1
    println(diff)
    diff = 1 diff 3
    println(diff)
}
```

- Local functions : 다른 함수 내부에 선언된 함수
  - local 함수는 외부 함수의 지역 변수에 접근 가능

```kotlin
fun foo() {
    var count = 0
    fun add() {
        println(count)
        count++
        if(count < 3) add()
    }
    add()
}

fun main() {
    foo()
}
```

- Tail recursive functions
  - Tail call : 함수의 마지막 코드가 함수 호출인 것
  - Tail recursion : 함수의 마지막 코드로 재귀 호출을 하는 것
  - 함수의 마지막 줄이 다른 함수 호출이라는 것은 이전 함수에서 더 이상 실행 할 코드가 없다는 뜻 -> 콜 스택에 모든 정보를 남길 필요가 없다 -> 성능을 높일 수 있다
  - 재귀 호출 함수를 tail racursion 으로 작성했다면 tailrec 키워드를 이용해 최적화를 할 수 있다

```kotlin
val eps = 1E-10

tailrec fun findFixPoint(x: Double = 1.0): Double =
	if (Math.abs(x - Math.cos(x)) < eps) x else findFixPoint(Math.cos(x))
```

- Tail recursive functions

```kotlin
tailrec fun foo(i:Int) {
    if(i == 0) return
    var next = i
    foo(--next)
}

tailrec fun bar(i:Int) {
    if(i==0) return
    var next = i
    foo(next--)
}

fun main() {
    foo(5)
    bar(5)
}
```

tailrec 최적화 ->

```java
public static final void foo(int i) {
    while(i != 0) {
        int next = -i - 1;
        i = next;
    }
}

public static final void bar(int i) {
    if(i != 0) {
        int var1 = i - 1;
        foo(i);
    }
}
```

<br />

# 고차원 함수와 람다

- 코틀린의 함수들은 First - class -> 함수를 다른 변수와 동일하게 다룰 수 있다
  - 함수를 파라미터로 받을 수 있다
  - 함수의 실행 결과로 함수를 반환할 수 있다
  - 함수를 변수나 자료구조에 저장할 수 있다
- 고차원 함수
  - 함수를 파라미터로 받을 수 있다
  - 함수의 실행결과로 함수를 반환할 수 있다

##### 함수의 타입 표기법

- ( parameter type, parameter type.. ) -> return type
- () -> Unit
- (Int) -> Int 등으로 파라미터 정의 및 함수의 return type 정의 가능

Top level 함수와 확장 함수는 :: 로 참조할 수 있다

- 함수 return

```kotlin
fun getBody(type:Int): () -> Unit {
    return if(type%2==0) {
        fun() {
            println("Hello")
        }
    } else {
        fun() {
            println("World")
        }
    }
}

fun main() {
    val f1 = getBody(1)
    f1()
    val f2 = getBody(2)
    f2()
}
```

- 함수를 변수에 할당하기, 함수를 파라미터로 받기

```kotlin
fun foo(i:Int, f:(Int)->Int):Int{
	return f(i)
}

fun bar(i:Int):Int = -i

fun main() {
    val f1 = ::bar
    val f2: (Int)->Int = ::bar
    f1(1)
    f2(-1)
    
    foo(1, fun(v:Int):Int{ return v*10 })
    foo(1) { it * 100 }
    foo(1, ::bar)
}
```

##### 람다식

- 함수로 선언되지는 않지만 함수 파라미터로 전달 가능

```kotlin
max(strings, { a, b -> a.length < b.length })
```

```kotlin
val sum: (Int, Int) -> Int = { x: Int, y: Int -> x + y }
```

```kotlin
val sum = { x: Int, y: Int -> x + y }
```

- 람다식이 함수의 마지막 파라미터인 경우 파라미터 바깥에 선언할 수 있다

```kotlin
val product = items.fold(1) { acc, e -> acc * e }
```

- 람다식이 유일한 파라미터인 경우 ()를 생략할 수 있다

```kotlin
run { println("...") }
```















