# ContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentHandler

```
abstract class ContentHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.ContentHandler](../java/net/ContentHandler.md) |

The abstract class`ContentHandler`is the superclass of all classes that read an`Object`from a`URLConnection`.

An application does not generally call the`getContent`method in this class directly. Instead, an application calls the`getContent`method in class`URL`or in`URLConnection`. The application's content handler factory (an instance of a class that implements the interface`ContentHandlerFactory`set up by a call to`setContentHandler`) is called with a`String`giving the MIME type of the object being received on the socket. The factory returns an instance of a subclass of`ContentHandler`, and its`getContent`method is called to create the object.

If no content handler could be found, URLConnection will look for a content handler in a user-defineable set of places. By default it looks in sun.net.www.content, but users can define a vertical-bar delimited set of class prefixes to search through in addition by defining the java.content.handler.pkgs property. The class name must be of the form: 

```kotlin
{package-prefix}.{major}.{minor}
  e.g.
      YoyoDyne.experimental.text.plain
  
```
If the loading of the content handler class would be performed by a classloader that is outside of the delegation chain of the caller, the JVM will need the RuntimePermission "getClassLoader".

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------|---|
| [ContentHandler](../java/net/ContentHandler.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](../java/net/ContentHandler.md))`(`urlc:` ` [URLConnection](../java/net/URLConnection.md)!`)` Given a URL connect stream positioned at the beginning of the representation of an object, this method reads that stream and creates an object from it. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](../java/net/ContentHandler.md))`(`urlc:` ` [URLConnection](../java/net/URLConnection.md)!`, `classes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java/lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>!`)` Given a URL connect stream positioned at the beginning of the representation of an object, this method reads that stream and creates an object that matches one of the types specified. |

## Public constructors

### ContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ContentHandler()
```

## Public methods

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContent(urlc: URLConnection!): Any!
```

Given a URL connect stream positioned at the beginning of the representation of an object, this method reads that stream and creates an object from it.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `urlc` | [URLConnection](../java/net/URLConnection.md)!:a URL connection. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object read by the`ContentHandler`. |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while reading the object. |

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContent(
    urlc: URLConnection!, 
    classes: Array<Class<Any!>!>!
): Any!
```

Given a URL connect stream positioned at the beginning of the representation of an object, this method reads that stream and creates an object that matches one of the types specified. The default implementation of this method should call getContent() and screen the return type for a match of the suggested types.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urlc` | [URLConnection](../java/net/URLConnection.md)!:a URL connection. |
| `classes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>!:an array of types requested |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object read by the`ContentHandler`that is the first match of the suggested types. null if none of the requested are supported. |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while reading the object. |
