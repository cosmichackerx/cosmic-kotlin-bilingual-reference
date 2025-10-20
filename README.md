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
![0](resources/0.png)
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
![1](resources/1.png)
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
![2](resources/2.png)
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
![3](resources/3.png)
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
![4](resources/4.png)
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
![5](resources/5.png)
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
![6](resources/6.png)
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
![7](resources/7.png)
---

## 🔤 Definitions (Classes)

- **`open` class**: Allows other classes to inherit from it. By default, Kotlin classes are final and cannot be extended.
- **Primary constructor**: The main constructor declared in the class header. Used for initializing properties.
- **Secondary constructor**: An optional constructor declared inside the class body for alternative initialization.
- **Constructor injection**: A technique where dependencies are passed directly into the constructor — often used in frameworks.
- **Property declaration in constructor**: Kotlin allows concise property initialization directly in the constructor.
- **Default parameter value**: A value assigned to a parameter if no argument is provided during object creation.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`open` = "permission to inherit"**  
  > _"Jaise aik teacher ne kaha 'ye notes sab copy kar sakte hain'."_  
  Like a teacher allowing everyone to copy the notes.

- **Primary constructor = "main entry gate"**  
  > _"Jaise ghar ka main darwaza — sabse pehla raasta andar aane ka."_  
  Like the main door to a house — the primary way to enter.

- **Secondary constructor = "side gate"**  
  > _"Jaise garage ka raasta — alternative tareeqa andar aane ka."_  
  Like a side entrance — an alternative way to enter.

- **Constructor injection = "ready-made delivery"**  
  > _"Jaise pizza order ke sath toppings already aa jayein."_  
  Like getting a pizza with toppings already included.

- **Property declaration in constructor = "one-line setup"**  
  > _"Jaise aik hi line mein naam, umar aur kaam likh diya jaye."_  
  Like writing name, age, and job in one line.

- **Default value = "backup plan"**  
  > _"Agar user kuch na de to system apna value use karega."_  
  If no input is given, the system uses its own value.

---

## 💻 Code Example

```kotlin
fun main() {
    // 'open' allows other classes to inherit this class
    open class Shape

    // 'Rectangle' extends 'Shape' and has two properties: height and length
    class Rectangle(var height: Double, var length: Double) : Shape() {
        var perimeter = (height + length) * 2  // property for perimeter
    }

    // A simple class with a primary constructor
    class Person constructor(firstName: String) {
        /*...*/
    }

    // Example of constructor injection (useful in dependency injection frameworks)
    class Customer @Inject constructor(name: String) {
        /*...*/
    }

    // Another class example with a primary constructor
    class Person1(firstName: String) {
        /*...*/
    }

    // Class with multiple properties in primary constructor
    class Person2(val firstName: String, val lastName: String, var age: Int)

    // Class with a default value for a property
    class Person3(val firstName: String, val lastName: String, var isEmployed: Boolean = true)

    // Example usage:
    val rect = Rectangle(5.0, 10.0)
    println("Perimeter of rectangle: ${rect.perimeter}")
}
```
---

---

## 🔤 Definitions (Secondary constructor)

- **Primary constructor**: The main constructor declared in the class header, used to initialize properties.
- **Secondary constructor**: An optional constructor declared inside the class body for alternative initialization logic.
- **`init` block**: A special block that runs immediately when an object is created — before any secondary constructor.
- **Private constructor**: A constructor that restricts object creation from outside the class.
- **Constructor chaining**: When a secondary constructor calls the primary constructor using `: this(...)`.
- **MutableList**: A list that can be modified — elements can be added, removed, or updated.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Primary constructor = "main gate"**  
  > _"Jaise ghar ka asal darwaza — sabse pehla raasta andar aane ka."_  
  Like the main entrance of a house — the default way to enter.

- **Secondary constructor = "side gate"**  
  > _"Jaise garage ka raasta — alternative tareeqa andar aane ka."_  
  Like a side entrance — used when extra setup is needed.

- **`init` block = "welcome message"**  
  > _"Jaise ghar mein ghusne par pehle salam hoti hai."_  
  Like a greeting that happens as soon as someone enters.

- **Private constructor = "no entry allowed"**  
  > _"Jaise aik locked room — sirf andar se khula ja sakta hai."_  
  Like a locked room — only accessible internally.

- **Constructor chaining = "one setup calls another"**  
  > _"Jaise ek kaam karne se doosra kaam bhi ho jaye."_  
  Like doing one task that automatically triggers another.

- **MutableList = "editable diary"**  
  > _"Jaise aik diary jisme naye log likhe ja sakte hain."_  
  Like a diary where new entries (children) can be added.

---

## 💻 Code Example

