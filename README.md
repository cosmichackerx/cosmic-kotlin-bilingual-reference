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
