# cosmic-kotlin-bilingual-reference
A beginner-friendly Kotlin reference with bilingual (Urdu-English) explanations, mnemonics, and practical code examples. Covers key topics like constructors, null safety, companion objects, and collections — designed for learners who love clarity, analogies, and hands-on coding

## 🔤 Definitions

- **`when` expression**: Kotlin’s powerful replacement for `switch`. It checks a value against multiple conditions.
- **`is` keyword**: Used for **type checking**. It verifies if a variable is of a specific type.
- **`Int`, `String`, `IntArray`**: Built-in Kotlin types for integers, text, and arrays of integers.
- **`println()`**: Prints output to the console.
- **`x + 1`**: Adds 1 to the integer.
- **`x.length + 1`**: Gets the length of the string and adds 1.
- **`x.sum()`**: Calculates the sum of all elements in an integer array.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`when` = "multi-condition gate"**  
  > _"Jaise ek chowk jahan har raasta alag condition ka hai."_  
  Like a traffic junction — each path leads to a different outcome.

- **`is` = "type detector"**  
  > _"Jaise passport check karta hai ke banda Pakistani hai ya nahi."_  
  Like checking someone's passport to confirm their nationality.

- **`?.` = "safe call bell"**  
  > _"Ghanti sirf tab bajti hai jab koi ho."_  
  The bell rings only if someone is present — avoids null crashes.

---

## 💻 Code Example

```kotlin
fun main() {  
    var x = 70

    when(x){
        is Int -> println(x + 1)
        is String -> println(x.length + 1)
        is IntArray -> println(x.sum())
    }
}
```
---

## 🔤 Definitions (Safe vs Unsafe cast)

- **`as` (Unsafe Cast)**: Forcefully converts a value to a specific type. If the actual type doesn't match, it throws a `ClassCastException`.
- **`as?` (Safe Cast)**: Attempts to convert a value to a specific type. If the cast fails, it returns `null` instead of crashing.
- **`Any`**: The universal supertype in Kotlin. Every non-nullable type inherits from `Any`.
- **`String?`**: A nullable string — can hold either a string or `null`.
- **`Long?`**: A nullable long integer — can hold a long value or `null`.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`as` = "forceful cast"**  
  > _"Jaise zabardasti kehna 'ye kitab Urdu ki hai' bina dekhe."_  
  Like insisting a book is Urdu without checking — risky and crash-prone.

- **`as?` = "polite cast"**  
  > _"Jaise tameez se pehle dekh lena, agar Urdu hai to padho, warna chhor do."_  
  Like checking politely — if it fits, use it; if not, return `null`.

- **`Any` = "universal container"**  
  > _"Jaise aik box jisme kuch bhi ho sakta hai."_  
  Like a box that can hold anything — string, number, or even an array.

---

## 💻 Code Example

```kotlin
fun main() {  
    val obj: Any = "Hello"

    // Unsafe Cast
    val str: String = obj as String // ✅ Returns "Hello"
    val std: String? = obj as String // ✅ Returns "Hello"

    // Safe Cast
    val num: Long? = obj as? Long // ✅ Returns null, no crash

    println("-= $str $std $num")
}
```
---

## 🔤 Definitions (If Expression)

- **`if` statement**: A conditional block that executes code based on whether a condition is true or false.
- **`if-else` block**: Provides two paths — one for `true`, one for `false`.
- **`if` as an expression**: Returns a value directly based on the condition.
- **`val` vs `var`**: `val` is immutable (like `final` in Java), `var` is mutable.
- **`println()`**: Prints output to the console.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`if` = "decision gate"**  
  > _"Jaise aik chowk jahan condition ke mutabiq raasta chunta hai."_  
  Like a junction where the path depends on the condition.

- **`if-else` = "two-way switch"**  
  > _"Jaise bijli ka switch — agar on ho to light, warna andhera."_  
  Like a light switch — either ON or OFF.

- **`if` as expression = "smart shortcut"**  
  > _"Jaise aik sawal ka turant jawab — bina poora essay likhe."_  
  Like giving a direct answer instead of writing a full essay.

