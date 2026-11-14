Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Class

```
class Class<T : Any!> : AnnotatedElement, GenericDeclaration, Serializable, Type, TypeDescriptor.OfField<Class<*>!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Class](../java/lang/Class.md) |

Instances of the class represent classes and interfaces in a running Java application. An enum class and a record class are kinds of class; an annotation interface is a kind of interface. Every array also belongs to a class that is reflected as a object that is shared by all arrays with the same element type and number of dimensions. The primitive Java types (`boolean`, `byte`, `char`, `short`, `int`, `long`, `float`, and `double`), and the keyword are also represented as objects.

`Class` has no public constructor. Instead a `Class` object is constructed automatically by the Java Virtual Machine when a class is derived from the bytes of a `class` file through the invocation of one of the following methods:

- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`

The methods of class `Class` expose many characteristics of a class or interface. Most characteristics are derived from the `class` file that the class loader passed to the Java Virtual Machine. A few characteristics are determined by the class loading environment at run time.

The following example uses a `Class` object to print the class name of an object:

```kotlin
void printClassName(Object obj) {
          System.out.println("The class of " + obj +
                             " is " + obj.getClass().getName());
      }
  
```
It is also possible to get the `Class` object for a named class or interface (or for `void`) using a *class literal* . For example: `System.out.println("The name of class Foo is: "+Foo.class.getName());`

Some methods of class `Class` expose whether the declaration of a class or interface in Java source code was *enclosed* within another declaration. Other methods describe how a class or interface is situated in a *nest* . A nest is a set of classes and interfaces, in the same run-time package, that allow mutual access to their `private` members. The classes and interfaces are known as *nestmates* . One nestmate acts as the *nest host* , and enumerates the other nestmates which belong to the nest; each of them in turn records it as the nest host. The classes and interfaces which belong to a nest, including its host, are determined when `class` files are generated, for example, a Java compiler will typically record a top-level class as the host of a nest where the other members are the classes and interfaces whose declarations are enclosed within the top-level class declaration.

Some methods of class `Class` expose whether the declaration of a class or interface in Java source code was *enclosed* within another declaration. Other methods describe how a class or interface is situated in a *nest* . A nest is a set of classes and interfaces, in the same run-time package, that allow mutual access to their `private` members. The classes and interfaces are known as *nestmates* . One nestmate acts as the *nest host* , and enumerates the other nestmates which belong to the nest; each of them in turn records it as the nest host. The classes and interfaces which belong to a nest, including its host, are determined when `class` files are generated, for example, a Java compiler will typically record a top-level class as the host of a nest where the other members are the classes and interfaces whose declarations are enclosed within the top-level class declaration.

## Summary

