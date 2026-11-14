# AbstractPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractPreferences

```
abstract class AbstractPreferences : Preferences
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.prefs.Preferences](../java/util/prefs/Preferences.md) ||
| | ↳ | [java.util.prefs.AbstractPreferences](../java/util/prefs/AbstractPreferences.md) |

This class provides a skeletal implementation of the [Preferences](../java/util/prefs/Preferences.md) class, greatly easing the task of implementing it.

**This class is for Preferences implementers only. Normal users of the Preferences facility should have no need to consult this documentation. The [Preferences](../java/util/prefs/Preferences.md) documentation should suffice.**

Implementors must override the nine abstract service-provider interface (SPI) methods: [getSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md)), [putSpi(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md)), [removeSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md)), [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md)), [removeNodeSpi()](../java/util/prefs/AbstractPreferences.md)), [keysSpi()](../java/util/prefs/AbstractPreferences.md)), [childrenNamesSpi()](../java/util/prefs/AbstractPreferences.md)), [syncSpi()](../java/util/prefs/AbstractPreferences.md))and [flushSpi()](../java/util/prefs/AbstractPreferences.md)). All of the concrete methods specify precisely how they are implemented atop these SPI methods. The implementor may, at his discretion, override one or more of the concrete methods if the default implementation is unsatisfactory for any reason, such as performance.

The SPI methods fall into three groups concerning exception behavior. The getSpi method should never throw exceptions, but it doesn't really matter, as any exception thrown by this method will be intercepted by [get(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md)), which will return the specified default value to the caller. The removeNodeSpi, keysSpi, childrenNamesSpi, syncSpi and flushSpi methods are specified to throw [BackingStoreException](../java/util/prefs/BackingStoreException.md), and the implementation is required to throw this checked exception if it is unable to perform the operation. The exception propagates outward, causing the corresponding API method to fail.

The remaining SPI methods [putSpi(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md)), [removeSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))and [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))have more complicated exception behavior. They are not specified to throw BackingStoreException, as they can generally obey their contracts even if the backing store is unavailable. This is true because they return no information and their effects are not required to become permanent until a subsequent call to [Preferences.flush()](../java/util/prefs/Preferences.md))or [Preferences.sync()](../java/util/prefs/Preferences.md)). Generally speaking, these SPI methods should not throw exceptions. In some implementations, there may be circumstances under which these calls cannot even enqueue the requested operation for later processing. Even under these circumstances it is generally better to simply ignore the invocation and return, rather than throwing an exception. Under these circumstances, however, all subsequent invocations of flush() and sync should return false, as returning true would imply that all previous operations had successfully been made permanent.

There is one circumstance under which putSpi, removeSpi and childSpi*should* throw an exception: if the caller lacks sufficient privileges on the underlying operating system to perform the requested operation. This will, for instance, occur on most systems if a non-privileged user attempts to modify system preferences. (The required privileges will vary from implementation to implementation. On some implementations, they are the right to modify the contents of some directory in the file system; on others they are the right to modify contents of some key in a registry.) Under any of these circumstances, it would generally be undesirable to let the program continue executing as if these operations would become permanent at a later time. While implementations are not required to throw an exception under these circumstances, they are encouraged to do so. A [SecurityException](../java/lang/SecurityException.md) would be appropriate.

Most of the SPI methods require the implementation to read or write information at a preferences node. The implementor should beware of the fact that another VM may have concurrently deleted this node from the backing store. It is the implementation's responsibility to recreate the node if it has been deleted.

Implementation note: In Sun's default Preferences implementations, the user's identity is inherited from the underlying operating system and does not change for the lifetime of the virtual machine. It is recognized that server-side Preferences implementations may have the user identity change from request to request, implicitly passed to Preferences methods via the use of a static [ThreadLocal](../java/lang/ThreadLocal.md) instance. Authors of such implementations are*strongly* encouraged to determine the user at the time preferences are accessed (for example by the [get(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))or [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))method) rather than permanently associating a user with each Preferences instance. The latter behavior conflicts with normal Preferences usage and would lead to great confusion.

## Summary

| Inherited constants ||
|---|---|
| From class [Preferences](../java/util/prefs/Preferences.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_KEY_LENGTH](../java/util/prefs/Preferences.md) <br /> Maximum length of string allowed as a key (80 characters). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_NAME_LENGTH](../java/util/prefs/Preferences.md) <br /> Maximum length of a node name (80 characters). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_VALUE_LENGTH](../java/util/prefs/Preferences.md) <br /> Maximum length of string allowed as a value (8192 characters). <br /> | ||

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractPreferences](../java/util/prefs/AbstractPreferences.md))`(`parent:` ` [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a preference node with the specified parent and the specified name relative to its parent. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [absolutePath](../java/util/prefs/AbstractPreferences.md))`()` Implements the absolutePath method as per the specification in [Preferences.absolutePath()](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addNodeChangeListener](../java/util/prefs/AbstractPreferences.md))`(`ncl:` ` [NodeChangeListener](../java/util/prefs/NodeChangeListener.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPreferenceChangeListener](../java/util/prefs/AbstractPreferences.md))`(`pcl:` ` [PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md)!`)` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [childrenNames](../java/util/prefs/AbstractPreferences.md))`()` Implements the children method as per the specification in [Preferences.childrenNames()](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/prefs/AbstractPreferences.md))`()` Implements the clear method as per the specification in [Preferences.clear()](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exportNode](../java/util/prefs/AbstractPreferences.md))`(`os:` ` [OutputStream](../java/io/OutputStream.md)!`)` Implements the exportNode method as per the specification in [Preferences.exportNode(OutputStream)](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exportSubtree](../java/util/prefs/AbstractPreferences.md))`(`os:` ` [OutputStream](../java/io/OutputStream.md)!`)` Implements the exportSubtree method as per the specification in [Preferences.exportSubtree(OutputStream)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/util/prefs/AbstractPreferences.md))`()` Implements the flush method as per the specification in [Preferences.flush()](../java/util/prefs/Preferences.md)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [get](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Implements the get method as per the specification in [Preferences.get(String,String)](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Implements the getBoolean method as per the specification in [Preferences.getBoolean(String,boolean)](../java/util/prefs/Preferences.md)). |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getByteArray](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Implements the getByteArray method as per the specification in[Preferences.getByteArray(String,byte[])](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getByteArray(kotlin.String,%20kotlin.ByteArray)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Implements the getDouble method as per the specification in [Preferences.getDouble(String,double)](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Implements the getFloat method as per the specification in [Preferences.getFloat(String,float)](../java/util/prefs/Preferences.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implements the getInt method as per the specification in [Preferences.getInt(String,int)](../java/util/prefs/Preferences.md)). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `def:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Implements the getLong method as per the specification in [Preferences.getLong(String,long)](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserNode](../java/util/prefs/AbstractPreferences.md))`()` Implements the isUserNode method as per the specification in [Preferences.isUserNode()](../java/util/prefs/Preferences.md)). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keys](../java/util/prefs/AbstractPreferences.md))`()` Implements the keys method as per the specification in [Preferences.keys()](../java/util/prefs/Preferences.md)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/util/prefs/AbstractPreferences.md))`()` Implements the name method as per the specification in [Preferences.name()](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Preferences](../java/util/prefs/Preferences.md)! | [node](../java/util/prefs/AbstractPreferences.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Implements the node method as per the specification in [Preferences.node(String)](../java/util/prefs/Preferences.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nodeExists](../java/util/prefs/AbstractPreferences.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Implements the nodeExists method as per the specification in [Preferences.nodeExists(String)](../java/util/prefs/Preferences.md)). |
| open [Preferences](../java/util/prefs/Preferences.md)! | [parent](../java/util/prefs/AbstractPreferences.md))`()` Implements the parent method as per the specification in [Preferences.parent()](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Implements the put method as per the specification in [Preferences.put(String,String)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putBoolean](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Implements the putBoolean method as per the specification in [Preferences.putBoolean(String,boolean)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putByteArray](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Implements the putByteArray method as per the specification in[Preferences.putByteArray(String,byte[])](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putByteArray(kotlin.String,%20kotlin.ByteArray)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putDouble](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Implements the putDouble method as per the specification in [Preferences.putDouble(String,double)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putFloat](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Implements the putFloat method as per the specification in [Preferences.putFloat(String,float)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putInt](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implements the putInt method as per the specification in [Preferences.putInt(String,int)](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLong](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Implements the putLong method as per the specification in [Preferences.putLong(String,long)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Implements the remove(String) method as per the specification in [Preferences.remove(String)](../java/util/prefs/Preferences.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNode](../java/util/prefs/AbstractPreferences.md))`()` Implements the removeNode() method as per the specification in [Preferences.removeNode()](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNodeChangeListener](../java/util/prefs/AbstractPreferences.md))`(`ncl:` ` [NodeChangeListener](../java/util/prefs/NodeChangeListener.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePreferenceChangeListener](../java/util/prefs/AbstractPreferences.md))`(`pcl:` ` [PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sync](../java/util/prefs/AbstractPreferences.md))`()` Implements the sync method as per the specification in [Preferences.sync()](../java/util/prefs/Preferences.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/prefs/AbstractPreferences.md))`()` Returns the absolute path name of this preferences node. |

| Protected methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)!\>! | [cachedChildren](../java/util/prefs/AbstractPreferences.md))`()` Returns all known unremoved children of this node. |
| abstract [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)! | [childSpi](../java/util/prefs/AbstractPreferences.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the named child of this preference node, creating it if it does not already exist. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [childrenNamesSpi](../java/util/prefs/AbstractPreferences.md))`()` Returns the names of the children of this preference node. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flushSpi](../java/util/prefs/AbstractPreferences.md))`()` This method is invoked with this node locked. |
| open [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)! | [getChild](../java/util/prefs/AbstractPreferences.md))`(`nodeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the named child if it exists, or null if it does not. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSpi](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the value associated with the specified key at this preference node, or null if there is no association for this key, or the association cannot be determined at this time. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemoved](../java/util/prefs/AbstractPreferences.md))`()` Returns true iff this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keysSpi](../java/util/prefs/AbstractPreferences.md))`()` Returns all of the keys that have an associated value in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putSpi](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Put the given key-value association into this preference node. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNodeSpi](../java/util/prefs/AbstractPreferences.md))`()` Removes this preference node, invalidating it and any preferences that it contains. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpi](../java/util/prefs/AbstractPreferences.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove the association (if any) for the specified key at this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [syncSpi](../java/util/prefs/AbstractPreferences.md))`()` This method is invoked with this node locked. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Preferences](../java/util/prefs/Preferences.md) |--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [importPreferences](../java/util/prefs/Preferences.md))`(`is:` ` [InputStream](../java/io/InputStream.md)!`)` <br /> Imports all of the preferences represented by the XML document on the specified input stream. The document may represent user preferences or system preferences. If it represents user preferences, the preferences will be imported into the calling user's preference tree (even if they originally came from a different user's preference tree). If any of the preferences described by the document inhabit preference nodes that do not exist, the nodes will be created. The XML document must have the following DOCTYPE declaration: ```kotlin <code>&lt;!DOCTYPE preferences SYSTEM "http://java.sun.com/dtd/preferences.dtd"&gt; </code> ``` (This method is designed for use in conjunction with [exportNode(java.io.OutputStream)](../java/util/prefs/Preferences.md))and [exportSubtree(java.io.OutputStream)](../java/util/prefs/Preferences.md)). This method is an exception to the general rule that the results of concurrently executing multiple methods in this class yields results equivalent to some serial execution. The method behaves as if implemented on top of the other public methods in this class, notably [node(java.lang.String)](../java/util/prefs/Preferences.md))and [put(java.lang.String,java.lang.String)](../java/util/prefs/Preferences.md)). <br /> | | [Preferences](../java/util/prefs/Preferences.md)! | [systemNodeForPackage](../java/util/prefs/Preferences.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`)` <br /> **WARNING:**On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the preference node from the system preference tree that is associated (by convention) with the specified class's package. The convention is as follows: the absolute path name of the node is the fully qualified package name, preceded by a slash ('/'), and with each period ('.') replaced by a slash. For example the absolute path name of the node associated with the class com.acme.widget.Foo is /com/acme/widget. This convention does not apply to the unnamed package, whose associated preference node is \<unnamed\>. This node is not intended for long term use, but for convenience in the early development of programs that do not yet belong to a package, and for "throwaway" programs.*Valuable data should not be stored at this node as it is shared by all programs that use it.* A class Foo wishing to access preferences pertaining to its package can obtain a preference node as follows: ```kotlin static Preferences prefs = Preferences.systemNodeForPackage(Foo.class); ``` This idiom obviates the need for using a string to describe the preferences node and decreases the likelihood of a run-time failure. (If the class name is misspelled, it will typically result in a compile-time error.) Invoking this method will result in the creation of the returned node and its ancestors if they do not already exist. If the returned node did not exist prior to this call, this node and any ancestors that were created by this call are not guaranteed to become permanent until the flush method is called on the returned node (or one of its ancestors or descendants). <br /> | | [Preferences](../java/util/prefs/Preferences.md)! | [systemRoot](../java/util/prefs/Preferences.md))`()` <br /> **WARNING:**On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the root preference node for the system. <br /> | | [Preferences](../java/util/prefs/Preferences.md)! | [userNodeForPackage](../java/util/prefs/Preferences.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`)` <br /> **WARNING:**On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the preference node from the calling user's preference tree that is associated (by convention) with the specified class's package. The convention is as follows: the absolute path name of the node is the fully qualified package name, preceded by a slash ('/'), and with each period ('.') replaced by a slash. For example the absolute path name of the node associated with the class com.acme.widget.Foo is /com/acme/widget. This convention does not apply to the unnamed package, whose associated preference node is \<unnamed\>. This node is not intended for long term use, but for convenience in the early development of programs that do not yet belong to a package, and for "throwaway" programs.*Valuable data should not be stored at this node as it is shared by all programs that use it.* A class Foo wishing to access preferences pertaining to its package can obtain a preference node as follows: ```kotlin static Preferences prefs = Preferences.userNodeForPackage(Foo.class); ``` This idiom obviates the need for using a string to describe the preferences node and decreases the likelihood of a run-time failure. (If the class name is misspelled, it will typically result in a compile-time error.) Invoking this method will result in the creation of the returned node and its ancestors if they do not already exist. If the returned node did not exist prior to this call, this node and any ancestors that were created by this call are not guaranteed to become permanent until the flush method is called on the returned node (or one of its ancestors or descendants). <br /> | | [Preferences](../java/util/prefs/Preferences.md)! | [userRoot](../java/util/prefs/Preferences.md))`()` <br /> **WARNING:**On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the root preference node for the calling user. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](../java/util/prefs/AbstractPreferences.md) An object whose monitor is used to lock this node. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [newNode](../java/util/prefs/AbstractPreferences.md) This field should be true if this node did not exist in the backing store prior to the creation of this object. |

## Protected constructors

### AbstractPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractPreferences(
    parent: AbstractPreferences!, 
    name: String!)