---

## 💻 Code Example

```kotlin
fun main() {  
    val a = 10  
    val b = 20  

    // Simple if condition
    var max = a
    if (a < b) max = b

    // Using if-else block
    var max2: Int
    if (a > b) {
        max2 = a
    } else {
        max2 = b
    }

    // Using if as an expression (short form)
    val max3 = if (a > b) a else b

    // Using if as expression with print statements
    val max4 = if (a > b) {
        println("Choose a")
        a
    } else {
        println("Choose b")
        b
    }

    // Display results
    println("max = $max")
    println("max2 = $max2")
    println("max3 = $max3")
    println("max4 = $max4")
}
```
---

## 🔤 Definitions (When Expression)

- **`when`**: Kotlin’s flexible alternative to `switch`. It matches a value or condition against multiple branches.
- **`enum class`**: A special class used to define a fixed set of constants.
- **`in` / `!in`**: Used to check if a value exists inside a range or collection.
- **`is`**: Used for type checking — smart casts allow safe access to properties.
- **`sealed class`**: Restricts class hierarchy to known subclasses — useful for exhaustive `when` expressions.
- **`when as expression`**: Returns a value directly from the matched branch.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`when` = "multi-path decision gate"**  
  > _"Jaise aik chowk jahan har raasta alag condition ka hai."_  
  Like a junction where each path depends on a condition.

- **`enum` = "fixed menu"**  
  > _"Jaise restaurant ka menu — sirf kuch hi options."_  
  Like a restaurant menu — only specific choices allowed.

- **`in` / `!in` = "membership check"**  
  > _"Jaise dekhna ke banda group mein hai ya nahi."_  
  Like checking if someone belongs to a group.

- **`is` = "type passport"**  
  > _"Jaise passport check karta hai ke banda Pakistani hai ya nahi."_  
  Like verifying someone's identity by their type.

- **`sealed class` = "controlled family tree"**  
  > _"Jaise ek khandan jisme sirf kuch hi members allowed hain."_  
  Like a family with limited, known members.

---

## 💻 Code Examples

```kotlin
fun main() {
    val x = 2
    val y = 5
    val s = "5"
    val validNumbers = listOf(2, 4, 6, 8, 10)

    // Example 1 — Simple when statement
    when (x) {
        1 -> println("x == 1")
        2 -> println("x == 2")
        else -> {
            println("x is neither 1 nor 2")
        }
    }

    // Example 2 — when as an expression (else required if not all cases covered)
    enum class Bit { ZERO, ONE }

    fun getRandomBit(): Bit = if (Math.random() > 0.5) Bit.ONE else Bit.ZERO

    val numericValue = when (getRandomBit()) {
        Bit.ZERO -> 0
        Bit.ONE -> 1
    }
    println("Numeric value: $numericValue")

    // Example 3 — when with enums (with and without else)
    enum class Color { RED, GREEN, BLUE }

    fun getColor(): Color = Color.GREEN

    when (getColor()) {
        Color.RED -> println("red")
        Color.GREEN -> println("green")
        Color.BLUE -> println("blue")
    }

    when (getColor()) {
        Color.RED -> println("red")
        else -> println("not red")
    }

    // Example 4 — multiple conditions in one branch
    when (x) {
        0, 1 -> println("x == 0 or x == 1")
        else -> println("otherwise")
    }

    // Example 5 — arbitrary expressions in conditions
    when (x) {
        s.toInt() -> println("s encodes x")
        else -> println("s doesn't encode x")
    }

    // Example 6 — checking ranges and collections
    when (x) {
        in 1..10 -> println("x is in the range 1..10")
        in validNumbers -> println("x is a valid number")
        !in 10..20 -> println("x is outside 10..20")
        else -> println("none of the above")
    }

    // Example 7 — type checking (smart casts)
    fun hasPrefix(x: Any) = when (x) {
        is String -> x.startsWith("prefix")
        else -> false
    }
    println("Has prefix: ${hasPrefix("prefixTest")}")

    // Example 8 — when without argument (condition-based)
    fun Int.isOdd() = this % 2 != 0
    fun Int.isEven() = this % 2 == 0

    when {
        x.isOdd() -> println("x is odd")
        y.isEven() -> println("y is even")
        else -> println("x + y is odd")
    }
}

// Example 9 — when as expression with result handling
// We can capture when subject in a variable using following syntax
sealed class Response
class Success(val body: String) : Response()
class HttpError(val status: Int) : Response()

fun executeRequest(): Response =
    if (Math.random() > 0.5) Success("OK") else HttpError(404)

fun getBody(): String = when (val response = executeRequest()) {
    is Success -> response.body
    is HttpError -> throw Exception("HTTP Error: ${response.status}")
}
```
---

