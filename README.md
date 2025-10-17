# cosmic-kotlin-bilingual-reference
A beginner-friendly Kotlin reference with bilingual (Urdu–English) explanations, mnemonics, and practical code examples. 🌱
Covers core topics like constructors, null safety, companion objects, and collections — and keeps growing daily as I add new concepts, definitions, and hands-on examples for clearer learning.
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

## 🔤 Definitions (Break and Continue)

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
---

## 🔤 Definitions (Function)

- **Function**: A reusable block of code that performs a specific task.
- **Parameters**: Inputs passed to a function to customize its behavior.
- **String Interpolation (`$var`, `${expression}`)**: Embeds variables or expressions directly inside strings.
- **`Unit`**: Kotlin’s equivalent of `void` in Java — indicates no meaningful return value.
- **Default Parameter**: A parameter with a pre-defined value used when no argument is passed.
- **Expression Body**: A concise way to define functions using `=` instead of `return`.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Function = "reusable machine"**  
  > _"Jaise aik chhoti factory jo har baar wahi kaam karti hai."_  
  Like a mini factory that performs the same task every time.

- **Parameters = "custom ingredients"**  
  > _"Jaise biryani mein mirch aur namak — har baar alag ho sakta hai."_  
  Like spices in biryani — you can adjust them each time.

- **String Interpolation = "inline printing"**  
  > _"Jaise sentence ke andar naam ghusa dena."_  
  Like inserting a name directly into a sentence.

- **`Unit` = "no return gift"**  
  > _"Kaam ho gaya, lekin kuch wapas nahi mila."_  
  Task completed, but nothing is returned.

- **Default Parameter = "backup value"**  
  > _"Agar user kuch na de to system apna value use karega."_  
  If no input is given, the system uses its own value.

- **Expression Body = "shortcut function"**  
  > _"Jaise ek line mein kaam nipta dena."_  
  Like finishing a task in one line.

---

## 💻 Code Example

```kotlin
fun main() {

    // Example 1 — Function with parameters and string interpolation
    fun printSum(a: Int, b: Int) {
        println("Sum of $a and $b is ${a + b}")
    }

    // Example 2 — Function returning Unit (like void in Java)
    fun printMessage(message: String): Unit {
        println(message)
    }

    // Example 3 — Function with a default parameter value
    fun printMessageWithPrefix(message: String, prefix: String = "Info") {
        println("[$prefix] $message")
    }

    // Example 4 — Function returning an Int explicitly
    fun sum(x: Int, y: Int): Int {
        return x + y
    }

    // Example 5 — Function with expression body (no need for 'return')
    fun multiply(x: Int, y: Int) = x * y

    // Example calls
    printSum(3, 7)
    printMessage("Hello, Kotlin!")
    printMessageWithPrefix("System starting...")
    printMessageWithPrefix("Low battery", "Warning")
    println("Sum result: ${sum(5, 8)}")
    println("Multiply result: ${multiply(4, 6)}")
}
```
---

## 🔤 Definitions (Overriding Methods)

- **`open`**: Marks a class or member as extendable or overridable.
- **`override`**: Replaces a superclass method or property with a new implementation in the subclass.
- **Base class**: A parent class that defines common behavior or structure.
- **Subclass**: A child class that inherits from a base class and can customize or extend its behavior.
- **Property overriding**: Changing the value or behavior of a property defined in a superclass.
- **Function overriding**: Replacing a method from the superclass with a new version in the subclass.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`open` = "permission to customize"**  
  > _"Jaise aik recipe jisme likha ho 'aap masalay badal sakte hain'."_  
  Like a recipe that allows you to change the spices.

- **`override` = "custom version"**  
  > _"Jaise aik student ne apna tareeqa apna liya — asal tareeqa chhor kar."_  
  Like a student using their own method instead of the original one.

- **Base class = "parent blueprint"**  
  > _"Jaise aik ghar ka naqsha jo sab ko diya gaya."_  
  Like a blueprint shared with all builders.

