Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Preferences

```
abstract class Preferences
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.prefs.Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#) |

| Known Direct Subclasses [AbstractPreferences](https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences) |---|---| | [AbstractPreferences](https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences) | This class provides a skeletal implementation of the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#` class, greatly easing the task of implementing it. | |
| --- | --- | --- | --- | --- | --- | --- |

A node in a hierarchical collection of preference data. This class allows applications to store and retrieve user and system preference and configuration data. This data is stored persistently in an implementation-dependent backing store. Typical implementations include flat files, OS-specific registries, directory servers and SQL databases. The user of this class needn't be concerned with details of the backing store.

There are two separate trees of preference nodes, one for user preferences and one for system preferences. Each user has a separate user preference tree, and all users in a given system share the same system preference tree. The precise description of "user" and "system" will vary from implementation to implementation. Typical information stored in the user preference tree might include font choice, color choice, or preferred window location and size for a particular application. Typical information stored in the system preference tree might include installation configuration data for an application.

Nodes in a preference tree are named in a similar fashion to directories in a hierarchical file system. Every node in a preference tree has a *node name* (which is not necessarily unique), a unique *absolute path name* , and a path name *relative* to each ancestor including itself.

The root node has a node name of the empty string (""). Every other node has an arbitrary node name, specified at the time it is created. The only restrictions on this name are that it cannot be the empty string, and it cannot contain the slash character ('/').

The root node has an absolute path name of "/". Children of the root node have absolute path names of "/" + *\<node name\>* . All other nodes have absolute path names of *\<parent's absolute path name\>* + "/" + *\<node name\>*. Note that all absolute path names begin with the slash character.

A node *n* 's path name relative to its ancestor *a* is simply the string that must be appended to *a* 's absolute path name in order to form *n*'s absolute path name, with the initial slash character (if present) removed. Note that:

- No relative path names begin with the slash character.
- Every node's path name relative to itself is the empty string.
- Every node's path name relative to its parent is its node name (except for the root node, which does not have a parent).
- Every node's path name relative to the root is its absolute path name with the initial slash character removed.

Note finally that:

- No path name contains multiple consecutive slash characters.
- No path name with the exception of the root's absolute path name ends in the slash character.
- Any string that conforms to these two rules is a valid path name.

All of the methods that modify preferences data are permitted to operate asynchronously; they may return immediately, and changes will eventually propagate to the persistent backing store with an implementation-dependent delay. The flush method may be used to synchronously force updates to the backing store. Normal termination of the Java Virtual Machine will *not* result in the loss of pending updates -- an explicit flush invocation is *not* required upon termination to ensure that pending updates are made persistent.

All of the methods that read preferences from a Preferences object require the invoker to provide a default value. The default value is returned if no value has been previously set *or if the backing store is unavailable* . The intent is to allow applications to operate, albeit with slightly degraded functionality, even if the backing store becomes unavailable. Several methods, like flush, have semantics that prevent them from operating if the backing store is unavailable. Ordinary applications should have no need to invoke any of these methods, which can be identified by the fact that they are declared to throw `https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException`.

The methods in this class may be invoked concurrently by multiple threads in a single JVM without the need for external synchronization, and the results will be equivalent to some serial execution. If this class is used concurrently *by multiple JVMs* that store their preference data in the same backing store, the data store will not be corrupted, but no other guarantees are made concerning the consistency of the preference data.

This class contains an export/import facility, allowing preferences to be "exported" to an XML document, and XML documents representing preferences to be "imported" back into the system. This facility may be used to back up all or part of a preference tree, and subsequently restore from the backup.

The XML document has the following DOCTYPE declaration:

