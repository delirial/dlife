---
title: "Basics"
date: 2023-08-15T19:06:49+02:00
draft: false
---
# Kotlin Basics
In a programmming language some elements are indispensable to have. Basic features, like numeric operations, variables and functions are common to all languages, while classes, type systems or annotation can be exclusive features. Kotlin have a lot of features, some basics and others exclusive make this language unique. Let's introduce some basics elements comparing them with java.

## Variables
Variables allow us to declare a name to a memory direction. In many language this operation is shadow to the user, delegate the logic to compilers. In Kotlin exist two types of variables declarations. The **non-mutable** `val`, and the **mutable** `var`. You can try to change the value of the *non-mutable* clicking on the run button.

{{< kotlin theme=darcula >}}
val inmutable = 42
var mutable = 32

fun changevariable(){
   mutable = 12
   inmutable = 12   
}
{{< /kotlin >}}

You must see an error like:
```
error: val cannot be reassigned
```
This is an important distinction, that allow us to express inmutable logic, and is a must in functional paradigm.

## Functions

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
// TODO
//sampleEnd  
{{< /kotlin >}}
