# JS-CONCEPTS

## my documentation for [33-js-concepts](https://github.com/leonardomso/33-js-concepts)

check the diff branches for the docs

# Primitive Types

All types except Object define immutable values represented directly at the lowest level of the language. We refer to values of these types as primitive values.

the primitive types are:
Null
Undefined
Number
Boolean
BigInt
String
Symbol

> If primitives have no properties, why does "abc".length return a value?

Because JavaScript will readily coerce between primitives and objects. In this case the string value is coerced to a string object in order to access the property length. The string object is only used for a fraction of second after which it is sacrificed to the Gods of garbage collection