| Public methods ||
|---|---|
| [Class](../java/lang/Class.md)\<\*\> | `https://developer.android.com/reference/kotlin/java/lang/Class#arrayType()()` Returns a `Class` for an array type whose component type is described by this [Class](../java/lang/Class.md). |
| [Class](../java/lang/Class.md)\<out U\> | `https://developer.android.com/reference/kotlin/java/lang/Class#asSubclass(java.lang.Class)(clazz: https://developer.android.com/reference/kotlin/java/lang/Class#<U>)` Casts this `Class` object to represent a subclass of the class represented by the specified class object. |
| T? | `https://developer.android.com/reference/kotlin/java/lang/Class#cast(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Casts an object to the class or interface represented by this `Class` object. |
| --- | --- |
| [Class](../java/lang/Class.md)\<\*\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#componentType()()` Returns the component type of this `Class`, if it describes an array type, or `null` otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#descriptorString()()` Returns the descriptor string of the entity (class, interface, array class, primitive type, or `void`) represented by this `Class` object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#desiredAssertionStatus()()` Returns the assertion status that would be assigned to this class if it were to be initialized at the time this method is invoked. |
| --- | --- |
| static [Class](../java/lang/Class.md)\<\*\> | `https://developer.android.com/reference/kotlin/java/lang/Class#forName(kotlin.String)(className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the `Class` object associated with the class or interface with the given string name. |
| static [Class](../java/lang/Class.md)\<\*\> | `https://developer.android.com/reference/kotlin/java/lang/Class#forName(kotlin.String,%20kotlin.Boolean,%20java.lang.ClassLoader)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, initialize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader?)` Returns the `Class` object associated with the class or interface with the given string name, using the given class loader. |
| A? | `https://developer.android.com/reference/kotlin/java/lang/Class#getAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class#<A>)` Returns this element's annotation for the specified type if such an annotation is *present*, else null. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getAnnotations()()` Returns annotations that are *present* on this element. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class#<A>)` Returns annotations that are *associated* with this element. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getCanonicalName()()` Returns the canonical name of the underlying class as defined by The Java Language Specification. |
| --- | --- |
| [ClassLoader](../java/lang/ClassLoader.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getClassLoader()()` Returns the class loader for the class. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getClasses()()` Returns an array containing `Class` objects representing all the public classes and interfaces that are members of the class represented by this `Class` object. |
| [Class](../java/lang/Class.md)\<\*\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getComponentType()()` Returns the `Class` representing the component type of an array. |
| --- | --- |
| [Constructor](../java/lang/reflect/Constructor.md)\<T\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getConstructor(java.lang.Class)(vararg parameterTypes: https://developer.android.com/reference/kotlin/java/lang/Class#<*>!)` Returns a `Constructor` object that reflects the specified public constructor of the class represented by this `Class` object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Constructor](../java/lang/reflect/Constructor.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getConstructors()()` Returns an array containing `Constructor` objects reflecting all the public constructors of the class represented by this `Class` object. |
| A? | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class#<A>)` Returns this element's annotation for the specified type if such an annotation is *directly present*, else null. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredAnnotations()()` Returns annotations that are *directly present* on this element. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class#<A>)` Returns this element's annotation(s) for the specified type if such annotations are either *directly present* or *indirectly present*. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredClasses()()` Returns an array of `Class` objects reflecting all the classes and interfaces declared as members of the class represented by this `Class` object. |
| --- | --- |
| [Constructor](../java/lang/reflect/Constructor.md)\<T\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredConstructor(java.lang.Class)(vararg parameterTypes: https://developer.android.com/reference/kotlin/java/lang/Class#<*>!)` Returns a `Constructor` object that reflects the specified constructor of the class or interface represented by this `Class` object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Constructor](../java/lang/reflect/Constructor.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredConstructors()()` Returns an array of `Constructor` objects reflecting all the constructors declared by the class represented by this `Class` object. |
| [Field](../java/lang/reflect/Field.md) | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredField(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a `Field` object that reflects the specified declared field of the class or interface represented by this `Class` object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Field](../java/lang/reflect/Field.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredFields()()` Returns an array of `Field` objects reflecting all the fields declared by the class or interface represented by this `Class` object. |
| [Method](../java/lang/reflect/Method.md) | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredMethod(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, vararg parameterTypes: https://developer.android.com/reference/kotlin/java/lang/Class#<*>!)` Returns a `Method` object that reflects the specified declared method of the class or interface represented by this `Class` object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Method](../java/lang/reflect/Method.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredMethods()()` Returns an array containing `Method` objects reflecting all the declared methods of the class or interface represented by this `Class` object, including public, protected, default (package) access, and private methods, but excluding inherited methods. |
| --- | --- |
| [Class](../java/lang/Class.md)\<\*\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaringClass()()` If the class or interface represented by this `Class` object is a member of another class, returns the `Class` object representing the class in which it was declared. |
| [Class](../java/lang/Class.md)\<\*\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getEnclosingClass()()` Returns the immediately enclosing class of the underlying class. |
| [Constructor](../java/lang/reflect/Constructor.md)\<\*\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getEnclosingConstructor()()` If this `Class` object represents a local or anonymous class within a constructor, returns a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object representing the immediately enclosing constructor of the underlying class. |
| --- | --- |
| [Method](../java/lang/reflect/Method.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getEnclosingMethod()()` If this `Class` object represents a local or anonymous class within a method, returns a `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` object representing the immediately enclosing method of the underlying class. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getEnumConstants()()` Returns the elements of this enum class or null if this Class object does not represent an enum class. |
| [Field](../java/lang/reflect/Field.md) | `https://developer.android.com/reference/kotlin/java/lang/Class#getField(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a `Field` object that reflects the specified public member field of the class or interface represented by this `Class` object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Field](../java/lang/reflect/Field.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getFields()()` Returns an array containing `Field` objects reflecting all the accessible public fields of the class or interface represented by this `Class` object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getGenericInterfaces()()` Returns the `Type`s representing the interfaces directly implemented by the class or interface represented by this `Class` object. |
| [Type](../java/lang/reflect/Type.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getGenericSuperclass()()` Returns the `Type` representing the direct superclass of the entity (class, interface, primitive type or void) represented by this `Class` object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getInterfaces()()` Returns the interfaces directly implemented by the class or interface represented by this object. |
| [Method](../java/lang/reflect/Method.md) | `https://developer.android.com/reference/kotlin/java/lang/Class#getMethod(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, vararg parameterTypes: https://developer.android.com/reference/kotlin/java/lang/Class#<*>!)` Returns a `Method` object that reflects the specified public member method of the class or interface represented by this `Class` object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Method](../java/lang/reflect/Method.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getMethods()()` Returns an array containing `Method` objects reflecting all the public methods of the class or interface represented by this `Class` object, including those declared by the class or interface and those inherited from superclasses and superinterfaces. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#getModifiers()()` Returns the Java language modifiers for this class or interface, encoded in an integer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#getName()()` Returns the name of the entity (class, interface, array class, primitive type, or void) represented by this `Class` object. |
| [Class](../java/lang/Class.md)\<\*\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getNestHost()()` Returns the nest host of the [nest](../java/lang/Class.md) to which the class or interface represented by this `Class` object belongs. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getNestMembers()()` Returns an array containing `Class` objects representing all the classes and interfaces that are members of the nest to which the class or interface represented by this `Class` object belongs. |
| [Package](../java/lang/Package.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getPackage()()` Gets the package of this class. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#getPackageName()()` Returns the fully qualified package name. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getPermittedSubclasses()()` Returns an array containing `Class` objects representing the direct subinterfaces or subclasses permitted to extend or implement this class or interface if it is sealed. |
| [ProtectionDomain](../java/security/ProtectionDomain.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getProtectionDomain()()` Returns the `ProtectionDomain` of this class. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RecordComponent](../java/lang/reflect/RecordComponent.md)!\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getRecordComponents()()` Returns an array of `RecordComponent` objects representing all the record components of this record class, or `null` if this class is not a record class. |
| --- | --- |
| [URL](../java/net/URL.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getResource(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Finds a resource with a given name. |
| [InputStream](../java/io/InputStream.md)? | `https://developer.android.com/reference/kotlin/java/lang/Class#getResourceAsStream(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Finds a resource with a given name. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getSigners()()` Gets the signers of this class. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#getSimpleName()()` Returns the simple name of the underlying class as given in the source code. |
| [Class](../java/lang/Class.md)\<in T\>? | `https://developer.android.com/reference/kotlin/java/lang/Class#getSuperclass()()` Returns the `Class` representing the direct superclass of the entity (class, interface, primitive type or void) represented by this `Class`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#getTypeName()()` Return an informative string for the name of this class or interface. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TypeVariable](../java/lang/reflect/TypeVariable.md)\< [Class](../java/lang/Class.md)\<T\>!\>!\> | `https://developer.android.com/reference/kotlin/java/lang/Class#getTypeParameters()()` Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isAnnotation()()` Returns true if this `Class` object represents an annotation interface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isAnnotationPresent(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class#<out https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>)` Returns true if an annotation for the specified type is *present* on this element, else false. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isAnonymousClass()()` Returns `true` if and only if the underlying class is an anonymous class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isArray()()` Determines if this `Class` object represents an array class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isAssignableFrom(java.lang.Class)(cls: https://developer.android.com/reference/kotlin/java/lang/Class#<*>)` Determines if the class or interface represented by this `Class` object is either the same as, or is a superclass or superinterface of, the class or interface represented by the specified `Class` parameter. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isEnum()()` Returns true if and only if this class was declared as an enum in the source code. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isInstance(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Determines if the specified `Object` is assignment-compatible with the object represented by this `Class`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isInterface()()` Determines if this `Class` object represents an interface type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isLocalClass()()` Returns `true` if and only if the underlying class is a local class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isMemberClass()()` Returns `true` if and only if the underlying class is a member class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isNestmateOf(java.lang.Class)(c: https://developer.android.com/reference/kotlin/java/lang/Class#<*>)` Determines if the given `Class` is a nestmate of the class or interface represented by this `Class` object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isPrimitive()()` Determines if the specified `Class` object represents a primitive type. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isRecord()()` Returns `true` if and only if this class is a record class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isSealed()()` Returns `true` if and only if this `Class` object represents a sealed class or interface. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#isSynthetic()()` {@return {@code true} if and only if this class has the synthetic modifier \* bit set} |
| T | `https://developer.android.com/reference/kotlin/java/lang/Class#newInstance()()` Creates a new instance of the class represented by this `Class` object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#toGenericString()()` Returns a string describing this `Class`, including information about modifiers and type parameters. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Class#toString()()` Converts the object to a string. |

## Public methods

### arrayType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun arrayType(): Class<*>
```

Returns a `Class` for an array type whose component type is described by this [Class](../java/lang/Class.md).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>` | a `Class` describing the array type |

### asSubclass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <U : Any!> asSubclass(clazz: Class<U>): Class<out U>
```

Casts this `Class` object to represent a subclass of the class represented by the specified class object. Checks that the cast is valid, and throws a `ClassCastException` if it is not. If this method succeeds, it always returns a reference to this `Class` object.

This method is useful when a client needs to "narrow" the type of a `Class` object to pass it to an API that restricts the `Class` objects that it is willing to accept. A cast would generate a compile-time warning, as the correctness of the cast could not be checked at runtime (because generic types are implemented by erasure).

| Parameters ||
|---|---|
| `<U>` | the type to cast this `Class` object to |
| `clazz` | [Class](../java/lang/Class.md)\<U\>: the class of the type to cast this `Class` object to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<out U>` | this `Class` object, cast to represent a subclass of the specified class object. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if this `Class` object does not represent a subclass of the specified class (here "subclass" includes the class itself). |

### cast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cast(obj: Any?): T?
```

Casts an object to the class or interface represented by this `Class` object.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the object to be cast |

| Return ||
|---|---|
| `T?` | the object after casting, or null if obj is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the object is not null and is not assignable to the type T. |

### componentType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun componentType(): Class<*>?
```

Returns the component type of this `Class`, if it describes an array type, or `null` otherwise.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>?` | a `Class` describing the component type, or `null` if this `Class` does not describe an array type |

### descriptorString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun descriptorString(): String
```

Returns the descriptor string of the entity (class, interface, array class, primitive type, or `void`) represented by this `Class` object.

If this `Class` object represents a class or interface, not an array class, then:

- The result is a field descriptor (JVMS {@jvms 4.3.2}) for the class or interface.

If this `Class` object represents an array class, then the result is a string consisting of one or more '`[`' characters representing the depth of the array nesting, followed by the descriptor string of the element type.

- This array class can be described nominally.

If this `Class` object represents a primitive type or `void`, then the result is a field descriptor string which is a one-letter code corresponding to a primitive type or `void` (`"B", "C", "D", "F", "I", "J", "S", "Z", "V"`) (JVMS {@jvms 4.3.2}).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the descriptor string for this `Class` object |

### desiredAssertionStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun desiredAssertionStatus(): Boolean
```

Returns the assertion status that would be assigned to this class if it were to be initialized at the time this method is invoked. If this class has had its assertion status set, the most recent setting will be returned; otherwise, if any package default assertion status pertains to this class, the most recent setting for the most specific pertinent package default assertion status is returned; otherwise, if this class is not a system class (i.e., it has a class loader) its class loader's default assertion status is returned; otherwise, the system class default assertion status is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the desired assertion status of the specified class. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#setClassAssertionStatus(kotlin.String,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#setPackageAssertionStatus(kotlin.String,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#setDefaultAssertionStatus(kotlin.Boolean)`

### forName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forName(className: String): Class<*>
```

Returns the `Class` object associated with the class or interface with the given string name. Invoking this method is equivalent to: `Class.forName(className, true, currentLoader)` where `currentLoader` denotes the defining class loader of the current class.

For example, the following code fragment returns the runtime `Class` descriptor for the class named `java.lang.Thread`:
`Class t = Class.forName("java.lang.Thread")`

A call to `forName("X")` causes the class named `X` to be initialized.

| Parameters ||
|---|---|
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the fully qualified name of the desired class. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>` | the `Class` object for the class with the specified name. |

| Exceptions ||
|---|---|
| `java.lang.ClassNotFoundException` | if the class cannot be located |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails |
| `java.lang.LinkageError` | if the linkage fails |
| --- | --- |

### forName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forName(
    name: String, 
    initialize: Boolean, 
    loader: ClassLoader?
): Class<*>
```

Returns the `Class` object associated with the class or interface with the given string name, using the given class loader. Given the fully qualified name for a class or interface (in the same format returned by `getName`) this method attempts to locate and load the class or interface. The specified class loader is used to load the class or interface. If the parameter `loader` is null, the class is loaded through the bootstrap class loader. The class is initialized only if the `initialize` parameter is `true` and if it has not been initialized earlier.

If `name` denotes a primitive type or void, an attempt will be made to locate a user-defined class in the unnamed package whose name is `name`. Therefore, this method cannot be used to obtain any of the `Class` objects representing primitive types or void.

If `name` denotes an array class, the component type of the array class is loaded but not initialized.

For example, in an instance method the expression:
`Class.forName("Foo")` is equivalent to: `Class.forName("Foo", true, this.getClass().getClassLoader())` Note that this method throws errors related to loading, linking or initializing as specified in Sections {@jls 12.2}, {@jls \* 12.3}, and {@jls 12.4} of The Java Language Specification. Note that this method does not check whether the requested class is accessible to its caller.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): fully qualified name of the desired class |
| `initialize` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` the class will be initialized (which implies linking). See Section {@jls \* 12.4} of The Java Language Specification. |
| `loader` | [ClassLoader](../java/lang/ClassLoader.md)?: class loader from which the class must be loaded |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>` | class object representing the desired class |

| Exceptions ||
|---|---|
| `java.lang.ClassNotFoundException` | if the class cannot be located by the specified class loader |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails |
| `java.lang.LinkageError` | if the linkage fails |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Class#forName(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader`

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Annotation!> getAnnotation(annotationClass: Class<A>): A?
```

Returns this element's annotation for the specified type if such an annotation is *present*, else null.

Note that any annotation returned by this method is a declaration annotation.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `A?` | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAnnotations(): Array<Annotation!>
```

Returns annotations that are *present* on this element. If there are no annotations *present* on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | annotations present on this element |

### getAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Annotation!> getAnnotationsByType(annotationClass: Class<A>): Array<A>
```

Returns annotations that are *associated* with this element. If there are no annotations *associated* with this element, the return value is an array of length 0. The difference between this method and `https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement#getAnnotation(java.lang.Class)` is that this method detects if its argument is a *repeatable annotation type* (JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<A>` | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getCanonicalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCanonicalName(): String?
```

Returns the canonical name of the underlying class as defined by The Java Language Specification. Returns `null` if the underlying class does not have a canonical name. Classes without canonical names include:

- a [local class](../java/lang/Class.md))
- a [anonymous class](../java/lang/Class.md))
- an array whose component type does not have a canonical name

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the canonical name of the underlying class if it exists, and `null` otherwise. |

### getClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClassLoader(): ClassLoader?
```

Returns the class loader for the class. Some implementations may use null to represent the bootstrap class loader. This method will return null in such implementations if this class was loaded by the bootstrap class loader.

If this `Class` object represents a primitive type or void, null is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/ClassLoader?` | the class loader that loaded the class or interface represented by this `Class` object. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader`
- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`

### getClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClasses(): Array<Class<*>!>
```

Returns an array containing `Class` objects representing all the public classes and interfaces that are members of the class represented by this `Class` object. This includes public class and interface members inherited from superclasses and public class and interface members declared by the class. This method returns an array of length 0 if this `Class` object has no public member classes or interfaces. This method also returns an array of length 0 if this `Class` object represents a primitive type, an array class, or void.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class#<*>!>` | the array of `Class` objects representing the public members of this class |

### getComponentType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponentType(): Class<*>?
```

Returns the `Class` representing the component type of an array. If this class does not represent an array class this method returns null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>?` | the `Class` representing the component type of this class if this class is an array |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/reflect/Array`

### getConstructor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConstructor(vararg parameterTypes: Class<*>!): Constructor<T>
```

Returns a `Constructor` object that reflects the specified public constructor of the class represented by this `Class` object. The `parameterTypes` parameter is an array of `Class` objects that identify the constructor's formal parameter types, in declared order. If this `Class` object represents an inner class declared in a non-static context, the formal parameter types include the explicit enclosing instance as the first parameter.

The constructor to reflect is the public constructor of the class represented by this `Class` object whose formal parameter types match those specified by `parameterTypes`.

| Parameters ||
|---|---|
| `parameterTypes` | [Class](../java/lang/Class.md)\<\*\>!: the parameter array |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor<T>` | the `Constructor` object of the public constructor that matches the specified `parameterTypes` |

| Exceptions ||
|---|---|
| `java.lang.NoSuchMethodException` | if a matching method is not found. |
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |

### getConstructors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConstructors(): Array<Constructor<*>!>
```

Returns an array containing `Constructor` objects reflecting all the public constructors of the class represented by this `Class` object. An array of length 0 is returned if the class has no public constructors, or if the class is an array class, or if the class reflects a primitive type or void.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor<*>!>` | the array of `Constructor` objects representing the public constructors of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |

### getDeclaredAnnotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Annotation!> getDeclaredAnnotation(annotationClass: Class<A>): A?
```

Returns this element's annotation for the specified type if such an annotation is *directly present*, else null. This method ignores inherited annotations. (Returns null if no annotations are directly present on this element.)

Note that any annotation returned by this method is a declaration annotation.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if directly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `A?` | this element's annotation for the specified annotation type if directly present on this element, else null |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are *directly present* on this element. This method ignores inherited annotations. If there are no annotations *directly present* on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | annotations directly present on this element |

### getDeclaredAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <A : Annotation!> getDeclaredAnnotationsByType(annotationClass: Class<A>): Array<A>
```

Returns this element's annotation(s) for the specified type if such annotations are either *directly present* or *indirectly present* . This method ignores inherited annotations. If there are no specified annotations directly or indirectly present on this element, the return value is an array of length 0. The difference between this method and `https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement#getDeclaredAnnotation(java.lang.Class)` is that this method detects if its argument is a *repeatable annotation type* (JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation if one is present. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if directly or indirectly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<A>` | all this element's annotations for the specified annotation type if directly or indirectly present on this element, else an array of length zero |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredClasses(): Array<Class<*>!>
```

Returns an array of `Class` objects reflecting all the classes and interfaces declared as members of the class represented by this `Class` object. This includes public, protected, default (package) access, and private classes and interfaces declared by the class, but excludes inherited classes and interfaces. This method returns an array of length 0 if the class declares no classes or interfaces as members, or if this `Class` object represents a primitive type, an array class, or void.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class#<*>!>` | the array of `Class` objects representing all the declared members of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared classes within this class - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

### getDeclaredConstructor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredConstructor(vararg parameterTypes: Class<*>!): Constructor<T>
```

Returns a `Constructor` object that reflects the specified constructor of the class or interface represented by this `Class` object. The `parameterTypes` parameter is an array of `Class` objects that identify the constructor's formal parameter types, in declared order. If this `Class` object represents an inner class declared in a non-static context, the formal parameter types include the explicit enclosing instance as the first parameter.

| Parameters ||
|---|---|
| `parameterTypes` | [Class](../java/lang/Class.md)\<\*\>!: the parameter array |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor<T>` | The `Constructor` object for the constructor with the specified parameter list |

| Exceptions ||
|---|---|
| `java.lang.NoSuchMethodException` | if a matching method is not found. |
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared constructor - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

### getDeclaredConstructors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredConstructors(): Array<Constructor<*>!>
```

Returns an array of `Constructor` objects reflecting all the constructors declared by the class represented by this `Class` object. These are public, protected, default (package) access, and private constructors. The elements in the array returned are not sorted and are not in any particular order. If the class has a default constructor, it is included in the returned array. This method returns an array of length 0 if this `Class` object represents an interface, a primitive type, an array class, or void.

See The Java Language Specification, section {@jls 8.2}.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor<*>!>` | the array of `Constructor` objects representing all the declared constructors of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared constructors within this class - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

### getDeclaredField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredField(name: String): Field
```

Returns a `Field` object that reflects the specified declared field of the class or interface represented by this `Class` object. The `name` parameter is a `String` that specifies the simple name of the desired field.

If this `Class` object represents an array type, then this method does not find the `length` field of the array type.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the field |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Field` | the `Field` object for the specified field in this class |

| Exceptions ||
|---|---|
| `java.lang.NoSuchFieldException` | if a field with the specified name is not found. |
| `java.lang.NullPointerException` | if `name` is `null` |
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared field - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |
| --- | --- |

### getDeclaredFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredFields(): Array<Field!>
```

Returns an array of `Field` objects reflecting all the fields declared by the class or interface represented by this `Class` object. This includes public, protected, default (package) access, and private fields, but excludes inherited fields.

If this `Class` object represents a class or interface with no declared fields, then this method returns an array of length 0.

If this `Class` object represents an array type, a primitive type, or void, then this method returns an array of length 0.

The elements in the returned array are not sorted and are not in any particular order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Field!>` | the array of `Field` objects representing all the declared fields of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared fields within this class - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

### getDeclaredMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredMethod(
    name: String, 
    vararg parameterTypes: Class<*>!
): Method
```

Returns a `Method` object that reflects the specified declared method of the class or interface represented by this `Class` object. The `name` parameter is a `String` that specifies the simple name of the desired method, and the `parameterTypes` parameter is an array of `Class` objects that identify the method's formal parameter types, in declared order. If more than one method with the same parameter types is declared in a class, and one of these methods has a return type that is more specific than any of the others, that method is returned; otherwise one of the methods is chosen arbitrarily. If the name is "\<init\>"or "\<clinit\>" a `NoSuchMethodException` is raised.

If this `Class` object represents an array type, then this method does not find the `clone()` method.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the method |
| `parameterTypes` | [Class](../java/lang/Class.md)\<\*\>!: the parameter array |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` | the `Method` object for the method of this class matching the specified name and parameters |

| Exceptions ||
|---|---|
| `java.lang.NoSuchMethodException` | if a matching method is not found. |
| `java.lang.NullPointerException` | if `name` is `null` |
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared method - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |
| --- | --- |

### getDeclaredMethods

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaredMethods(): Array<Method!>
```

Returns an array containing `Method` objects reflecting all the declared methods of the class or interface represented by this `Class` object, including public, protected, default (package) access, and private methods, but excluding inherited methods. The declared methods may include methods *not* in the source of the class or interface, including [bridge methods](../java/lang/reflect/Method.md)) and other [synthetic](../java/lang/reflect/Executable.md)) methods added by compilers.

If this `Class` object represents a class or interface that has multiple declared methods with the same name and parameter types, but different return types, then the returned array has a `Method` object for each such method.

If this `Class` object represents a class or interface that has a class initialization method `<clinit>`, then the returned array does *not* have a corresponding `Method` object.

If this `Class` object represents a class or interface with no declared methods, then the returned array has length 0.

If this `Class` object represents an array type, a primitive type, or void, then the returned array has length 0.

The elements in the returned array are not sorted and are not in any particular order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Method!>` | the array of `Method` objects representing all the declared methods of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared methods within this class - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

**See Also**

### getDeclaringClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaringClass(): Class<*>?
```

If the class or interface represented by this `Class` object is a member of another class, returns the `Class` object representing the class in which it was declared. This method returns null if this class or interface is not a member of any other class. If this `Class` object represents an array class, a primitive type, or void,then this method returns null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>?` | the declaring class for this class |

### getEnclosingClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnclosingClass(): Class<*>?
```

Returns the immediately enclosing class of the underlying class. If the underlying class is a top level class this method returns `null`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>?` | the immediately enclosing class of the underlying class |

### getEnclosingConstructor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnclosingConstructor(): Constructor<*>?
```

If this `Class` object represents a local or anonymous class within a constructor, returns a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object representing the immediately enclosing constructor of the underlying class. Returns `null` otherwise. In particular, this method returns `null` if the underlying class is a local or anonymous class immediately enclosed by a class or interface declaration, instance initializer or static initializer.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor<*>?` | the immediately enclosing constructor of the underlying class, if that class is a local or anonymous class; otherwise `null`. |

### getEnclosingMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnclosingMethod(): Method?
```

If this `Class` object represents a local or anonymous class within a method, returns a `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` object representing the immediately enclosing method of the underlying class. Returns `null` otherwise. In particular, this method returns `null` if the underlying class is a local or anonymous class immediately enclosed by a class or interface declaration, instance initializer or static initializer.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Method?` | the immediately enclosing method of the underlying class, if that class is a local or anonymous class; otherwise `null`. |

### getEnumConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnumConstants(): Array<T>?
```

Returns the elements of this enum class or null if this Class object does not represent an enum class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | an array containing the values comprising the enum class represented by this `Class` object in the order they're declared, or null if this `Class` object does not represent an enum class |

### getField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getField(name: String): Field
```

Returns a `Field` object that reflects the specified public member field of the class or interface represented by this `Class` object. The `name` parameter is a `String` specifying the simple name of the desired field.

The field to be reflected is determined by the algorithm that follows. Let C be the class or interface represented by this `Class` object:

1. If C declares a public field with the name specified, that is the field to be reflected.
2. If no field was found in step 1 above, this algorithm is applied recursively to each direct superinterface of C. The direct superinterfaces are searched in the order they were declared.
3. If no field was found in steps 1 and 2 above, and C has a superclass S, then this algorithm is invoked recursively upon S. If C has no superclass, then a `NoSuchFieldException` is thrown.

If this `Class` object represents an array type, then this method does not find the `length` field of the array type.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the field name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Field` | the `Field` object of this class specified by `name` |

| Exceptions ||
|---|---|
| `java.lang.NoSuchFieldException` | if a field with the specified name is not found. |
| `java.lang.NullPointerException` | if `name` is `null` |
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |
| --- | --- |

### getFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFields(): Array<Field!>
```

Returns an array containing `Field` objects reflecting all the accessible public fields of the class or interface represented by this `Class` object.

If this `Class` object represents a class or interface with no accessible public fields, then this method returns an array of length 0.

If this `Class` object represents a class, then this method returns the public fields of the class and of all its superclasses and superinterfaces.

If this `Class` object represents an interface, then this method returns the fields of the interface and of all its superinterfaces.

If this `Class` object represents an array type, a primitive type, or void, then this method returns an array of length 0.

The elements in the returned array are not sorted and are not in any particular order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Field!>` | the array of `Field` objects representing the public fields |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |

### getGenericInterfaces

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGenericInterfaces(): Array<Type!>
```

Returns the `Type`s representing the interfaces directly implemented by the class or interface represented by this `Class` object.

If a superinterface is a parameterized type, the `Type` object returned for it must accurately reflect the actual type arguments used in the source code. The parameterized type representing each superinterface is created if it had not been created before. See the declaration of `https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType` for the semantics of the creation process for parameterized types.

If this `Class` object represents a class, the return value is an array containing objects representing all interfaces directly implemented by the class. The order of the interface objects in the array corresponds to the order of the interface names in the `implements` clause of the declaration of the class represented by this `Class` object.

If this `Class` object represents an interface, the array contains objects representing all interfaces directly extended by the interface. The order of the interface objects in the array corresponds to the order of the interface names in the `extends` clause of the declaration of the interface represented by this `Class` object.

If this `Class` object represents a class or interface that implements no interfaces, the method returns an array of length 0.

If this `Class` object represents a primitive type or void, the method returns an array of length 0.

If this `Class` object represents an array type, the interfaces `Cloneable` and `java.io.Serializable` are returned in that order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Type!>` | an array of interfaces directly implemented by this class |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if any of the generic superinterfaces refers to a non-existent type declaration |
| `java.lang.reflect.GenericSignatureFormatError` | if the generic class signature does not conform to the format specified in section {@jvms 4.7.9} of The Java Virtual Machine Specification |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the generic superinterfaces refer to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getGenericSuperclass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGenericSuperclass(): Type?
```

Returns the `Type` representing the direct superclass of the entity (class, interface, primitive type or void) represented by this `Class` object.

If the superclass is a parameterized type, the `Type` object returned must accurately reflect the actual type arguments used in the source code. The parameterized type representing the superclass is created if it had not been created before. See the declaration of `https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType` for the semantics of the creation process for parameterized types. If this `Class` object represents either the `Object` class, an interface, a primitive type, or void, then null is returned. If this `Class` object represents an array class then the `Class` object representing the `Object` class is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Type?` | the direct superclass of the class represented by this `Class` object |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if the generic superclass refers to a non-existent type declaration |
| `java.lang.reflect.GenericSignatureFormatError` | if the generic class signature does not conform to the format specified in section {@jvms 4.7.9} of The Java Virtual Machine Specification |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the generic superclass refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getInterfaces

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInterfaces(): Array<Class<*>!>
```

Returns the interfaces directly implemented by the class or interface represented by this object.

If this `Class` object represents a class, the return value is an array containing objects representing all interfaces directly implemented by the class. The order of the interface objects in the array corresponds to the order of the interface names in the `implements` clause of the declaration of the class represented by this `Class` object. For example, given the declaration:
`class Shimmer implements FloorWax, DessertTopping { ... }` suppose the value of `s` is an instance of `Shimmer`; the value of the expression: `s.getClass().getInterfaces()[0]` is the `Class` object that represents interface `FloorWax`; and the value of: `s.getClass().getInterfaces()[1]` is the `Class` object that represents interface `DessertTopping`.

If this `Class` object represents an interface, the array contains objects representing all interfaces directly extended by the interface. The order of the interface objects in the array corresponds to the order of the interface names in the `extends` clause of the declaration of the interface represented by this `Class` object.

If this `Class` object represents a class or interface that implements no interfaces, the method returns an array of length 0.

If this `Class` object represents a primitive type or void, the method returns an array of length 0.

If this `Class` object represents an array type, the interfaces `Cloneable` and `java.io.Serializable` are returned in that order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class#<*>!>` | an array of interfaces directly implemented by this class |

### getMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMethod(
    name: String, 
    vararg parameterTypes: Class<*>!
): Method
```

Returns a `Method` object that reflects the specified public member method of the class or interface represented by this `Class` object. The `name` parameter is a `String` specifying the simple name of the desired method. The `parameterTypes` parameter is an array of `Class` objects that identify the method's formal parameter types, in declared order. If `parameterTypes` is `null`, it is treated as if it were an empty array.

If this `Class` object represents an array type, then this method finds any public method inherited by the array type from `Object` except method `clone()`.

If this `Class` object represents an interface then this method does not find any implicitly declared method from `Object`. Therefore, if no methods are explicitly declared in this interface or any of its superinterfaces, then this method does not find any method.

This method does not find any method with name "`<init>`" or "`<clinit>`".

Generally, the method to be reflected is determined by the 4 step algorithm that follows. Let C be the class or interface represented by this `Class` object:

1. A union of methods is composed of:
 1. C's declared public instance and static methods as returned by `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredMethods()` and filtered to include only public methods that match given `name` and `parameterTypes`
 2. If C is a class other than `Object`, then include the result of invoking this algorithm recursively on the superclass of C.
 3. Include the results of invoking this algorithm recursively on all direct superinterfaces of C, but include only instance methods.
2. This union is partitioned into subsets of methods with same return type (the selection of methods from step 1 also guarantees that they have the same method name and parameter types).
3. Within each such subset only the most specific methods are selected. Let method M be a method from a set of methods with same VM signature (return type, name, parameter types). M is most specific if there is no such method N != M from the same set, such that N is more specific than M. N is more specific than M if:
 1. N is declared by a class and M is declared by an interface; or
 2. N and M are both declared by classes or both by interfaces and N's declaring type is the same as or a subtype of M's declaring type (clearly, if M's and N's declaring types are the same type, then M and N are the same method).
4. The result of this algorithm is chosen arbitrarily from the methods with most specific return type among all selected methods from step 3. Let R be a return type of a method M from the set of all selected methods from step 3. M is a method with most specific return type if there is no such method N != M from the same set, having return type S != R, such that S is a subtype of R as determined by R.class.`https://developer.android.com/reference/kotlin/java/lang/Class#isAssignableFrom(java.lang.Class)`(S.class).

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the method |
| `parameterTypes` | [Class](../java/lang/Class.md)\<\*\>!: the list of parameters |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` | the `Method` object that matches the specified `name` and `parameterTypes` |

| Exceptions ||
|---|---|
| `java.lang.NoSuchMethodException` | if a matching method is not found or if the name is "\<init\>"or "\<clinit\>". |
| `java.lang.NullPointerException` | if `name` is `null` |
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |
| --- | --- |

### getMethods

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMethods(): Array<Method!>
```