```kotlin
<code>&lt;!DOCTYPE preferences SYSTEM "http://java.sun.com/dtd/preferences.dtd"&gt;
  </code>
```
Note that the system URI (http://java.sun.com/dtd/preferences.dtd) is *not* accessed when exporting or importing preferences; it merely serves as a string to uniquely identify the DTD, which is:

```kotlin
<code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
 
     &lt;!-- DTD for a Preferences tree. --&gt;
 
     &lt;!-- The preferences element is at the root of an XML document
          representing a Preferences tree. --&gt;
     &lt;!ELEMENT preferences (root)&gt;
 
     &lt;!-- The preferences element contains an optional version attribute,
           which specifies version of DTD. --&gt;
     &lt;!ATTLIST preferences EXTERNAL_XML_VERSION CDATA "0.0" &gt;
 
     &lt;!-- The root element has a map representing the root's preferences
          (if any), and one node for each child of the root (if any). --&gt;
     &lt;!ELEMENT root (map, node*) &gt;
 
     &lt;!-- Additionally, the root contains a type attribute, which
          specifies whether it's the system or user root. --&gt;
     &lt;!ATTLIST root
               type (system|user) #REQUIRED &gt;
 
     &lt;!-- Each node has a map representing its preferences (if any),
          and one node for each child (if any). --&gt;
     &lt;!ELEMENT node (map, node*) &gt;
 
     &lt;!-- Additionally, each node has a name attribute --&gt;
     &lt;!ATTLIST node
               name CDATA #REQUIRED &gt;
 
     &lt;!-- A map represents the preferences stored at a node (if any). --&gt;
     &lt;!ELEMENT map (entry*) &gt;
 
     &lt;!-- An entry represents a single preference, which is simply
           a key-value pair. --&gt;
     &lt;!ELEMENT entry EMPTY &gt;
     &lt;!ATTLIST entry
               key   CDATA #REQUIRED
               value CDATA #REQUIRED &gt;
  </code>
```
Every Preferences implementation must have an associated `https://developer.android.com/reference/kotlin/java/util/prefs/PreferencesFactory` implementation. Every Java(TM) SE implementation must provide some means of specifying which PreferencesFactory implementation is used to generate the root preferences nodes. This allows the administrator to replace the default preferences implementation with an alternative implementation.

Implementation note: In Sun's JRE, the PreferencesFactory implementation is located as follows:

1. If the system property java.util.prefs.PreferencesFactory is defined, then it is taken to be the fully-qualified name of a class implementing the PreferencesFactory interface. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
2. If a PreferencesFactory implementation class file has been installed in a jar file that is visible to the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#getSystemClassLoader()`, and that jar file contains a provider-configuration file named java.util.prefs.PreferencesFactory in the resource directory META-INF/services, then the first class name specified in that file is taken. If more than one such jar file is provided, the first one found will be used. The class is loaded and instantiated; if this process fails then an unspecified error is thrown.
3. Finally, if neither the above-mentioned system property nor an extension jar file is provided, then the system-wide default PreferencesFactory implementation for the underlying platform is loaded and instantiated.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#MAX_KEY_LENGTH:kotlin.Int` Maximum length of string allowed as a key (80 characters). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#MAX_NAME_LENGTH:kotlin.Int` Maximum length of a node name (80 characters). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#MAX_VALUE_LENGTH:kotlin.Int` Maximum length of string allowed as a value (8192 characters). |
| --- | --- |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#Preferences()()` Sole constructor. |

| Public methods ||
|---|---|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#absolutePath()()` Returns this preference node's absolute path name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addNodeChangeListener(java.util.prefs.NodeChangeListener)(ncl: https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener!)` Registers the specified listener to receive *node change events* for this node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addPreferenceChangeListener(java.util.prefs.PreferenceChangeListener)(pcl: https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeListener!)` Registers the specified listener to receive *preference change events* for this preference node. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#childrenNames()()` Returns the names of the children of this preference node, relative to this node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#clear()()` Removes all of the preferences (key-value associations) in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#exportNode(java.io.OutputStream)(os: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Emits on the specified output stream an XML document representing all of the preferences contained in this node (but not its descendants). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#exportSubtree(java.io.OutputStream)(os: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Emits an XML document representing all of the preferences contained in this node and all of its descendants. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#flush()()` Forces any changes in the contents of this preference node and its descendants to the persistent store. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the specified key in this preference node. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the boolean value represented by the string associated with the specified key in this preference node. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getByteArray(kotlin.String,%20kotlin.ByteArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Returns the byte array value represented by the string associated with the specified key in this preference node. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getDouble(kotlin.String,%20kotlin.Double)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the double value represented by the string associated with the specified key in this preference node. |
| --- | --- |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the float value represented by the string associated with the specified key in this preference node. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the int value represented by the string associated with the specified key in this preference node. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the long value represented by the string associated with the specified key in this preference node. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#importPreferences(java.io.InputStream)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Imports all of the preferences represented by the XML document on the specified input stream. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#isUserNode()()` Returns true if this preference node is in the user preference tree, false if it's in the system preference tree. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#keys()()` Returns all of the keys that have an associated value in this preference node. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#name()()` Returns this preference node's name, relative to its parent. |
| abstract [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#node(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the named preference node in the same tree as this node, creating it and any of its ancestors if they do not already exist. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#nodeExists(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns true if the named preference node exists in the same tree as this node. |
| --- | --- |
| abstract [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#parent()()` Returns the parent of this preference node, or null if this is the root. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#put(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Associates the specified value with the specified key in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Associates a string representing the specified boolean value with the specified key in this preference node. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putByteArray(kotlin.String,%20kotlin.ByteArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Associates a string representing the specified byte array with the specified key in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putDouble(kotlin.String,%20kotlin.Double)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Associates a string representing the specified double value with the specified key in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Associates a string representing the specified float value with the specified key in this preference node. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Associates a string representing the specified int value with the specified key in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Associates a string representing the specified long value with the specified key in this preference node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#remove(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes the value associated with the specified key in this preference node, if any. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()()` Removes this preference node and all of its descendants, invalidating any preferences contained in the removed nodes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNodeChangeListener(java.util.prefs.NodeChangeListener)(ncl: https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener!)` Removes the specified NodeChangeListener, so it no longer receives change events. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removePreferenceChangeListener(java.util.prefs.PreferenceChangeListener)(pcl: https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeListener!)` Removes the specified preference change listener, so it no longer receives preference change events. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#sync()()` Ensures that future reads from this preference node and its descendants reflect any changes that were committed to the persistent store (from any VM) prior to the sync invocation. |
| open static [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#systemNodeForPackage(java.lang.Class)(c: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!)` **WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. |
| open static [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#systemRoot()()` **WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#toString()()` Returns a string representation of this preferences node, as if computed by the expression:(this.isUserNode() ? "User" : "System") + " Preference Node: " + this.absolutePath(). |
| open static [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#userNodeForPackage(java.lang.Class)(c: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!)` **WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. |
| open static [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#)! | `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#userRoot()()` **WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. |
| --- | --- |

## Constants

### MAX_KEY_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_KEY_LENGTH: Int
```

Maximum length of string allowed as a key (80 characters).

 Value: 80

### MAX_NAME_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_NAME_LENGTH: Int
```

Maximum length of a node name (80 characters).

 Value: 80

### MAX_VALUE_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_VALUE_LENGTH: Int
```

Maximum length of string allowed as a value (8192 characters).

 Value: 8192

## Protected constructors

### Preferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Preferences()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### absolutePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun absolutePath(): String!
```

Returns this preference node's absolute path name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | this preference node's absolute path name. |

### addNodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addNodeChangeListener(ncl: NodeChangeListener!): Unit
```

Registers the specified listener to receive *node change events* for this node. A node change event is generated when a child node is added to or removed from this node. (A single `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` invocation results in multiple *node change events*, one for every node in the subtree rooted at the removed node.)

Events are only guaranteed for changes made within the same JVM as the registered listener, though some implementations may generate events for changes made outside this JVM. Events may be generated before the changes have become permanent. Events are not generated when indirect descendants of this node are added or removed; a caller desiring such events must register with each descendant.

Few guarantees can be made regarding node creation. Because nodes are created implicitly upon access, it may not be feasible for an implementation to determine whether a child node existed in the backing store prior to access (for example, because the backing store is unreachable or cached information is out of date). Under these circumstances, implementations are neither required to generate node change events nor prohibited from doing so.

| Parameters ||
|---|---|
| `ncl` | [NodeChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener)!: The NodeChangeListener to add. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if ncl is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNodeChangeListener(java.util.prefs.NodeChangeListener)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addPreferenceChangeListener(java.util.prefs.PreferenceChangeListener)`

### addPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addPreferenceChangeListener(pcl: PreferenceChangeListener!): Unit
```

Registers the specified listener to receive *preference change events* for this preference node. A preference change event is generated when a preference is added to this node, removed from this node, or when the value associated with a preference is changed. (Preference change events are *not* generated by the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method, which generates a *node change event* . Preference change events *are* generated by the clear method.)

Events are only guaranteed for changes made within the same JVM as the registered listener, though some implementations may generate events for changes made outside this JVM. Events may be generated before the changes have been made persistent. Events are not generated when preferences are modified in descendants of this node; a caller desiring such events must register with each descendant.

| Parameters ||
|---|---|
| `pcl` | [PreferenceChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeListener)!: The preference change listener to add. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if pcl is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removePreferenceChangeListener(java.util.prefs.PreferenceChangeListener)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addNodeChangeListener(java.util.prefs.NodeChangeListener)`

### childrenNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun childrenNames(): Array<String!>!
```

Returns the names of the children of this preference node, relative to this node. (The returned array will be of size zero if this node has no children.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the names of the children of this preference node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clear(): Unit
```

Removes all of the preferences (key-value associations) in this preference node. This call has no effect on any descendants of this node.

If this implementation supports *stored defaults*, and this node in the preferences hierarchy contains any such defaults, the stored defaults will be "exposed" by this call, in the sense that they will be returned by succeeding calls to get.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()`

### exportNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun exportNode(os: OutputStream!): Unit
```

Emits on the specified output stream an XML document representing all of the preferences contained in this node (but not its descendants). This XML document is, in effect, an offline backup of the node.

The XML document will have the following DOCTYPE declaration:

```kotlin
<code>&lt;!DOCTYPE preferences SYSTEM "http://java.sun.com/dtd/preferences.dtd"&gt;
  </code>
```
The UTF-8 character encoding will be used.

This method is an exception to the general rule that the results of concurrently executing multiple methods in this class yields results equivalent to some serial execution. If the preferences at this node are modified concurrently with an invocation of this method, the exported preferences comprise a "fuzzy snapshot" of the preferences contained in the node; some of the concurrent modifications may be reflected in the exported data while others may not.

| Parameters ||
|---|---|
| `os` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream on which to emit the XML document. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing to the specified output stream results in an IOException. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if preference data cannot be read from backing store. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#importPreferences(java.io.InputStream)`

### exportSubtree

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun exportSubtree(os: OutputStream!): Unit
```

Emits an XML document representing all of the preferences contained in this node and all of its descendants. This XML document is, in effect, an offline backup of the subtree rooted at the node.

The XML document will have the following DOCTYPE declaration:

```kotlin
<code>&lt;!DOCTYPE preferences SYSTEM "http://java.sun.com/dtd/preferences.dtd"&gt;
  </code>
```
The UTF-8 character encoding will be used.

This method is an exception to the general rule that the results of concurrently executing multiple methods in this class yields results equivalent to some serial execution. If the preferences or nodes in the subtree rooted at this node are modified concurrently with an invocation of this method, the exported preferences comprise a "fuzzy snapshot" of the subtree; some of the concurrent modifications may be reflected in the exported data while others may not.

| Parameters ||
|---|---|
| `os` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream on which to emit the XML document. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing to the specified output stream results in an IOException. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if preference data cannot be read from backing store. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#importPreferences(java.io.InputStream)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#exportNode(java.io.OutputStream)`

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun flush(): Unit
```

Forces any changes in the contents of this preference node and its descendants to the persistent store. Once this method returns successfully, it is safe to assume that all changes made in the subtree rooted at this node prior to the method invocation have become permanent.

Implementations are free to flush changes into the persistent store at any time. They do not need to wait for this method to be called.

When a flush occurs on a newly created node, it is made persistent, as are any ancestors (and descendants) that have yet to be made persistent. Note however that any preference value changes in ancestors are *not* guaranteed to be made persistent.

If this method is invoked on a node that has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method, flushSpi() is invoked on this node, but not on others.

| Exceptions ||
|---|---|
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#sync()`

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(
    key: String!, 
    def: String!
): String!
```

Returns the value associated with the specified key in this preference node. Returns the specified default if there is no value associated with the key, or the backing store is inaccessible.

Some implementations may store default values in their backing stores. If there is no value associated with the specified key but there is such a *stored default*, it is returned in preference to the specified default.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned. |
| `def` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value to be returned in the event that this preference node has no value associated with key. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the value associated with key, or def if no value is associated with key, or the backing store is inaccessible. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. (A null value for def *is* permitted.) |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBoolean(
    key: String!, 
    def: Boolean
): Boolean
```

Returns the boolean value represented by the string associated with the specified key in this preference node. Valid strings are "true", which represents true, and "false", which represents false. Case is ignored, so, for example, "TRUE" and "False" are also valid. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putBoolean(kotlin.String,%20kotlin.Boolean)`.

Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if the associated value is something other than "true" or "false", ignoring case.

If the implementation supports *stored defaults* and such a default exists and is accessible, it is used in preference to the specified default, unless the stored default is something other than "true" or "false", ignoring case, in which case the specified default is used.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as a boolean. |
| `def` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a boolean, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the boolean value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a boolean. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putBoolean(kotlin.String,%20kotlin.Boolean)`

### getByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getByteArray(
    key: String!, 
    def: ByteArray!
): ByteArray!
```

Returns the byte array value represented by the string associated with the specified key in this preference node. Valid strings are *Base64* encoded binary data, as defined in [RFC 2045](http://www.ietf.org/rfc/rfc2045.txt), Section 6.8, with one minor change: the string must consist solely of characters from the *Base64 Alphabet* ; no newline characters or extraneous characters are permitted. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putByteArray(kotlin.String,%20kotlin.ByteArray)`.

Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if the associated value is not a valid Base64 encoded byte array (as defined above).

If the implementation supports *stored defaults* and such a default exists and is accessible, it is used in preference to the specified default, unless the stored default is not a valid Base64 encoded byte array (as defined above), in which case the specified default is used.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as a byte array. |
| `def` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a byte array, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the byte array value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a byte array. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. (A null value for def *is* permitted.) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putByteArray(kotlin.String,%20kotlin.ByteArray)`

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDouble(
    key: String!, 
    def: Double
): Double
```

Returns the double value represented by the string associated with the specified key in this preference node. The string is converted to an integer as by `https://developer.android.com/reference/kotlin/java/lang/Double.html#parseDouble(kotlin.String)`. Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if Double.parseDouble(String) would throw a `https://developer.android.com/reference/kotlin/java/lang/NumberFormatException.html#` if the associated value were passed. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putDouble(kotlin.String,%20kotlin.Double)`.

If the implementation supports *stored defaults* and such a default exists, is accessible, and could be converted to a double with Double.parseDouble, this double is returned in preference to the specified default.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as a double. |
| `def` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a double, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the double value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a double. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putDouble(kotlin.String,%20kotlin.Double)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFloat(
    key: String!, 
    def: Float
): Float
```

Returns the float value represented by the string associated with the specified key in this preference node. The string is converted to an integer as by `https://developer.android.com/reference/kotlin/java/lang/Float.html#parseFloat(kotlin.String)`. Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if Float.parseFloat(String) would throw a `https://developer.android.com/reference/kotlin/java/lang/NumberFormatException.html#` if the associated value were passed. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putFloat(kotlin.String,%20kotlin.Float)`.

If the implementation supports *stored defaults* and such a default exists, is accessible, and could be converted to a float with Float.parseFloat, this float is returned in preference to the specified default.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as a float. |
| `def` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a float, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the float value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a float. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putFloat(kotlin.String,%20kotlin.Float)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInt(
    key: String!, 
    def: Int
): Int
```

Returns the int value represented by the string associated with the specified key in this preference node. The string is converted to an integer as by `https://developer.android.com/reference/kotlin/java/lang/Integer.html#parseInt(kotlin.String)`. Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if Integer.parseInt(String) would throw a `https://developer.android.com/reference/kotlin/java/lang/NumberFormatException.html#` if the associated value were passed. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putInt(kotlin.String,%20kotlin.Int)`.

If the implementation supports *stored defaults* and such a default exists, is accessible, and could be converted to an int with Integer.parseInt, this int is returned in preference to the specified default.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as an int. |
| `def` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as an int, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the int value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as an int. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putInt(kotlin.String,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLong(
    key: String!, 
    def: Long
): Long
```

Returns the long value represented by the string associated with the specified key in this preference node. The string is converted to a long as by `https://developer.android.com/reference/kotlin/java/lang/Long.html#parseLong(kotlin.String)`. Returns the specified default if there is no value associated with the key, the backing store is inaccessible, or if Long.parseLong(String) would throw a `https://developer.android.com/reference/kotlin/java/lang/NumberFormatException.html#` if the associated value were passed. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putLong(kotlin.String,%20kotlin.Long)`.

If the implementation supports *stored defaults* and such a default exists, is accessible, and could be converted to a long with Long.parseLong, this long is returned in preference to the specified default.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose associated value is to be returned as a long. |
| `def` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to be returned in the event that this preference node has no value associated with key or the associated value cannot be interpreted as a long, or the backing store is inaccessible. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the long value represented by the string associated with key in this preference node, or def if the associated value does not exist or cannot be interpreted as a long. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#putLong(kotlin.String,%20kotlin.Long)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### importPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun importPreferences(is: InputStream!): Unit
```

Imports all of the preferences represented by the XML document on the specified input stream. The document may represent user preferences or system preferences. If it represents user preferences, the preferences will be imported into the calling user's preference tree (even if they originally came from a different user's preference tree). If any of the preferences described by the document inhabit preference nodes that do not exist, the nodes will be created.

The XML document must have the following DOCTYPE declaration:

```kotlin
<code>&lt;!DOCTYPE preferences SYSTEM "http://java.sun.com/dtd/preferences.dtd"&gt;
  </code>
```
(This method is designed for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#exportNode(java.io.OutputStream)` and `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#exportSubtree(java.io.OutputStream)`.

This method is an exception to the general rule that the results of concurrently executing multiple methods in this class yields results equivalent to some serial execution. The method behaves as if implemented on top of the other public methods in this class, notably `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#node(kotlin.String)` and `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#put(kotlin.String,%20kotlin.String)`.

| Parameters ||
|---|---|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the input stream from which to read the XML document. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if reading from the specified input stream results in an IOException. |
| `java.lang.SecurityException` | If a security manager is present and it denies RuntimePermission("preferences"). |
| `java.util.prefs.InvalidPreferencesFormatException` | Data on input stream does not constitute a valid XML document with the mandated document type. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`

### isUserNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isUserNode(): Boolean
```

Returns true if this preference node is in the user preference tree, false if it's in the system preference tree.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this preference node is in the user preference tree, false if it's in the system preference tree. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun keys(): Array<String!>!
```

Returns all of the keys that have an associated value in this preference node. (The returned array will be of size zero if this node has no preferences.)

If the implementation supports *stored defaults* and there are any such defaults at this node that have not been overridden, by explicit preferences, the defaults are returned in the array in addition to any explicit preferences.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of the keys that have an associated value in this preference node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun name(): String!
```

Returns this preference node's name, relative to its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | this preference node's name, relative to its parent. |

### node

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun node(pathName: String!): Preferences!
```

Returns the named preference node in the same tree as this node, creating it and any of its ancestors if they do not already exist. Accepts a relative or absolute path name. Relative path names (which do not begin with the slash character ('/')) are interpreted relative to this preference node.

If the returned node did not exist prior to this call, this node and any ancestors that were created by this call are not guaranteed to become permanent until the flush method is called on the returned node (or one of its ancestors or descendants).

| Parameters ||
|---|---|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the path name of the preference node to return. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the specified preference node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the path name is invalid (i.e., it contains multiple consecutive slash characters, or ends with a slash character and is more than one character long). |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if path name is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#flush()`

### nodeExists

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun nodeExists(pathName: String!): Boolean
```

Returns true if the named preference node exists in the same tree as this node. Relative path names (which do not begin with the slash character ('/')) are interpreted relative to this preference node.

If this node (or an ancestor) has already been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method, it *is* legal to invoke this method, but only with the path name ""; the invocation will return false. Thus, the idiom p.nodeExists("") may be used to test whether p has been removed.

| Parameters ||
|---|---|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the path name of the node whose existence is to be checked. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the specified node exists. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the path name is invalid (i.e., it contains multiple consecutive slash characters, or ends with a slash character and is more than one character long). |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method and pathName is not the empty string (""). |
| `java.lang.NullPointerException` | if path name is null. |
| --- | --- |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

### parent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun parent(): Preferences!
```

Returns the parent of this preference node, or null if this is the root.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the parent of this preference node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun put(
    key: String!, 
    value: String!
): Unit
```

Associates the specified value with the specified key in this preference node.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the specified value is to be associated. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: value to be associated with the specified key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH or if value.length exceeds MAX_VALUE_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key or value is null. |
| --- | --- |

### putBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putBoolean(
    key: String!, 
    value: Boolean
): Unit
```

Associates a string representing the specified boolean value with the specified key in this preference node. The associated string is "true" if the value is true, and "false" if it is false. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getBoolean(kotlin.String,%20kotlin.Boolean)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getBoolean(kotlin.String,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### putByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putByteArray(
    key: String!, 
    value: ByteArray!
): Unit
```

Associates a string representing the specified byte array with the specified key in this preference node. The associated string is the *Base64* encoding of the byte array, as defined in [RFC 2045](http://www.ietf.org/rfc/rfc2045.txt), Section 6.8, with one minor change: the string will consist solely of characters from the *Base64 Alphabet* ; it will not contain any newline characters. Note that the maximum length of the byte array is limited to three quarters of MAX_VALUE_LENGTH so that the length of the Base64 encoded String does not exceed MAX_VALUE_LENGTH. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getByteArray(kotlin.String,%20kotlin.ByteArray)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH or if value.length exceeds MAX_VALUE_LENGTH\*3/4. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key or value is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getByteArray(kotlin.String,%20kotlin.ByteArray)`
- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#get(kotlin.String,%20kotlin.String)`

### putDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putDouble(
    key: String!, 
    value: Double
): Unit
```

Associates a string representing the specified double value with the specified key in this preference node. The associated string is the one that would be returned if the double value were passed to `https://developer.android.com/reference/kotlin/java/lang/Double.html#toString(kotlin.Double)`. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getDouble(kotlin.String,%20kotlin.Double)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getDouble(kotlin.String,%20kotlin.Double)`

### putFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putFloat(
    key: String!, 
    value: Float
): Unit
```

Associates a string representing the specified float value with the specified key in this preference node. The associated string is the one that would be returned if the float value were passed to `https://developer.android.com/reference/kotlin/java/lang/Float.html#toString(kotlin.Float)`. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getFloat(kotlin.String,%20kotlin.Float)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getFloat(kotlin.String,%20kotlin.Float)`

### putInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putInt(
    key: String!, 
    value: Int
): Unit
```

Associates a string representing the specified int value with the specified key in this preference node. The associated string is the one that would be returned if the int value were passed to `https://developer.android.com/reference/kotlin/java/lang/Integer.html#toString(kotlin.Int)`. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getInt(kotlin.String,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getInt(kotlin.String,%20kotlin.Int)`

### putLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putLong(
    key: String!, 
    value: Long
): Unit
```

Associates a string representing the specified long value with the specified key in this preference node. The associated string is the one that would be returned if the long value were passed to `https://developer.android.com/reference/kotlin/java/lang/Long.html#toString(kotlin.Long)`. This method is intended for use in conjunction with `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getLong(kotlin.String,%20kotlin.Long)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key with which the string form of value is to be associated. |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): value whose string form is to be associated with key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key.length() exceeds MAX_KEY_LENGTH. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#getLong(kotlin.String,%20kotlin.Long)`

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(key: String!): Unit
```

Removes the value associated with the specified key in this preference node, if any.

If this implementation supports *stored defaults*, and there is such a default for the specified preference, the stored default will be "exposed" by this call, in the sense that it will be returned by a succeeding call to get.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: key whose mapping is to be removed from the preference node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.NullPointerException` | if key is null. |

### removeNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeNode(): Unit
```

Removes this preference node and all of its descendants, invalidating any preferences contained in the removed nodes. Once a node has been removed, attempting any method other than `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#name()`, `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#absolutePath()`, `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#isUserNode()`, `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#flush()` or `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#node(kotlin.String)` on the corresponding Preferences instance will fail with an IllegalStateException. (The methods defined on `https://developer.android.com/reference/kotlin/java/lang/Object.html#` can still be invoked on a node after it has been removed; they will not throw IllegalStateException.)

The removal is not guaranteed to be persistent until the flush method is called on this node (or an ancestor).

If this implementation supports *stored defaults*, removing a node exposes any stored defaults at or below this node. Thus, a subsequent call to nodeExists on this node's path name may return true, and a subsequent call to node on this path name may return a (different) Preferences instance representing a non-empty collection of preferences and/or children.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has already been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.lang.UnsupportedOperationException` | if this method is invoked on the root node. |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#flush()`

### removeNodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeNodeChangeListener(ncl: NodeChangeListener!): Unit
```

Removes the specified NodeChangeListener, so it no longer receives change events.

| Parameters ||
|---|---|
| `ncl` | [NodeChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener)!: The NodeChangeListener to remove. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if ncl was not a registered NodeChangeListener on this node. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addNodeChangeListener(java.util.prefs.NodeChangeListener)`

### removePreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removePreferenceChangeListener(pcl: PreferenceChangeListener!): Unit
```

Removes the specified preference change listener, so it no longer receives preference change events.

| Parameters ||
|---|---|
| `pcl` | [PreferenceChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeListener)!: The preference change listener to remove. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if pcl was not a registered preference change listener on this node. |
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#addPreferenceChangeListener(java.util.prefs.PreferenceChangeListener)`

### sync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun sync(): Unit
```

Ensures that future reads from this preference node and its descendants reflect any changes that were committed to the persistent store (from any VM) prior to the sync invocation. As a side-effect, forces any changes in the contents of this preference node and its descendants to the persistent store, as if the flush method had been invoked on this node.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this node (or an ancestor) has been removed with the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#removeNode()` method. |
| `java.util.prefs.BackingStoreException` | if this operation cannot be completed due to a failure in the backing store, or inability to communicate with it. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#flush()`

### systemNodeForPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun systemNodeForPackage(c: Class<*>!): Preferences!
```

**WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the preference node from the system preference tree that is associated (by convention) with the specified class's package. The convention is as follows: the absolute path name of the node is the fully qualified package name, preceded by a slash ('/'), and with each period ('.') replaced by a slash. For example the absolute path name of the node associated with the class com.acme.widget.Foo is /com/acme/widget.

This convention does not apply to the unnamed package, whose associated preference node is \<unnamed\>. This node is not intended for long term use, but for convenience in the early development of programs that do not yet belong to a package, and for "throwaway" programs. *Valuable data should not be stored at this node as it is shared by all programs that use it.*

A class Foo wishing to access preferences pertaining to its package can obtain a preference node as follows:

```kotlin
static Preferences prefs = Preferences.systemNodeForPackage(Foo.class);
  
```
This idiom obviates the need for using a string to describe the preferences node and decreases the likelihood of a run-time failure. (If the class name is misspelled, it will typically result in a compile-time error.)

Invoking this method will result in the creation of the returned node and its ancestors if they do not already exist. If the returned node did not exist prior to this call, this node and any ancestors that were created by this call are not guaranteed to become permanent until the flush method is called on the returned node (or one of its ancestors or descendants).

| Parameters ||
|---|---|
| `c` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!: the class for whose package a system preference node is desired. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the system preference node associated with the package of which c is a member. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if c is null. |
| `java.lang.SecurityException` | if a security manager is present and it denies RuntimePermission("preferences"). |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`

### systemRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun systemRoot(): Preferences!
```

**WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the root preference node for the system.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the root preference node for the system. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager is present and it denies RuntimePermission("preferences"). |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toString(): String
```

Returns a string representation of this preferences node, as if computed by the expression:(this.isUserNode() ? "User" : "System") + " Preference Node: " + this.absolutePath().

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### userNodeForPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun userNodeForPackage(c: Class<*>!): Preferences!
```

**WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the preference node from the calling user's preference tree that is associated (by convention) with the specified class's package. The convention is as follows: the absolute path name of the node is the fully qualified package name, preceded by a slash ('/'), and with each period ('.') replaced by a slash. For example the absolute path name of the node associated with the class com.acme.widget.Foo is /com/acme/widget.

This convention does not apply to the unnamed package, whose associated preference node is \<unnamed\>. This node is not intended for long term use, but for convenience in the early development of programs that do not yet belong to a package, and for "throwaway" programs. *Valuable data should not be stored at this node as it is shared by all programs that use it.*

A class Foo wishing to access preferences pertaining to its package can obtain a preference node as follows:

```kotlin
static Preferences prefs = Preferences.userNodeForPackage(Foo.class);
  
```
This idiom obviates the need for using a string to describe the preferences node and decreases the likelihood of a run-time failure. (If the class name is misspelled, it will typically result in a compile-time error.)

Invoking this method will result in the creation of the returned node and its ancestors if they do not already exist. If the returned node did not exist prior to this call, this node and any ancestors that were created by this call are not guaranteed to become permanent until the flush method is called on the returned node (or one of its ancestors or descendants).

| Parameters ||
|---|---|
| `c` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!: the class for whose package a user preference node is desired. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the user preference node associated with the package of which c is a member. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if c is null. |
| `java.lang.SecurityException` | if a security manager is present and it denies RuntimePermission("preferences"). |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`

### userRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun userRoot(): Preferences!
```

**WARNING:** On Android, the Preference nodes corresponding to the "system" and "user" preferences are stored in sections of the file system that are inaccessible to apps. Further, allowing apps to set "system wide" preferences is contrary to android's security model. Returns the root preference node for the calling user.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences#!` | the root preference node for the calling user. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager is present and it denies RuntimePermission("preferences"). |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`