## 🔤 Definitions

- **Labeled loop (`loop@`)**: A named loop that allows you to break or continue from outer loops.
- **`break@label`**: Exits the loop with the specified label.
- **`return`**: Exits from a function or lambda.
- **`return@label`**: Performs a local return from a lambda or block with a label.
- **Anonymous function**: A function without a name, often used inside higher-order functions like `forEach`.
- **`run` block**: Executes a block of code and returns its result — can be labeled for controlled exits.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Labeled loop = "named gate"**  
  > _"Jaise har darwaza ka naam ho — taake pata chale kis darwazay se nikalna hai."_  
  Like naming each door so you know exactly which one to exit.

- **`break@label` = "emergency exit from specific gate"**  
  > _"Jaise aik building mein se seedha bahar nikalna — bina andar ke raste follow kiye."_  
  Like exiting a building directly from a specific door.

- **`return` in lambda = "exit from function"**  
  > _"Jaise kisi kaam ko chhor kar seedha ghar chale jaana."_  
  Like abandoning a task and going home immediately.

- **`return@label` = "skip this step only"**  
  > _"Jaise aik sawal chhor kar agla sawal karna — poora paper nahi chhorna."_  
  Like skipping one question without leaving the whole exam.

- **Anonymous function = "nameless helper"**  
  > _"Jaise aik mazdoor jo kaam karta hai bina naam bataye."_  
  Like a worker who does the job without introducing himself.

---

## 💻 Code Example

```kotlin
fun main() {

    // Example 1 — Simple labeled loop (label name = loop)
    loop@ for (i in 1..100) {
        // Do something
        // break@loop or continue@loop can be used here if needed
    }

    // Example 2 — Using break with a label (breaks outer loop)
    loop@ for (i in 1..100) {
        for (j in 1..100) {
            if (i * j > 500) break@loop // exits both loops when condition met
        }
    }

    // Example 3 — Non-local return from lambda (stops whole function)
    fun foo1() {
        listOf(1, 2, 3, 6, 5).forEach {
            if (it == 3) return // exits foo1() completely
            println(it)
        }
        println("this point is unreachable") // never runs
    }

    // Example 4 — Local return using explicit label
    fun foo2() {
        listOf(1, 2, 3, 4, 5).forEach Muhammad@{
            if (it == 3) return@Muhammad // skips only this iteration
            println(it)
        }
        println("done with explicit label")
    }

    // Example 5 — Local return using implicit label (forEach)
    fun foo3() {
        listOf(1, 2, 3, 4, 5).forEach {
            if (it == 3) return@forEach // continues loop, doesn’t exit function
            println(it)
        }
        println("done with implicit label")
    }

    // Example 6 — Local return with anonymous function
    fun foo4() {
        listOf(1, 2, 3, 4, 5).forEach(fun(value: Int) {
            if (value == 3) return // returns only from anonymous function
            println(value)
        })
        println("done with anonymous function")
    }

    // Example 7 — Using run block with label
    fun foo5() = run loop@{
        listOf(1, 2, 3, 4, 5).forEach {
            if (it == 3) return@loop // exits run block, not main
            print(it)
        }
    }

    // Call all examples
    foo1()
    foo2()
    foo3()
    foo4()
    foo5()
    println("\nAll loops completed.")
}
```