Returns an array containing `Method` objects reflecting all the public methods of the class or interface represented by this `Class` object, including those declared by the class or interface and those inherited from superclasses and superinterfaces.

If this `Class` object represents an array type, then the returned array has a `Method` object for each of the public methods inherited by the array type from `Object`. It does not contain a `Method` object for `clone()`.

If this `Class` object represents an interface then the returned array does not contain any implicitly declared methods from `Object`. Therefore, if no methods are explicitly declared in this interface or any of its superinterfaces then the returned array has length 0. (Note that a `Class` object which represents a class always has public methods, inherited from `Object`.)

The returned array never contains methods with names "`<init>`" or "`<clinit>`".

The elements in the returned array are not sorted and are not in any particular order.

Generally, the result is computed as with the following 4 step algorithm. Let C be the class or interface represented by this `Class` object:

1. A union of methods is composed of:
 1. C's declared public instance and static methods as returned by `https://developer.android.com/reference/kotlin/java/lang/Class#getDeclaredMethods()` and filtered to include only public methods.
 2. If C is a class other than `Object`, then include the result of invoking this algorithm recursively on the superclass of C.
 3. Include the results of invoking this algorithm recursively on all direct superinterfaces of C, but include only instance methods.
2. Union from step 1 is partitioned into subsets of methods with same signature (name, parameter types) and return type.
3. Within each such subset only the most specific methods are selected. Let method M be a method from a set of methods with same signature and return type. M is most specific if there is no such method N != M from the same set, such that N is more specific than M. N is more specific than M if:
 1. N is declared by a class and M is declared by an interface; or
 2. N and M are both declared by classes or both by interfaces and N's declaring type is the same as or a subtype of M's declaring type (clearly, if M's and N's declaring types are the same type, then M and N are the same method).
