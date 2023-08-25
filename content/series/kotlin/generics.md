---
title: "Generics"
date: 2023-08-23T12:36:55Z
draft: true
---

The generics in `kotlin` must be discuss related with the type system. For example when we have:
{{< kotlin theme=darcula >}}
class Box<T>(t: T) {
    var value = t
}
{{</kotlin>}}

## Variance
In a type generic system, when a type `T` is a subtype of other type `E`, that could be express it like:

$$
T \in E
$$

`T` has **variance** with `E`
Declaration-site variance and type projections. 