```kotlin
fun main() {

    // Class with primary and secondary constructors
    class Person(val name: String) {

        // Each person can have children (list of Person objects)
        val children: MutableList<Person> = mutableListOf()

        // Secondary constructor — adds this new person to the parent's children list
        constructor(name: String, parent: Person) : this(name) {
            parent.children.add(this)
        }
    }

    // Class with primary and secondary constructors
    class Constructors {

        // init block runs whenever an instance is created
        init {
            println("Primary constructor called (no parameters)")
        }

        // Secondary constructor
        constructor(i: Int) {
            println("Secondary constructor called with value: $i")
        }
    }

    // Example of a class with private constructor (cannot be instantiated outside)
    class DontCreateMe private constructor() {
        /*...*/
    }

    // --- Example Usage ---
    val parent = Person("Alice")
    val child = Person("Bob", parent)
    println("${parent.name}'s children: ${parent.children.map { it.name }}")

    val obj1 = Constructors()
    val obj2 = Constructors(10)
}
```
---

## 🔤 Definitions (Data Classes)

- **`data class`**: A special class in Kotlin designed to hold data. It automatically generates utility methods.
- **`toString()`**: Returns a readable string representation of the object.
- **`equals()`**: Compares two objects for equality based on their properties.
- **`hashCode()`**: Generates a hash value used in hashing structures like maps and sets.
- **`copy()`**: Creates a new object with modified properties while keeping others unchanged.
- **`componentN()`**: Enables destructuring declarations (e.g., `val (name, age) = user`).

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **`data class` = "smart container"**  
  > _"Jaise aik dabba jo apne andar ki cheezon ka pura record rakhta hai."_  
  Like a box that keeps track of everything inside — name, age, etc.

- **`toString()` = "self-introduction"**  
  > _"Jaise banda apna naam aur umar bata raha ho."_  
  Like someone introducing themselves with name and age.

- **`copy()` = "clone with change"**  
  > _"Jaise photocopy kar ke sirf aik cheez badal dena."_  
  Like making a copy and changing just one detail.

- **`equals()` = "identity check"**  
  > _"Jaise do ID cards compare karna — dono same hain ya nahi."_  
  Like comparing two ID cards to see if they match.

- **Destructuring = "split and assign"**  
  > _"Jaise aik box khol kar alag alag cheezein nikaal lena."_  
  Like unpacking a box and assigning each item to a variable.

---

## 💻 Code Example

```kotlin
fun main() {

    /*
     * Data classes are used to hold data.
     * Kotlin automatically generates useful methods such as:
     * - toString()  → for readable object output
     * - equals()    → for object comparison
     * - hashCode()  → for hashing
     * - copy()      → for creating modified copies
     * - componentN() functions for destructuring
     */
    data class User(val name: String, val age: Int)

    // Creating an object of the data class
    val user1 = User("Muhammad", 19)

    // Printing object (uses auto-generated toString())
    println(user1)

    // Copying with modification
    val user2 = user1.copy(age = 20)

    // Comparing two data objects (uses auto-generated equals())
    println(user1 == user2)

    // Destructuring declaration
    val (name, age) = user2
    println("Name: $name, Age: $age")
}
```
---

## 🔤 Definitions (Interfaces)

- **Interface**: A blueprint or contract that defines functions a class must implement.
- **`fun foo()`**: A function declared in the interface without a body — must be implemented by the class.
- **`fun bar()`**: A function with a default body — optional for the implementing class to override.
- **`override`**: A keyword used to provide a custom implementation of a function defined in an interface or superclass.
- **Implementation**: The actual code written in a class to fulfill the contract defined by the interface.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Interface = "contract or promise"**  
  > _"Jaise aik agreement jisme likha ho ke kya kaam karna hai."_  
  Like a contract that says what tasks must be done.

- **Function without body = "must-do task"**  
  > _"Jaise boss ne kaha 'ye kaam zaroor karna hai' — detail baad mein tum likho."_  
  Like a boss assigning a task — you must decide how to do it.

- **Function with body = "optional helper"**  
  > _"Jaise boss ne example bhi de diya — agar chaho to use karo."_  
  Like a boss giving a sample solution — you can use it or write your own.

- **`override` = "custom execution"**  
  > _"Jaise kisi kaam ka apna tareeqa apna lena."_  
  Like doing a task your own way instead of the default.

---

## 💻 Code Example

```kotlin
// Defining an interface — a contract that classes can implement
interface MyInterface {

    // Default method with implementation (optional)
    fun bar() {
        println("bar() function with default body")
    }

    // Abstract method (must be implemented by any class that implements this interface)
    fun foo()
}

// A class implementing the interface
class MyClass : MyInterface {
    // Must override foo() because it has no default implementation
    override fun foo() {
        println("foo() function implemented in MyClass")
    }
}

// Main function to test interface implementation
fun main() {
    val obj = MyClass()  // Create object of MyClass
    obj.foo()             // Calls overridden function
    obj.bar()             // Calls default function from interface
}
```
---

## 🔤 Definitions (Implementation)

- **Interface**: A contract that defines behaviors (functions) a class must follow.
- **Default implementation**: A function inside an interface that already has a body — can be used as-is or overridden.
- **`override`**: A keyword used to replace the default behavior with a custom one in the implementing class.
- **Implementing class**: A class that agrees to follow the interface and provide its own versions of the required functions.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Interface = "behavior contract"**  
  > _"Jaise aik job description — har employee ko follow karna hota hai."_  
  Like a job description — every employee must follow it.