```

Creates a preference node with the specified parent and the specified name relative to its parent.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)!:the parent of this preference node, or null if this is the root. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of this preference node, relative to its parent, or "" if this is the root. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if name contains a slash ('/'), or parent is null and name isn't "". |

## Public methods

### absolutePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun absolutePath(): String!
```

Implements the absolutePath method as per the specification in [Preferences.absolutePath()](../java/util/prefs/Preferences.md)).

This implementation merely returns the absolute path name that was computed at the time that this node was constructed (based on the name that was passed to this node's constructor, and the names that were passed to this node's ancestors' constructors).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | this preference node's absolute path name. |

### addNodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNodeChangeListener(ncl: NodeChangeListener!): Unit
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `ncl` | [NodeChangeListener](../java/util/prefs/NodeChangeListener.md)!:The NodeChangeListener to add. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if ncl is null. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |

### addPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPreferenceChangeListener(pcl: PreferenceChangeListener!): Unit
```

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pcl` | [PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md)!:The preference change listener to add. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if pcl is null. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |

### childrenNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun childrenNames(): Array<String!>!
```

Implements the children method as per the specification in [Preferences.childrenNames()](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock, checks that the node has not been removed, constructs a TreeSet initialized to the names of children already cached (the children in this node's "child-cache"), invokes [childrenNamesSpi()](../java/util/prefs/AbstractPreferences.md)), and adds all of the returned child-names into the set. The elements of the tree set are dumped into a String array using the toArray method, and this array is returned.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the names of the children of this preference node. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences#cachedChildren()> 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Implements the clear method as per the specification in [Preferences.clear()](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock, invokes [keys()](../java/util/prefs/AbstractPreferences.md))to obtain an array of keys, and iterates over the array invoking [remove(java.lang.String)](../java/util/prefs/AbstractPreferences.md))on each key.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

### exportNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exportNode(os: OutputStream!): Unit
```

Implements the exportNode method as per the specification in [Preferences.exportNode(OutputStream)](../java/util/prefs/Preferences.md)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `os` | [OutputStream](../java/io/OutputStream.md)!:the output stream on which to emit the XML document. |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if writing to the specified output stream results in an IOException. |
| `java.util.prefs.BackingStoreException` | if preference data cannot be read from backing store. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |
| --- | --- |

### exportSubtree

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exportSubtree(os: OutputStream!): Unit
```

Implements the exportSubtree method as per the specification in [Preferences.exportSubtree(OutputStream)](../java/util/prefs/Preferences.md)).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `os` | [OutputStream](../java/io/OutputStream.md)!:the output stream on which to emit the XML document. |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if writing to the specified output stream results in an IOException. |
| `java.util.prefs.BackingStoreException` | if preference data cannot be read from backing store. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |
| --- | --- |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Implements the flush method as per the specification in [Preferences.flush()](../java/util/prefs/Preferences.md)).

This implementation calls a recursive helper method that locks this node, invokes flushSpi() on it, unlocks this node, and recursively invokes this method on each "cached child." A cached child is a child of this node that has been created in this VM and not subsequently removed. In effect, this method does a depth first traversal of the "cached subtree" rooted at this node, calling flushSpi() on each node in the subTree while only that node is locked. Note that flushSpi() is invoked top-down.

If this method is invoked on a node that has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method, flushSpi() is invoked on this node, but not on others.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences#flush()> 

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    key: String!, 
    def: String!
): String!
```

Implements the get method as per the specification in [Preferences.get(String,String)](../java/util/prefs/Preferences.md)).

