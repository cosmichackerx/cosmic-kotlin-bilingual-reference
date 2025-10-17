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

## 🔤 Definitions

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

## 🔤 Definitions

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

## 🔤 Definitions

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