- **Default implementation = "ready-made solution"**  
  > _"Jaise boss ne kaam ka tareeqa bhi bata diya — chaho to apna tareeqa use karo."_  
  Like a boss giving a suggested method — you can use it or customize it.

- **Override = "custom behavior"**  
  > _"Jaise aik chef ne apni recipe mein thoda twist daal diya."_  
  Like a chef adding their own twist to a standard recipe.

- **Implementing class = "contract follower"**  
  > _"Jaise aik student jo school ke rules follow karta hai."_  
  Like a student who follows the school’s rules.

---

## 💻 Code Example

```kotlin
// Define an interface (a contract of behaviors)
interface MyInterface {

    // Function with a default implementation
    fun bar() {
        println("Default bar() from MyInterface")
    }
}

// Class implementing the interface
class Child : MyInterface {

    // Overriding the interface function
    override fun bar() {
        println("bar() overridden in Child class")
    }
}

// Main function — program entry point
fun main() {
    val obj = Child()  // Create object of Child
    obj.bar()          // Calls overridden version from Child
}
```
---

## 🔤 Definitions (Properties in Interface)

- **Interface**: A contract that defines abstract and optionally implemented members (functions or properties).
- **Abstract property**: A property declared without a body — must be implemented by the class.
- **Property with implementation**: A read-only property inside an interface that provides a default value.
- **`override`**: Used to provide a concrete implementation of abstract members from an interface or superclass.
- **Interface function using property**: Functions in interfaces can access both abstract and implemented properties.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Interface = "rulebook with examples"**  
  > _"Jaise aik kitab jisme kuch kaam karne ke tareeqay likhe hain — kuch sirf headings, kuch poore."_  
  Like a manual where some tasks are just listed, others are fully explained.

- **Abstract property = "must-fill blank"**  
  > _"Jaise form mein khaali jagah — har banda apna jawab likhe."_  
  Like a blank in a form — everyone must fill it in.

- **Property with implementation = "default answer"**  
  > _"Jaise form mein kuch fields pehle se bharay huay hon."_  
  Like pre-filled fields in a form — you can use them as-is.

- **`override` = "personalized version"**  
  > _"Jaise kisi ne asal tareeqa chhor kar apna naya tareeqa likh diya."_  
  Like replacing the default method with your own.

- **Interface function using property = "template with variables"**  
  > _"Jaise aik sentence jisme naam aur umar insert karni ho."_  
  Like a sentence that uses variables to complete itself.

---

## 💻 Code Example

```kotlin
// Interface can contain both abstract and concrete (implemented) properties and functions
interface MyInterface {

    // Abstract property — must be implemented by the class
    val prop: Int

    // Property with default implementation (read-only)
    val propertyWithImplementation: String
        get() = "foo"

    // Function using the abstract property
    fun foo() {
        println(prop)
    }
}

// Class implementing the interface
class Child : MyInterface {

    // Must override abstract property 'prop'
    override val prop: Int = 29
}

// Main function — program entry point
fun main() {
    val obj = Child()         // Create object of Child
    obj.foo()                 // Calls foo() → prints prop value (29)
    println(obj.propertyWithImplementation) // Accesses implemented property "foo"
}
```
---

## 🔤 Definitions (Comments)

- **Single-line comment (`//`)**: Used to add short notes or explanations on a single line.
- **Block comment (`/* ... */`)**: Used for multi-line explanations or to temporarily disable code blocks.
- **Documentation comment (`/** ... */`)**: Known as KDoc in Kotlin — used to generate API documentation for classes, functions, and parameters.
- **Inline comment**: A comment written on the same line as a statement, typically to explain that specific line.

---

## 🧠 Mnemonics & Analogies (English + Urdu)

- **Single-line comment = "quick whisper"**  
  > _"Jaise kisi line ke saath chhoti si baat likh dena."_  
  Like whispering a quick note beside a sentence.

- **Block comment = "sticky note on code"**  
  > _"Jaise aik bara sticky note jo poora code block cover karta hai."_  
  Like placing a sticky note over a whole section of code.

- **Documentation comment = "official label"**  
  > _"Jaise kisi file ke upar likha ho 'ye kya karta hai' taake doosre samajh saken."_  
  Like labeling a file with its purpose so others can understand it.

- **Inline comment = "side note"**  
  > _"Jaise kisi jumlay ke baad zara si wazahat likhna."_  
  Like adding a small side note after a sentence.

---

## 💻 Code Example

```kotlin
// Comments

// This is an end-of-line comment (single line)

/*
   This is a block comment
   that spans multiple lines.
   Useful for disabling or explaining code blocks.
*/

/**
 * This is a documentation comment (KDoc)
 * Used for generating documentation automatically.
 * Example: functions, classes, parameters, etc.
 */

fun main() {
    // You can add inline comments inside code too
    println("Hello, Kotlin!") // Prints greeting message
}
```
