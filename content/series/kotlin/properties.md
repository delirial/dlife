---
title: "Properties"
date: 2023-08-16T13:10:49+02:00
draft: false
---

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
class A {
    private lateinit var prop: String

    fun setUp() {
        prop = "value"
    }

    fun display() {
        if (prop.isInitialized) println(prop)
    }
}

fun main(args: Array<String>) {
    val a = A()
    // If display fun haven't initalized check, then kotlin throw an UninitializedPropertyAccessException
    a.display()
}
//sampleEnd  
{{< /kotlin >}}