4. The result of this algorithm is the union of all selected methods from step 3.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Method!>` | the array of `Method` objects representing the public methods of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class. |

### getModifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getModifiers(): Int
```

Returns the Java language modifiers for this class or interface, encoded in an integer. The modifiers consist of the Java Virtual Machine's constants for `public`, `protected`, `private`, `final`, `static`, `abstract` and `interface`; they should be decoded using the methods of class `Modifier`.

If the underlying class is an array class, then its `public`, `private` and `protected` modifiers are the same as those of its component type. If this `Class` object represents a primitive type or void, its `public` modifier is always `true`, and its `protected` and `private` modifiers are always `false`. If this `Class` object represents an array class, a primitive type or void, then its `final` modifier is always `true` and its interface modifier is always `false`. The values of its other modifiers are not determined by this specification.

The modifier encodings are defined in section {@jvms 4.1} of The Java Virtual Machine Specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the `int` representing the modifiers for this class |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/reflect/Modifier`

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Returns the name of the entity (class, interface, array class, primitive type, or void) represented by this `Class` object.

If this `Class` object represents a class or interface, not an array class, then:

If this `Class` object represents an array class, then the result is a string consisting of one or more '`[`' characters representing the depth of the array nesting, followed by the element type as encoded using the following table:

| Element Type | Encoding |
| --- | --- |
| `boolean` | `Z` |
| `byte` | `B` |
| `char` | `C` |
| --- | --- |
| class or interface with [binary name](../java/lang/ClassLoader.md) *N* | `L`*N* `;` |
| `double` | `D` |
| `float` | `F` |
| --- | --- |
| `int` | `I` |
| `long` | `J` |
| `short` | `S` |
|---|---|

If this `Class` object represents a primitive type or `void`, then the result is a string with the same spelling as the Java language keyword which corresponds to the primitive type or `void`.

Examples:

```kotlin
String.class.getName()
      returns "java.lang.String"
  byte.class.getName()
      returns "byte"
  (new Object[3]).getClass().getName()
      returns "[Ljava.lang.Object;"
  (new int[3][4][5][6][7][8][9]).getClass().getName()
      returns "[[[[[[[I"
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the name of the class, interface, or other entity represented by this `Class` object. |

### getNestHost

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNestHost(): Class<*>
```

Returns the nest host of the [nest](../java/lang/Class.md) to which the class or interface represented by this `Class` object belongs. Every class and interface belongs to exactly one nest. If the nest host of this class or interface has previously been determined, then this method returns the nest host. If the nest host of this class or interface has not previously been determined, then this method determines the nest host using the algorithm of JVMS 5.4.4, and returns it. Often, a class or interface belongs to a nest consisting only of itself, in which case this method returns `this` to indicate that the class or interface is the nest host.

If this `Class` object represents a primitive type, an array type, or `void`, then this method returns `this`, indicating that the represented entity belongs to the nest consisting only of itself, and is the nest host.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<*>` | the nest host of this class or interface |

### getNestMembers

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNestMembers(): Array<Class<*>!>
```

Returns an array containing `Class` objects representing all the classes and interfaces that are members of the nest to which the class or interface represented by this `Class` object belongs. First, this method obtains the [nest host](../java/lang/Class.md)), `H`, of the nest to which the class or interface represented by this `Class` object belongs. The zeroth element of the returned array is `H`. Then, for each class or interface `C` which is recorded by `H` as being a member of its nest, this method attempts to obtain the `Class` object for `C` (using [the defining class](../java/lang/Class.md)) of the current `Class` object), and then obtains the [nest host](../java/lang/Class.md)) of the nest to which `C` belongs. The classes and interfaces which are recorded by `H` as being members of its nest, and for which `H` can be determined as their nest host, are indicated by subsequent elements of the returned array. The order of such elements is unspecified. Duplicates are permitted.

If this `Class` object represents a primitive type, an array type, or `void`, then this method returns a single-element array containing `this`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class#<*>!>` | an array of all classes and interfaces in the same nest as this class or interface |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Class#getNestHost()`

### getPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackage(): Package?
```

Gets the package of this class.

If this class represents an array type, a primitive type or void, this method returns `null`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Package?` | the package of this class. |

### getPackageName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Returns the fully qualified package name.

If this class is a top level class, then this method returns the fully qualified name of the package that the class is a member of, or the empty string if the class is in an unnamed package.

If this class is a member class, then this method is equivalent to invoking `getPackageName()` on the [enclosing class](../java/lang/Class.md)).