This implementation first checks to see if key is null throwing a NullPointerException if this is the case. Then it obtains this preference node's lock, checks that the node has not been removed, invokes [getSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md)), and returns the result, unless the getSpi invocation returns null or throws an exception, in which case this invocation returns def.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned. |
| `def` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value to be returned in the event that this preference node has no value associated with key. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value associated with key, or def if no value is associated with key. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. (A null default*is*permitted.) |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(
    key: String!, 
    def: Boolean
): Boolean
```

Implements the getBoolean method as per the specification in [Preferences.getBoolean(String,boolean)](../java/util/prefs/Preferences.md)).

This implementation invokes [get(key,](../java/util/prefs/AbstractPreferences.md)). If the return value is non-null, it is compared with "true" using [String.equalsIgnoreCase(String)](../java/lang/String.md)). If the comparison returns true, this invocation returns true. Otherwise, the original return value is compared with "false", again using [String.equalsIgnoreCase(String)](../java/lang/String.md)). If the comparison returns true, this invocation returns false. Otherwise, this invocation returns def.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as a boolean. |
| `def` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a boolean. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the boolean value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a boolean. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. |

### getByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getByteArray(
    key: String!, 
    def: ByteArray!
): ByteArray!
```

Implements the getByteArray method as per the specification in[Preferences.getByteArray(String,byte[])](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getByteArray(kotlin.String,%20kotlin.ByteArray)).

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as a byte array. |
| `def` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a byte array. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the byte array value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a byte array. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. (A null value for def*is*permitted.) |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(
    key: String!, 
    def: Double
): Double
```

Implements the getDouble method as per the specification in [Preferences.getDouble(String,double)](../java/util/prefs/Preferences.md)).

This implementation invokes [get(key,](../java/util/prefs/AbstractPreferences.md)). If the return value is non-null, the implementation attempts to translate it to an double with [Double.parseDouble(String)](../java/lang/Double.md)). If the attempt succeeds, the return value is returned by this method. Otherwise, def is returned.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as a double. |
| `def` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a double. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the double value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a double. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFloat(
    key: String!, 
    def: Float
): Float
```

