# Compiler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Compiler

```
class Compiler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.lang.Compiler](https://developer.android.com/reference/kotlin/java/lang/Compiler#) |

Does nothing on Android.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [command](https://developer.android.com/reference/kotlin/java/lang/Compiler#command(kotlin.Any))`(`cmd:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Executes an operation according to the specified command object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compileClass](https://developer.android.com/reference/kotlin/java/lang/Compiler#compileClass(java.lang.Class))`(`classToCompile:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<*>!`)` Compiles the specified class using the JIT compiler and indicates if compilation has been successful. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compileClasses](https://developer.android.com/reference/kotlin/java/lang/Compiler#compileClasses(kotlin.String))`(`nameRoot:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compiles all classes whose name matches the specified name using the JIT compiler and indicates if compilation has been successful. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disable](https://developer.android.com/reference/kotlin/java/lang/Compiler#disable())`()` Disables the JIT compiler. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enable](https://developer.android.com/reference/kotlin/java/lang/Compiler#enable())`()` Enables the JIT compiler. |

## Public methods

### command

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun command(cmd: Any!): Any!
```

Executes an operation according to the specified command object. This method is the low-level interface to the JIT compiler. It may return any object or`null`if no JIT compiler is available. Returns null on Android, whether or not the system has a JIT.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `cmd` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the command object for the JIT compiler. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the result of executing command or`null`. |

### compileClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compileClass(classToCompile: Class<*>!): Boolean
```

Compiles the specified class using the JIT compiler and indicates if compilation has been successful. Does nothing and returns false on Android.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| `classToCompile` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<\*\>!:java.lang.Class the class to JIT compile |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the compilation has been successful;`false`if it has failed or if there is no JIT compiler available. |

### compileClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compileClasses(nameRoot: String!): Boolean
```

Compiles all classes whose name matches the specified name using the JIT compiler and indicates if compilation has been successful. Does nothing and returns false on Android.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `nameRoot` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to match class names with. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the compilation has been successful;`false`if it has failed or if there is no JIT compiler available. |

### disable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun disable(): Unit
```

Disables the JIT compiler. Does nothing on Android. 

### enable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun enable(): Unit
```

Enables the JIT compiler. Does nothing on Android.