If this class is a [local class](../java/lang/Class.md)) or an [anonymous class](../java/lang/Class.md)), then this method is equivalent to invoking `getPackageName()` on the [declaring class](../java/lang/Class.md)) of the [enclosing method](../java/lang/Class.md)) or [enclosing constructor](../java/lang/Class.md)).

If this class represents an array type then this method returns the package name of the element type. If this class represents a primitive type or void then the package name "`java.lang`" is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the fully qualified package name |

### getPermittedSubclasses

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPermittedSubclasses(): Array<Class<*>!>?
```

Returns an array containing `Class` objects representing the direct subinterfaces or subclasses permitted to extend or implement this class or interface if it is sealed. The order of such elements is unspecified. The array is empty if this sealed class or interface has no permitted subclass. If this `Class` object represents a primitive type, `void`, an array type, or a class or interface that is not sealed, that is `https://developer.android.com/reference/kotlin/java/lang/Class#isSealed()` returns `false`, then this method returns `null`. Conversely, if `https://developer.android.com/reference/kotlin/java/lang/Class#isSealed()` returns `true`, then this method returns a non-null value. For each class or interface `C` which is recorded as a permitted direct subinterface or subclass of this class or interface, this method attempts to obtain the `Class` object for `C` (using [the defining class](../java/lang/Class.md)) of the current `Class` object). The `Class` objects which can be obtained and which are direct subinterfaces or subclasses of this class or interface, are indicated by elements of the returned array. If a `Class` object cannot be obtained, it is silently ignored, and not included in the result array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class#<*>!>?` | an array of `Class` objects of the permitted subclasses of this class or interface, or `null` if this class or interface is not sealed. |

### getProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProtectionDomain(): ProtectionDomain?
```

Returns the `ProtectionDomain` of this class. If there is a security manager installed, this method first calls the security manager's `checkPermission` method with a `RuntimePermission("getProtectionDomain")` permission to ensure it's ok to get the `ProtectionDomain`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/ProtectionDomain.html#?` | the ProtectionDomain of this class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow getting the ProtectionDomain. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/ProtectionDomain.html#`
- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`

### getRecordComponents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRecordComponents(): Array<RecordComponent!>?
```

Returns an array of `RecordComponent` objects representing all the record components of this record class, or `null` if this class is not a record class.

The components are returned in the same order that they are declared in the record header. The array is empty if this record class has no components. If the class is not a record class, that is `https://developer.android.com/reference/kotlin/java/lang/Class#isRecord()` returns `false`, then this method returns `null`. Conversely, if `https://developer.android.com/reference/kotlin/java/lang/Class#isRecord()` returns `true`, then this method returns a non-null value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/RecordComponent!>?` | An array of `RecordComponent` objects representing all the record components of this record class, or `null` if this class is not a record class |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager, *s* , is present and any of the following conditions is met: - the caller's class loader is not the same as the class loader of this class and invocation of java.lang.SecurityManager#checkPermission method with `RuntimePermission("accessDeclaredMembers")` denies access to the declared methods within this class - the caller's class loader is not the same as or an ancestor of the class loader for the current class and invocation of `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String)` denies access to the package of this class |

### getResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResource(name: String): URL?
```