Implements the getFloat method as per the specification in [Preferences.getFloat(String,float)](../java/util/prefs/Preferences.md)).

This implementation invokes [get(key,](../java/util/prefs/AbstractPreferences.md)). If the return value is non-null, the implementation attempts to translate it to an float with [Float.parseFloat(String)](../java/lang/Float.md)). If the attempt succeeds, the return value is returned by this method. Otherwise, def is returned.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as a float. |
| `def` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a float. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the float value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a float. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(
    key: String!, 
    def: Int
): Int
```

Implements the getInt method as per the specification in [Preferences.getInt(String,int)](../java/util/prefs/Preferences.md)).

This implementation invokes [get(key,](../java/util/prefs/AbstractPreferences.md)). If the return value is non-null, the implementation attempts to translate it to an int with [Integer.parseInt(String)](../java/lang/Integer.md)). If the attempt succeeds, the return value is returned by this method. Otherwise, def is returned.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as an int. |
| `def` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as an int. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the int value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as an int. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(
    key: String!, 
    def: Long
): Long
```

Implements the getLong method as per the specification in [Preferences.getLong(String,long)](../java/util/prefs/Preferences.md)).

This implementation invokes [get(key,](../java/util/prefs/AbstractPreferences.md)). If the return value is non-null, the implementation attempts to translate it to a long with [Long.parseLong(String)](../java/lang/Long.md)). If the attempt succeeds, the return value is returned by this method. Otherwise, def is returned.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose associated value is to be returned as a long. |
| `def` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a long. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a long. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.NullPointerException` | if key is null. |

### isUserNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserNode(): Boolean
```

