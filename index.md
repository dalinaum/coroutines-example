## 코루틴 예제 

첫번째 코루틴 예제입니다.

<script src="https://unpkg.com/kotlin-playground@1"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
  KotlinPlayground('.kotlin-playground');
});
</script>

<div class="kotlin-playground" >
fun main() {
    val name = "stranger"        // Declare your first variable
    println("Hi, $name!")        // ...and use it!
    print("Current count:")
    for (i in 0..10) {           // Loop over a range from 0 to 10
        print(" $i")
    }
}
</div>

다음의 코루틴을 수행해봅시다.

<div class="kotlin-playground" >
fun main() = runBlocking { // this: CoroutineScope
    launch { // launch a new coroutine and continue
        delay(1000L) // non-blocking delay for 1 second (default time unit is ms)
        println("World!") // print after delay
    }
    println("Hello") // main coroutine continues while a previous one is delayed
}
</div>