- **Subclass = "customized child"**  
  > _"Jaise har bacha apne tareeqay se kaam karta hai — asal se seekh kar."_  
  Like a child who learns from the parent but adds their own style.

- **Property overriding = "updated trait"**  
  > _"Jaise asal mein teen kone thay, lekin rectangle ne chaar kar diye."_  
  Like changing the number of corners from triangle to rectangle.

---

## 💻 Code Example

```kotlin
fun main() {

    // Example 1 — Base class with open functions
    open class Shape {
        open fun draw() {              // can be overridden
            println("Drawing a generic shape")
        }

        fun fill() {                   // not open → cannot be overridden
            println("Filling the shape")
        }
    }

    // Example 2 — Subclass overriding the function
    class Circle : Shape() {
        override fun draw() {          // overrides draw() from Shape
            println("Drawing a circle")
        }
    }

    // Example 3 — Overriding properties
    open class Polygon : Shape() {
        open val vertexCount: Int = 3  // open property for overriding
        override fun draw() {          // can still override draw()
            println("Drawing a polygon with $vertexCount vertices")
        }
    }

    class Rectangle : Polygon() {
        override val vertexCount: Int = 4   // override property value
        override fun draw() {               // override function again
            println("Drawing a rectangle with $vertexCount vertices")
        }
    }

    // Example 4 — Using the classes
    val shape = Shape()
    val circle = Circle()
    val polygon = Polygon()
    val rectangle = Rectangle()

    shape.draw()
    shape.fill()

    circle.draw()

    polygon.draw()
    rectangle.draw()

    println("Rectangle vertex count: ${rectangle.vertexCount}")
}
```
---

## 🔤 Definitions (Extension Function)

- **Extension Function**: A way to add new functionality to existing classes without modifying their source code.
- **`this` keyword**: Refers to the current object — in extension functions, it refers to the receiver (e.g., the list).
- **Generic Function (`<T>`)**: A function that works with any type, making it reusable and type-safe.
- **MutableList**: A list that allows modification — adding, removing, or updating elements.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Extension Function = "add-on skill"**  
  > _"Jaise aik aadmi ko nayi skill sikhana bina uski asal shakl badle."_  
  Like teaching someone a new skill without changing who they are.

- **`this` = "current object pointer"**  
  > _"Jaise 'main khud' — jab koi banda apne baare mein baat karta hai."_  
  Like saying “I myself” — refers to the current object.

- **Generic Function = "universal tool"**  
  > _"Jaise aik screwdriver jo har size ke bolt ko khol sakta hai."_  
  Like a screwdriver that fits any bolt size.

- **MutableList = "editable notebook"**  
  > _"Jaise aik diary jisme aap kuch bhi likh sakte hain, mita sakte hain."_  
  Like a diary where you can write, erase, and update freely.

---

## 💻 Code Example

```kotlin
fun main() {

    // Example 1 — Extension function for MutableList<Int>
    fun MutableList<Int>.swap(index1: Int, index2: Int) {
        val tmp = this[index1]       // 'this' refers to the list itself
        this[index1] = this[index2]  // swap values
        this[index2] = tmp
    }

    // Using the Int-specific version
    val intList = mutableListOf(1, 2, 3)
    println("Before swap (Int list): $intList")
    intList.swap(0, 2)               // swaps first and last
    println("After swap (Int list):  $intList\n")


    // Example 2 — Generic version (works for any type)
    fun <T> MutableList<T>.swap(index1: Int, index2: Int) {
        val tmp = this[index1]       // 'this' refers to the current list
        this[index1] = this[index2]
        this[index2] = tmp
    }

    // Using the generic version with Strings
    val stringList = mutableListOf("A", "B", "C")
    println("Before swap (String list): $stringList")
    stringList.swap(0, 2)            // swaps "A" and "C"
    println("After swap (String list):  $stringList")
}
```