Implements the isUserNode method as per the specification in [Preferences.isUserNode()](../java/util/prefs/Preferences.md)).

This implementation compares this node's root node (which is stored in a private field) with the value returned by [Preferences.userRoot()](../java/util/prefs/Preferences.md)). If the two object references are identical, this method returns true.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this preference node is in the user preference tree, false if it's in the system preference tree. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keys(): Array<String!>!
```

Implements the keys method as per the specification in [Preferences.keys()](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock, checks that the node has not been removed and invokes [keysSpi()](../java/util/prefs/AbstractPreferences.md)).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of the keys that have an associated value in this preference node. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun name(): String!
```

Implements the name method as per the specification in [Preferences.name()](../java/util/prefs/Preferences.md)).

This implementation merely returns the name that was passed to this node's constructor.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | this preference node's name, relative to its parent. |

### node

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun node(path: String!): Preferences!
```

Implements the node method as per the specification in [Preferences.node(String)](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock and checks that the node has not been removed. If path is "", this node is returned; if path is "/", this node's root is returned. If the first character in path is not '/', the implementation breaks path into tokens and recursively traverses the path from this node to the named node, "consuming" a name and a slash from path at each step of the traversal. At each step, the current node is locked and the node's child-cache is checked for the named node. If it is not found, the name is checked to make sure its length does not exceed MAX_NAME_LENGTH. Then the [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))method is invoked, and the result stored in this node's child-cache. If the newly created Preferences object's [newNode](../java/util/prefs/AbstractPreferences.md) field is true and there are any node change listeners, a notification event is enqueued for processing by the event dispatch thread.

When there are no more tokens, the last value found in the child-cache or returned by childSpi is returned by this method. If during the traversal, two "/" tokens occur consecutively, or the final token is "/" (rather than a name), an appropriate IllegalArgumentException is thrown.

If the first character of path is '/' (indicating an absolute path name) this preference node's lock is dropped prior to breaking path into tokens, and this method recursively traverses the path starting from the root (rather than starting from this node). The traversal is otherwise identical to the one described for relative path names. Dropping the lock on this node prior to commencing the traversal at the root node is essential to avoid the possibility of deadlock, as per the [locking invariant](../java/util/prefs/AbstractPreferences.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `pathName` | the path name of the preference node to return. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path name of the preference node to return. |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | the specified preference node. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the path name is invalid (i.e., it contains multiple consecutive slash characters, or ends with a slash character and is more than one character long). |
| `java.lang.NullPointerException` | if path name is null. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### nodeExists

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nodeExists(path: String!): Boolean
```

