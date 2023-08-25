---
title: "Object Oriented Programming"
date: 2023-08-16T13:16:49+02:00
draft: false
---



## Objects
Singleton in kotlin

## Objects expressions 
Replace Java anonymous classes

## Companion Objects
Nested object inside a class but special, because avoid statics problems in Java.

- Implement an interface
- Be the receiver for extensions functions

`@JvmStatic`

## Constants
You can make constants in kotlin with keyword const. Only work in primitives types and String. 
`const val answer = 42`
Also to interoperability with Java you can exposes a kotlin property as a field in Java with annotation `@JvmField`.
`@JvmField
val answer = 42
`
same as in Java:    
`
public static final Number answer = 42
`

## Generics
The generics in kotlin works like in Java. ???

```
interface List<E> {
   fun get(index:Int):E
}
```

You can make generic functions like this:

```
fun <T> List<T>.filter(predicate:(T)-> Boolean):List<T>
```

But this assume that the List could have nullable types. With nullability in mind, you can see that we have three posibilities here:
- Nullable generic argument
- Non-nullable upper bound

As an example we can write a function that filter nullable elements and only return the non-nullable ones.
```
fun <T:Any> List<T?>.filterNonNull(): List<T> {...}
```

Multiple constraint for a type parameter allow us to define more specifics generics. For instance:
```
fun <T> trailing( seq: T ) where T: CharSequence, T: Appendable { ... }
```

If you want to use some extension with differents types declared with generics, you need to change the name in the jvm with:
{{< kotlin theme=darcula targetPlatform=junit foldedButton=true >}}
fun List<Int>.average(): Double {...}
@JvmName("averageOfDouble")
fun List<Double>.average(): Double {...}
{{</kotlin>}}


### Queer
Null Pointer Exception in pure kotlin. WHY!!
{{< kotlin theme=darcula targetPlatform=junit foldedButton=true >}}
import org.junit.Test
import org.junit.Assert

class TestExtensionFunctions() {
    @Test fun testIntExtension() {
        Assert.assertEquals("Non mutable: ", inmutable, 42)
    }

    @Test fun testPairExtension() {
        Assert.assertEquals("Mutable : ", mutable, 12)
    }
}
//sampleStart
open class A(open val value: String) {
    init {
      value.length
    }
}

class B(override val value: String) : A(value)

fun main(args: Array<String>) {
    B("a")
}
//sampleEnd  
{{< /kotlin >}}