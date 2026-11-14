# Target

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Target

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class Target
```

| [java.lang.annotation.Target](Target.md) |

Indicates the contexts in which an annotation interface is applicable. The declaration contexts and type contexts in which an annotation interface may be applicable are specified in JLS {@jls 9.6.4.1}, and denoted in source code by enum constants of [java.lang.annotation.ElementType](ElementType.md).

If an `@Target` meta-annotation is not present on an annotation interface `T`, then an annotation of type `T` may be written as a modifier for any declaration.

If an `@Target` meta-annotation is present, the compiler will enforce the usage restrictions indicated by `ElementType` enum constants, in line with JLS {@jls 9.7.4}.

For example, this `@Target` meta-annotation indicates that the declared interface is itself a meta-annotation interface. It can only be used on annotation interface declarations: 

```kotlin
@Target(ElementType.ANNOTATION_TYPE)
     public @interface MetaAnnotationType {
         ...
     }
  
```

This `@Target` meta-annotation indicates that the declared class or interface is intended solely for use as a member class or interface in complex annotation interface declarations. It cannot be used to annotate anything directly: 

```kotlin
@Target({})
     public @interface MemberInterface {
         ...
     }
  
```

It is a compile-time error for a single `ElementType` constant to appear more than once in an `@Target` annotation. For example, the following `@Target` meta-annotation is illegal: 

```kotlin
@Target({ElementType.FIELD, ElementType.METHOD, ElementType.FIELD})
     public @interface Bogus {
         ...
     }
  
```

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Target](Target.md))`(`vararg` `value:` ` [ElementType](ElementType.md)`)` Indicates the contexts in which an annotation interface is applicable. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ElementType](ElementType.md)\> | [value](Target.md) Returns an array of the kinds of elements an annotation interface can be applied to. |

## Public constructors

### Target

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Target(vararg value: ElementType)
```

Indicates the contexts in which an annotation interface is applicable. The declaration contexts and type contexts in which an annotation interface may be applicable are specified in JLS {@jls 9.6.4.1}, and denoted in source code by enum constants of [java.lang.annotation.ElementType](ElementType.md).

If an `@Target` meta-annotation is not present on an annotation interface `T`, then an annotation of type `T` may be written as a modifier for any declaration.

If an `@Target` meta-annotation is present, the compiler will enforce the usage restrictions indicated by `ElementType` enum constants, in line with JLS {@jls 9.7.4}.

For example, this `@Target` meta-annotation indicates that the declared interface is itself a meta-annotation interface. It can only be used on annotation interface declarations: 

```kotlin
@Target(ElementType.ANNOTATION_TYPE)
     public @interface MetaAnnotationType {
         ...
     }
  
```

This `@Target` meta-annotation indicates that the declared class or interface is intended solely for use as a member class or interface in complex annotation interface declarations. It cannot be used to annotate anything directly: 

```kotlin
@Target({})
     public @interface MemberInterface {
         ...
     }
  
```

It is a compile-time error for a single `ElementType` constant to appear more than once in an `@Target` annotation. For example, the following `@Target` meta-annotation is illegal: 

```kotlin
@Target({ElementType.FIELD, ElementType.METHOD, ElementType.FIELD})
     public @interface Bogus {
         ...
     }
  
```

## Properties

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: Array<ElementType>
```

Returns an array of the kinds of elements an annotation interface can be applied to.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ElementType](ElementType.md)> | an array of the kinds of elements an annotation interface can be applied to |