Implements the nodeExists method as per the specification in [Preferences.nodeExists(String)](../java/util/prefs/Preferences.md)).

This implementation is very similar to [node(java.lang.String)](../java/util/prefs/AbstractPreferences.md)), except that [getChild(java.lang.String)](../java/util/prefs/AbstractPreferences.md))is used instead of [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `pathName` | the path name of the node whose existence is to be checked. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path name of the node whose existence is to be checked. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified node exists. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalArgumentException` | if the path name is invalid (i.e., it contains multiple consecutive slash characters, or ends with a slash character and is more than one character long). |
| `java.lang.NullPointerException` | if path name is null. |
| --- | --- |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method and pathname is not the empty string (""). |

### parent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parent(): Preferences!
```

Implements the parent method as per the specification in [Preferences.parent()](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock, checks that the node has not been removed and returns the parent value that was passed to this node's constructor.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | the parent of this preference node. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: String!, 
    value: String!
): Unit
```

Implements the put method as per the specification in [Preferences.put(String,String)](../java/util/prefs/Preferences.md)).

This implementation checks that the key and value are legal, obtains this preference node's lock, checks that the node has not been removed, invokes [putSpi(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md)), and if there are any preference change listeners, enqueues a notification event for processing by the event dispatch thread.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the specified value is to be associated. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:value to be associated with the specified key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key or value is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH or if value.length exceeds MAX_VALUE_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putBoolean(
    key: String!, 
    value: Boolean
): Unit
```

Implements the putBoolean method as per the specification in [Preferences.putBoolean(String,boolean)](../java/util/prefs/Preferences.md)).

This implementation translates value to a string with [String.valueOf(boolean)](../java/lang/String.md))and invokes [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))on the result.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putByteArray(
    key: String!, 
    value: ByteArray!
): Unit
```

Implements the putByteArray method as per the specification in[Preferences.putByteArray(String,byte[])](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putByteArray(kotlin.String,%20kotlin.ByteArray)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key or value is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH or if value.length exceeds MAX_VALUE_LENGTH\*3/4. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putDouble(
    key: String!, 
    value: Double
): Unit
```

Implements the putDouble method as per the specification in [Preferences.putDouble(String,double)](../java/util/prefs/Preferences.md)).

This implementation translates value to a string with [Double.toString(double)](../java/lang/Double.md))and invokes [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))on the result.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putFloat(
    key: String!, 
    value: Float
): Unit
```

Implements the putFloat method as per the specification in [Preferences.putFloat(String,float)](../java/util/prefs/Preferences.md)).

This implementation translates value to a string with [Float.toString(float)](../java/lang/Float.md))and invokes [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))on the result.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putInt(
    key: String!, 
    value: Int
): Unit
```

Implements the putInt method as per the specification in [Preferences.putInt(String,int)](../java/util/prefs/Preferences.md)).

This implementation translates value to a string with [Integer.toString(int)](../java/lang/Integer.md))and invokes [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))on the result.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### putLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLong(
    key: String!, 
    value: Long
): Unit
```

Implements the putLong method as per the specification in [Preferences.putLong(String,long)](../java/util/prefs/Preferences.md)).

This implementation translates value to a string with [Long.toString(long)](../java/lang/Long.md))and invokes [put(java.lang.String,java.lang.String)](../java/util/prefs/AbstractPreferences.md))on the result.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key with which the string form of value is to be associated. |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):value whose string form is to be associated with key. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null. |
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: String!): Unit
```

Implements the remove(String) method as per the specification in [Preferences.remove(String)](../java/util/prefs/Preferences.md)).

This implementation obtains this preference node's lock, checks that the node has not been removed, invokes [removeSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))and if there are any preference change listeners, enqueues a notification event for processing by the event dispatch thread.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose mapping is to be removed from the preference node. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if key is null.. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

### removeNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNode(): Unit
```

Implements the removeNode() method as per the specification in [Preferences.removeNode()](../java/util/prefs/Preferences.md)).

This implementation checks to see that this node is the root; if so, it throws an appropriate exception. Then, it locks this node's parent, and calls a recursive helper method that traverses the subtree rooted at this node. The recursive method locks the node on which it was called, checks that it has not already been removed, and then ensures that all of its children are cached: The [childrenNamesSpi()](../java/util/prefs/AbstractPreferences.md))method is invoked and each returned child name is checked for containment in the child-cache. If a child is not already cached, the [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))method is invoked to create a Preferences instance for it, and this instance is put into the child-cache. Then the helper method calls itself recursively on each node contained in its child-cache. Next, it invokes [removeNodeSpi()](../java/util/prefs/AbstractPreferences.md)), marks itself as removed, and removes itself from its parent's child-cache. Finally, if there are any node change listeners, it enqueues a notification event for processing by the event dispatch thread.

Note that the helper method is always invoked with all ancestors up to the "closest non-removed ancestor" locked.

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has already been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |
| `java.lang.UnsupportedOperationException` | if this method is invoked on the root node. |
| --- | --- |

### removeNodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNodeChangeListener(ncl: NodeChangeListener!): Unit
```

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `ncl` | [NodeChangeListener](../java/util/prefs/NodeChangeListener.md)!:The NodeChangeListener to remove. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if ncl was not a registered NodeChangeListener on this node. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |

### removePreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePreferenceChangeListener(pcl: PreferenceChangeListener!): Unit
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pcl` | [PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md)!:The preference change listener to remove. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if pcl was not a registered preference change listener on this node. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/Preferences.md))method. |

### sync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sync(): Unit
```

Implements the sync method as per the specification in [Preferences.sync()](../java/util/prefs/Preferences.md)).

This implementation calls a recursive helper method that locks this node, invokes syncSpi() on it, unlocks this node, and recursively invokes this method on each "cached child." A cached child is a child of this node that has been created in this VM and not subsequently removed. In effect, this method does a depth first traversal of the "cached subtree" rooted at this node, calling syncSpi() on each node in the subTree while only that node is locked. Note that syncSpi() is invoked top-down.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences#flush()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the absolute path name of this preferences node.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Protected methods

### cachedChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun cachedChildren(): Array<AbstractPreferences!>!
```

Returns all known unremoved children of this node.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)!>! | all known unremoved children of this node. |

### childSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun childSpi(name: String!): AbstractPreferences!
```

Returns the named child of this preference node, creating it if it does not already exist. It is guaranteed that name is non-null, non-empty, does not contain the slash character ('/'), and is no longer than [MAX_NAME_LENGTH](../java/util/prefs/Preferences.md) characters. Also, it is guaranteed that this node has not been removed. (The implementor needn't check for any of these things.)

Finally, it is guaranteed that the named node has not been returned by a previous invocation of this method or [getChild(java.lang.String)](../java/util/prefs/AbstractPreferences.md))after the last time that it was removed. In other words, a cached value will always be used in preference to invoking this method. Subclasses need not maintain their own cache of previously returned children.

The implementer must ensure that the returned node has not been removed. If a like-named child of this node was previously removed, the implementer must return a newly constructed AbstractPreferences node; once removed, an AbstractPreferences node cannot be "resuscitated."

If this method causes a node to be created, this node is not guaranteed to be persistent until the flush method is invoked on this node or one of its ancestors (or descendants).

This method is invoked with the lock on this node held.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the child node to return, relative to this preference node. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------|
| [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)! | The named child node. |

### childrenNamesSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun childrenNamesSpi(): Array<String!>!
```

Returns the names of the children of this preference node. (The returned array will be of size zero if this node has no children.) This method need not return the names of any nodes already cached, but may do so without harm.

This method is invoked with the lock on this node held.

If this node throws a BackingStoreException, the exception will propagate out beyond the enclosing [childrenNames()](../java/util/prefs/AbstractPreferences.md))invocation.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array containing the names of the children of this preference node. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### flushSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun flushSpi(): Unit
```

This method is invoked with this node locked. The contract of this method is to force any cached changes in the contents of this preference node to the backing store, guaranteeing their persistence. (It is perfectly possible that this node does not exist on the backing store, either because it has been deleted by another VM, or because it has not yet been created.) Note that this method should*not*flush the preferences in any subnodes of this node. If the backing store naturally flushes an entire subtree at once, the implementer is encouraged to override flush(), rather than merely overriding this method.