Finds a resource with a given name.

The rules for searching resources associated with a given class are implemented by the defining [class loader](../java/lang/ClassLoader.md) of the class. This method delegates to this `Class` object's class loader. If this `Class` object was loaded by the bootstrap class loader, the method delegates to `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#getSystemResource(kotlin.String)`.

Before delegation, an absolute resource name is constructed from the given resource name using this algorithm:

- If the `name` begins with a `'/'` (`'\u002f'`), then the absolute name of the resource is the portion of the `name` following the `'/'`.
- Otherwise, the absolute name is of the following form: `modified_package_name/name`

 Where the `modified_package_name` is the package name of this object with `'/'` substituted for `'.'` (`'\u002e'`).

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the desired resource |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URL.html#?` | A `https://developer.android.com/reference/kotlin/java/net/URL.html#` object; `null` if no resource with this name is found. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `name` is `null` |

### getResourceAsStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResourceAsStream(name: String): InputStream?
```

Finds a resource with a given name.

The rules for searching resources associated with a given class are implemented by the defining [class loader](../java/lang/ClassLoader.md) of the class. This method delegates to this `Class` object's class loader. If this `Class` object was loaded by the bootstrap class loader, the method delegates to `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#getSystemResourceAsStream(kotlin.String)`.

Before delegation, an absolute resource name is constructed from the given resource name using this algorithm:

- If the `name` begins with a `'/'` (`'\u002f'`), then the absolute name of the resource is the portion of the `name` following the `'/'`.
- Otherwise, the absolute name is of the following form: `modified_package_name/name`

 Where the `modified_package_name` is the package name of this object with `'/'` substituted for `'.'` (`'\u002e'`).

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the desired resource |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#?` | A `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` object; `null` if no resource with this name is found. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `name` is `null` |

### getSigners

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSigners(): Array<Any!>?
```

Gets the signers of this class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>?` | the signers of this class, or null if there are no signers. In particular, this method returns null if this `Class` object represents a primitive type or void. |

### getSimpleName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSimpleName(): String
```

Returns the simple name of the underlying class as given in the source code. An empty string is returned if the underlying class is [anonymous](../java/lang/Class.md)). A [synthetic class](../java/lang/Class.md)), one not present in source code, can have a non-empty name including special characters, such as "`$`".

The simple name of an [array class](../java/lang/Class.md)) is the simple name of the component type with "\[\]" appended. In particular the simple name of an array class whose component type is anonymous is "\[\]".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the simple name of the underlying class |

### getSuperclass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuperclass(): Class<in T>?
```

Returns the `Class` representing the direct superclass of the entity (class, interface, primitive type or void) represented by this `Class`. If this `Class` represents either the `Object` class, an interface, a primitive type, or void, then null is returned. If this `Class` object represents an array class then the `Class` object representing the `Object` class is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class#<in T>?` | the direct superclass of the class represented by this `Class` object |

### getTypeName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTypeName(): String
```

Return an informative string for the name of this class or interface.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | an informative string for the name of this class or interface |

### getTypeParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTypeParameters(): Array<TypeVariable<Class<T>!>!>
```

Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. Returns an array of length 0 if the underlying generic declaration declares no type variables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable<https://developer.android.com/reference/kotlin/java/lang/Class#<T>!>!>` | an array of `TypeVariable` objects that represent the type variables declared by this generic declaration |

| Exceptions ||
|---|---|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic signature of this generic declaration does not conform to the format specified in section {@jvms 4.7.9} of The Java Virtual Machine Specification |

### isAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAnnotation(): Boolean
```

Returns true if this `Class` object represents an annotation interface. Note that if this method returns true, `https://developer.android.com/reference/kotlin/java/lang/Class#isInterface()` would also return true, as all annotation interfaces are also interfaces.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `Class` object represents an annotation interface; `false` otherwise |

### isAnnotationPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAnnotationPresent(annotationClass: Class<out Annotation!>): Boolean
```

Returns true if an annotation for the specified type is *present* on this element, else false. This method is designed primarily for convenient access to marker annotations.

The truth value returned by this method is equivalent to: `getAnnotation(annotationClass) != null`

The body of the default method is specified to be the code above.

| Parameters ||
|---|---|
| `annotationClass` | [Class](../java/lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isAnonymousClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAnonymousClass(): Boolean
```

Returns `true` if and only if the underlying class is an anonymous class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if this class is an anonymous class. |

### isArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isArray(): Boolean
```

Determines if this `Class` object represents an array class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `Class` object represents an array class; `false` otherwise. |

### isAssignableFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAssignableFrom(cls: Class<*>): Boolean
```

