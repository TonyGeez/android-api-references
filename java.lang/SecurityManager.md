# SecurityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecurityManager

```
open class SecurityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#) |

Legacy security code; do not use.

Security managers do*not* provide a secure environment for executing untrusted code and are unsupported on Android. Untrusted code cannot be safely isolated within a single VM on Android. Application developers can assume that there's no SecurityManager installed, i.e. [java.lang.System#getSecurityManager()](https://developer.android.com/reference/kotlin/java/lang/System#getSecurityManager())will return null.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#SecurityManager())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkAccept(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkAccess(java.lang.Thread))`(`t:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkAccess(java.lang.ThreadGroup))`(`g:` ` [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAwtEventQueueAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkAwtEventQueueAccess())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkConnect](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkConnect(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkConnect](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkConnect(kotlin.String,%20kotlin.Int,%20kotlin.Any))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkCreateClassLoader](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkCreateClassLoader())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkDelete](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkDelete(kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkExec](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkExec(kotlin.String))`(`cmd:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkExit](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkExit(kotlin.Int))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkLink](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkLink(kotlin.String))`(`lib:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkListen(kotlin.Int))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkMemberAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkMemberAccess(java.lang.Class,%20kotlin.Int))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<*>!`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkMulticast](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkMulticast(java.net.InetAddress))`(`maddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkMulticast](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkMulticast(java.net.InetAddress,%20kotlin.Byte))`(`maddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `ttl:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPackageAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageAccess(kotlin.String))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPackageDefinition](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPackageDefinition(kotlin.String))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPermission(java.security.Permission))`(`perm:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPermission(java.security.Permission,%20kotlin.Any))`(`perm:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`, `context:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPrintJobAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPrintJobAccess())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPropertiesAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertiesAccess())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPropertyAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertyAccess(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkRead(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkRead(kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkRead(kotlin.String,%20kotlin.Any))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `context:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkSecurityAccess(kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkSetFactory](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkSetFactory())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkSystemClipboardAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkSystemClipboardAccess())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkTopLevelWindow](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkTopLevelWindow(kotlin.Any))`(`window:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkWrite(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkWrite(kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getInCheck](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#getInCheck())`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSecurityContext](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#getSecurityContext())`()` <br /> |
| --- | --- |
| open [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup)! | [getThreadGroup](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#getThreadGroup())`()` Returns the current thread's thread group. |

| Protected methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [classDepth](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#classDepth(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [classLoaderDepth](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#classLoaderDepth())`()` <br /> |
| open [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader)! | [currentClassLoader](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#currentClassLoader())`()` <br /> |
| --- | --- |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<\*\>! | [currentLoadedClass](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#currentLoadedClass())`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>! | [getClassContext](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#getClassContext())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inClass](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#inClass(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inClassLoader](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#inClassLoader())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inCheck](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#inCheck:kotlin.Boolean) <br /> |

## Public constructors

### SecurityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityManager()
```

## Public methods

### checkAccept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkAccept(
    host: String!, 
    port: Int
): Unit
```  

### checkAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkAccess(t: Thread!): Unit
```  

### checkAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkAccess(g: ThreadGroup!): Unit
```  

### checkAwtEventQueueAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkAwtEventQueueAccess(): Unit
```  

### checkConnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkConnect(
    host: String!, 
    port: Int
): Unit
```  

### checkConnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkConnect(
    host: String!, 
    port: Int, 
    context: Any!
): Unit
```  

### checkCreateClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkCreateClassLoader(): Unit
```  

### checkDelete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkDelete(file: String!): Unit
```  

### checkExec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkExec(cmd: String!): Unit
```  

### checkExit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkExit(status: Int): Unit
```  

### checkLink

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkLink(lib: String!): Unit
```  

### checkListen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkListen(port: Int): Unit
```  

### checkMemberAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkMemberAccess(
    clazz: Class<*>!, 
    which: Int
): Unit
```

**Deprecated:** *this method is deprecated.* 

### checkMulticast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkMulticast(maddr: InetAddress!): Unit
```  

### checkMulticast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkMulticast(
    maddr: InetAddress!, 
    ttl: Byte
): Unit
```

**Deprecated:** *use [checkMulticast(java.net.InetAddress)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkMulticast(java.net.InetAddress))instead.* 

### checkPackageAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPackageAccess(pkg: String!): Unit
```  

### checkPackageDefinition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPackageDefinition(pkg: String!): Unit
```  

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPermission(perm: Permission!): Unit
```  

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPermission(
    perm: Permission!, 
    context: Any!
): Unit
```  

### checkPrintJobAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPrintJobAccess(): Unit
```  

### checkPropertiesAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPropertiesAccess(): Unit
```  

### checkPropertyAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkPropertyAccess(key: String!): Unit
```  

### checkRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRead(fd: FileDescriptor!): Unit
```  

### checkRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRead(file: String!): Unit
```  

### checkRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkRead(
    file: String!, 
    context: Any!
): Unit
```  

### checkSecurityAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkSecurityAccess(target: String!): Unit
```  

### checkSetFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkSetFactory(): Unit
```  

### checkSystemClipboardAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkSystemClipboardAccess(): Unit
```  

### checkTopLevelWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkTopLevelWindow(window: Any!): Boolean
```

**Deprecated:** *this method is deprecated.* 

### checkWrite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkWrite(fd: FileDescriptor!): Unit
```  

### checkWrite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkWrite(file: String!): Unit
```  

### getInCheck

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInCheck(): Boolean
```

**Deprecated:** *Use #checkPermission instead.* 

### getSecurityContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecurityContext(): Any!
```  

### getThreadGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getThreadGroup(): ThreadGroup!
```

Returns the current thread's thread group.

## Protected methods

### classDepth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun classDepth(name: String!): Int
```

**Deprecated:** *Use #checkPermission instead.* 

### classLoaderDepth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun classLoaderDepth(): Int
```

**Deprecated:** *Use #checkPermission instead.* 

### currentClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun currentClassLoader(): ClassLoader!
```

**Deprecated:** *Use #checkPermission instead.* 

### currentLoadedClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun currentLoadedClass(): Class<*>!
```

**Deprecated:** *Use #checkPermission instead.* 

### getClassContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getClassContext(): Array<Class<Any!>!>!
```  

### inClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun inClass(name: String!): Boolean
```

**Deprecated:** *Use #checkPermission instead.* 

### inClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun inClassLoader(): Boolean
```

**Deprecated:** *Use #checkPermission instead.*

## Properties

### inCheck

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var inCheck: Boolean
```

**Deprecated:** *Use #checkPermission instead.*