If this node throws a BackingStoreException, the exception will propagate out beyond the enclosing [flush()](../java/util/prefs/AbstractPreferences.md))invocation.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getChild(nodeName: String!): AbstractPreferences!
```

Returns the named child if it exists, or null if it does not. It is guaranteed that nodeName is non-null, non-empty, does not contain the slash character ('/'), and is no longer than [MAX_NAME_LENGTH](../java/util/prefs/Preferences.md) characters. Also, it is guaranteed that this node has not been removed. (The implementor needn't check for any of these things if he chooses to override this method.)

Finally, it is guaranteed that the named node has not been returned by a previous invocation of this method or [childSpi](../java/util/prefs/AbstractPreferences.md))after the last time that it was removed. In other words, a cached value will always be used in preference to invoking this method. (The implementor needn't maintain his own cache of previously returned children if he chooses to override this method.)

This implementation obtains this preference node's lock, invokes [childrenNames()](../java/util/prefs/AbstractPreferences.md))to get an array of the names of this node's children, and iterates over the array comparing the name of each child with the specified node name. If a child node has the correct name, the [childSpi(java.lang.String)](../java/util/prefs/AbstractPreferences.md))method is invoked and the resulting node is returned. If the iteration completes without finding the specified name, null is returned.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `nodeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:name of the child to be searched for. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [AbstractPreferences](../java/util/prefs/AbstractPreferences.md)! | the named child if it exists, or null if it does not. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### getSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun getSpi(key: String!): String!
```

Return the value associated with the specified key at this preference node, or null if there is no association for this key, or the association cannot be determined at this time. It is guaranteed that key is non-null. Also, it is guaranteed that this node has not been removed. (The implementor needn't check for either of these things.)

Generally speaking, this method should not throw an exception under any circumstances. If, however, if it does throw an exception, the exception will be intercepted and treated as a null return value.

This method is invoked with the lock on this node held.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value associated with the specified key at this preference node, or null if there is no association for this key, or the association cannot be determined at this time. |

### isRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun isRemoved(): Boolean
```

Returns true iff this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. This method locks this node prior to returning the contents of the private field used to track this state.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff this node (or an ancestor) has been removed with the [removeNode()](../java/util/prefs/AbstractPreferences.md))method. |

### keysSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun keysSpi(): Array<String!>!
```

Returns all of the keys that have an associated value in this preference node. (The returned array will be of size zero if this node has no preferences.) It is guaranteed that this node has not been removed.

This method is invoked with the lock on this node held.

If this node throws a BackingStoreException, the exception will propagate out beyond the enclosing [keys()](../java/util/prefs/AbstractPreferences.md))invocation.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of the keys that have an associated value in this preference node. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### putSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun putSpi(
    key: String!, 
    value: String!
): Unit
```

Put the given key-value association into this preference node. It is guaranteed that key and value are non-null and of legal length. Also, it is guaranteed that this node has not been removed. (The implementor needn't check for any of these things.)

This method is invoked with the lock on this node held.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value |

### removeNodeSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun removeNodeSpi(): Unit
```

Removes this preference node, invalidating it and any preferences that it contains. The named child will have no descendants at the time this invocation is made (i.e., the [Preferences.removeNode()](../java/util/prefs/Preferences.md))method invokes this method repeatedly in a bottom-up fashion, removing each of a node's descendants before removing the node itself).

This method is invoked with the lock held on this node and its parent (and all ancestors that are being removed as a result of a single invocation to [Preferences.removeNode()](../java/util/prefs/Preferences.md))).

The removal of a node needn't become persistent until the flush method is invoked on this node (or an ancestor).

If this node throws a BackingStoreException, the exception will propagate out beyond the enclosing [removeNode()](../java/util/prefs/AbstractPreferences.md))invocation.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### removeSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun removeSpi(key: String!): Unit
```

Remove the association (if any) for the specified key at this preference node. It is guaranteed that key is non-null. Also, it is guaranteed that this node has not been removed. (The implementor needn't check for either of these things.)

This method is invoked with the lock on this node held.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key |

### syncSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun syncSpi(): Unit
```

This method is invoked with this node locked. The contract of this method is to synchronize any cached preferences stored at this node with any stored in the backing store. (It is perfectly possible that this node does not exist on the backing store, either because it has been deleted by another VM, or because it has not yet been created.) Note that this method should*not*synchronize the preferences in any subnodes of this node. If the backing store naturally syncs an entire subtree at once, the implementer is encouraged to override sync(), rather than merely overriding this method.

If this node throws a BackingStoreException, the exception will propagate out beyond the enclosing [sync()](../java/util/prefs/AbstractPreferences.md))invocation.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

## Properties

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected val lock: Any!
```

An object whose monitor is used to lock this node. This object is used in preference to the node itself to reduce the likelihood of intentional or unintentional denial of service due to a locked node. To avoid deadlock, a node is*never*locked by a thread that holds a lock on a descendant of that node. 

### newNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var newNode: Boolean
```

This field should be true if this node did not exist in the backing store prior to the creation of this object. The field is initialized to false, but may be set to true by a subclass constructor (and should not be modified thereafter). This field indicates whether a node change event should be fired when creation is complete.