Determines if the class or interface represented by this `Class` object is either the same as, or is a superclass or superinterface of, the class or interface represented by the specified `Class` parameter. It returns `true` if so; otherwise it returns `false`. If this `Class` object represents a primitive type, this method returns `true` if the specified `Class` parameter is exactly this `Class` object; otherwise it returns `false`.

Specifically, this method tests whether the type represented by the specified `Class` parameter can be converted to the type represented by this `Class` object via an identity conversion or via a widening reference conversion. See The Java Language Specification, sections {@jls 5.1.1} and {@jls 5.1.4}, for details.

| Parameters ||
|---|---|
| `cls` | [Class](../java/lang/Class.md)\<\*\>: the `Class` object to be checked |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the `boolean` value indicating whether objects of the type `cls` can be assigned to objects of this class |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified Class parameter is null. |

### isEnum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnum(): Boolean
```

Returns true if and only if this class was declared as an enum in the source code. Note that `https://developer.android.com/reference/kotlin/java/lang/Enum` is not itself an enum class. Also note that if an enum constant is declared with a class body, the class of that enum constant object is an anonymous class and *not* the class of the declaring enum class. The `https://developer.android.com/reference/kotlin/java/lang/Enum#getDeclaringClass()` method of an enum constant can be used to get the class of the enum class declaring the constant.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this class was declared as an enum in the source code |

### isInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInstance(obj: Any?): Boolean
```

Determines if the specified `Object` is assignment-compatible with the object represented by this `Class`. This method is the dynamic equivalent of the Java language `instanceof` operator. The method returns `true` if the specified `Object` argument is non-null and can be cast to the reference type represented by this `Class` object without raising a `ClassCastException.` It returns `false` otherwise.

Specifically, if this `Class` object represents a declared class, this method returns `true` if the specified `Object` argument is an instance of the represented class (or of any of its subclasses); it returns `false` otherwise. If this `Class` object represents an array class, this method returns `true` if the specified `Object` argument can be converted to an object of the array class by an identity conversion or by a widening reference conversion; it returns `false` otherwise. If this `Class` object represents an interface, this method returns `true` if the class or any superclass of the specified `Object` argument implements this interface; it returns `false` otherwise. If this `Class` object represents a primitive type, this method returns `false`.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the object to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if `obj` is an instance of this class |

### isInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInterface(): Boolean
```

Determines if this `Class` object represents an interface type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `Class` object represents an interface; `false` otherwise. |

### isLocalClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLocalClass(): Boolean
```

Returns `true` if and only if the underlying class is a local class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if this class is a local class. |

### isMemberClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMemberClass(): Boolean
```

Returns `true` if and only if the underlying class is a member class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if this class is a member class. |

### isNestmateOf

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNestmateOf(c: Class<*>): Boolean
```

Determines if the given `Class` is a nestmate of the class or interface represented by this `Class` object. Two classes or interfaces are nestmates if they have the same [nest host](../java/lang/Class.md)).

| Parameters ||
|---|---|
| `c` | [Class](../java/lang/Class.md)\<\*\>: the class to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this class and `c` are members of the same nest; and `false` otherwise. |

### isPrimitive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPrimitive(): Boolean
```

Determines if the specified `Class` object represents a primitive type.

There are nine predefined `Class` objects to represent the eight primitive types and void. These are created by the Java Virtual Machine, and have the same names as the primitive types that they represent, namely `boolean`, `byte`, `char`, `short`, `int`, `long`, `float`, and `double`.

These objects may only be accessed via the following public static final variables, and are the only `Class` objects for which this method returns `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this class represents a primitive type |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Boolean#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Character#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Byte#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Short#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Long#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Float#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Double#TYPE:java.lang.Class`
- `https://developer.android.com/reference/kotlin/java/lang/Void#TYPE:java.lang.Class`

### isRecord

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRecord(): Boolean
```

Returns `true` if and only if this class is a record class.

The [direct superclass](../java/lang/Class.md)) of a record class is `java.lang.Record`. A record class is [final](../java/lang/reflect/Modifier.md). A record class has (possibly zero) record components; `https://developer.android.com/reference/kotlin/java/lang/Class#getRecordComponents()` returns a non-null but possibly empty value for a record.

Note that class `https://developer.android.com/reference/kotlin/java/lang/Record` is not a record class and thus invoking this method on class `Record` returns `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this class is a record class, otherwise false |

### isSealed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSealed(): Boolean
```

Returns `true` if and only if this `Class` object represents a sealed class or interface. If this `Class` object represents a primitive type, `void`, or an array type, this method returns `false`. A sealed class or interface has (possibly zero) permitted subclasses; `https://developer.android.com/reference/kotlin/java/lang/Class#getPermittedSubclasses()` returns a non-null but possibly empty value for a sealed class or interface.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if this `Class` object represents a sealed class or interface. |

### isSynthetic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSynthetic(): Boolean
```

{@return {@code true} if and only if this class has the synthetic modifier \* bit set}
**See Also**

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun newInstance(): T
```

**Deprecated:** *This method propagates any exception thrown by the nullary constructor, including a checked exception. Use of this method effectively bypasses the compile-time exception checking that would otherwise be performed by the compiler. The `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor#newInstance(kotlin.Any)` method avoids this problem by wrapping any exception thrown by the constructor in a (checked) `https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException`.*

*The call*
*```kotlin
<code>clazz.newInstance()
</code>
```
can be replaced by
```kotlin
<code>clazz.getDeclaredConstructor().newInstance()
</code>
```
The latter sequence of calls is inferred to be able to throw the additional exception types `https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException` and `https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException`. Both of these exception types are subclasses of `https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException`.*

<br />

Creates a new instance of the class represented by this `Class` object. The class is instantiated as if by a `new` expression with an empty argument list. The class is initialized if it has not already been initialized.

| Return ||
|---|---|
| `T` | a newly allocated instance of the class represented by this object. |

| Exceptions ||
|---|---|
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |
| `java.lang.IllegalAccessException` | if the class or its nullary constructor is not accessible. |
| `java.lang.InstantiationException` | if this `Class` represents an abstract class, an interface, an array class, a primitive type, or void; or if the class has no nullary constructor; or if the instantiation fails for some other reason. |

### toGenericString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toGenericString(): String
```

Returns a string describing this `Class`, including information about modifiers and type parameters. The string is formatted as a list of type modifiers, if any, followed by the kind of type (empty string for primitive types and `class`, `enum`, `interface`, `@interface`, or `record` as appropriate), followed by the type's name, followed by an angle-bracketed comma-separated list of the type's type parameters, if any, including informative bounds on the type parameters, if any. A space is used to separate modifiers from one another and to separate any modifiers from the kind of type. The modifiers occur in canonical order. If there are no type parameters, the type parameter list is elided. For an array type, the string starts with the type name, followed by an angle-bracketed comma-separated list of the type's type parameters, if any, followed by a sequence of `[]` characters, one set of brackets per dimension of the array.

Note that since information about the runtime representation of a type is being generated, modifiers not present on the originating source code or illegal on the originating source code may be present.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string describing this `Class`, including information about modifiers and type parameters |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Converts the object to a string. The string representation is the string "class" or "interface", followed by a space, and then by the name of the class in the format returned by `getName`. If this `Class` object represents a primitive type, this method returns the name of the primitive type. If this `Class` object represents void this method returns "void". If this `Class` object represents an array type, this method returns "class " followed by `getName`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this `Class` object. |
