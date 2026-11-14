# Path

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Path

```
interface Path : Comparable<Path!>, MutableIterable<Path!>, Watchable
```

| [java.nio.file.Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#) |

An object that may be used to locate a file in a file system. It will typically represent a system dependent file path.

A`Path`represents a path that is hierarchical and composed of a sequence of directory and file name elements separated by a special separator or delimiter. A*root component* , that identifies a file system hierarchy, may also be present. The name element that is*farthest* from the root of the directory hierarchy is the name of a file or directory. The other name elements are directory names. A`Path`can represent a root, a root and a sequence of names, or simply one or more name elements. A`Path`is considered to be an*empty path* if it consists solely of one name element that is empty. Accessing a file using an*empty path* is equivalent to accessing the default directory of the file system.`Path`defines the [getFileName](https://developer.android.com/reference/kotlin/java/nio/file/Path#getFileName()), [getParent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent()), [getRoot](https://developer.android.com/reference/kotlin/java/nio/file/Path#getRoot()), and [subpath](https://developer.android.com/reference/kotlin/java/nio/file/Path#subpath(kotlin.Int,%20kotlin.Int))methods to access the path components or a subsequence of its name elements.

In addition to accessing the components of a path, a`Path`also defines the [resolve](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path))and [resolveSibling](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolveSibling(java.nio.file.Path))methods to combine paths. The [relativize](https://developer.android.com/reference/kotlin/java/nio/file/Path#relativize(java.nio.file.Path))method that can be used to construct a relative path between two paths. Paths can be [compared](https://developer.android.com/reference/kotlin/java/nio/file/Path#compareTo(java.nio.file.Path)), and tested against each other using the #startsWith and #endsWith methods.

This interface extends [Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable) interface so that a directory located by a path can be #register with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService) and entries in the directory watched.

**WARNING:**This interface is only intended to be implemented by those developing custom file system implementations. Methods may be added to this interface in future releases.

## Accessing Files

Paths may be used with the [Files](https://developer.android.com/reference/kotlin/java/nio/file/Files) class to operate on files, directories, and other types of files. For example, suppose we want a to read text from a file "`access.log`". The file is located in a directory "`logs`" relative to the current working directory and is UTF-8 encoded. 

```kotlin
Path path = FileSystems.getDefault().getPath("logs", "access.log");
      BufferedReader reader = Files.newBufferedReader(path, StandardCharsets.UTF_8);
  
```

## Interoperability

Paths associated with the default are generally interoperable with the [java.io.File](https://developer.android.com/reference/kotlin/java/io/File.html#) class. Paths created by other providers are unlikely to be interoperable with the abstract path names represented by`java.io.File`. The [toPath](https://developer.android.com/reference/kotlin/java/io/File.html#toPath())method may be used to obtain a`Path`from the abstract path name represented by a`java.io.File`object. The resulting`Path`can be used to operate on the same file as the`java.io.File`object. In addition, the [toFile](https://developer.android.com/reference/kotlin/java/nio/file/Path#toFile())method is useful to construct a`File`from the`String`representation of a`Path`.

## Concurrency

Implementations of this interface are immutable and safe for use by multiple concurrent threads.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/nio/file/Path#compareTo(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Compares two abstract paths lexicographically. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [endsWith](https://developer.android.com/reference/kotlin/java/nio/file/Path#endsWith(kotlin.String))`(`other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tests if this path ends with a`Path`, constructed by converting the given path string, in exactly the manner specified by the [endsWith(Path)](https://developer.android.com/reference/kotlin/java/nio/file/Path#endsWith(java.nio.file.Path))method. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [endsWith](https://developer.android.com/reference/kotlin/java/nio/file/Path#endsWith(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Tests if this path ends with the given path. |
| --- | --- |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [getFileName](https://developer.android.com/reference/kotlin/java/nio/file/Path#getFileName())`()` Returns the name of the file or directory denoted by this path as a`Path`object. |
| abstract [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | [getFileSystem](https://developer.android.com/reference/kotlin/java/nio/file/Path#getFileSystem())`()` Returns the file system that created this object. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [getName](https://developer.android.com/reference/kotlin/java/nio/file/Path#getName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a name element of this path as a`Path`object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNameCount](https://developer.android.com/reference/kotlin/java/nio/file/Path#getNameCount())`()` Returns the number of name elements in the path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [getParent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())`()` Returns the*parent path* , or`null`if this path does not have a parent. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [getRoot](https://developer.android.com/reference/kotlin/java/nio/file/Path#getRoot())`()` Returns the root component of this path as a`Path`object, or`null`if this path does not have a root component. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbsolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())`()` Tells whether or not this path is absolute. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!\> | [iterator](https://developer.android.com/reference/kotlin/java/nio/file/Path#iterator())`()` Returns an iterator over the name elements of this path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [normalize](https://developer.android.com/reference/kotlin/java/nio/file/Path#normalize())`()` Returns a path that is this path with redundant name elements eliminated. |
| --- | --- |
| openstatic [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [of](https://developer.android.com/reference/kotlin/java/nio/file/Path#of(kotlin.String,%20kotlin.String))`(`first:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `more:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`Path`by converting a path string, or a sequence of strings that when joined form a path string. |
| openstatic [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [of](https://developer.android.com/reference/kotlin/java/nio/file/Path#of(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`)` Returns a by converting a URI. |
| abstract [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/file/Path#register(java.nio.file.WatchService,%20java.nio.file.WatchEvent.Kind))`(`watcher:` ` [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!`, `vararg` `events:` ` [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)<*>!`)` Registers the file located by this path with a watch service. |
| --- | --- |
| abstract [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/file/Path#register(java.nio.file.WatchService,%20kotlin.Array,%20java.nio.file.WatchEvent.Modifier))`(`watcher:` ` [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!`, `events:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)<*>!>!`, `vararg` `modifiers:` ` [WatchEvent.Modifier](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Modifier)!`)` Registers the file located by this path with a watch service. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [relativize](https://developer.android.com/reference/kotlin/java/nio/file/Path#relativize(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Constructs a relative path between this path and a given path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [resolve](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(kotlin.String))`(`other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a given path string to a`Path`and resolves it against this`Path`in exactly the manner specified by the [resolve](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path))method. |
| --- | --- |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [resolve](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Resolve the given path against this path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [resolveSibling](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolveSibling(kotlin.String))`(`other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a given path string to a`Path`and resolves it against this path's [parent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())path in exactly the manner specified by the [resolveSibling](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolveSibling(java.nio.file.Path))method. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [resolveSibling](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolveSibling(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Resolves the given path against this path's [parent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())path. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [startsWith](https://developer.android.com/reference/kotlin/java/nio/file/Path#startsWith(kotlin.String))`(`other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tests if this path starts with a`Path`, constructed by converting the given path string, in exactly the manner specified by the [startsWith(Path)](https://developer.android.com/reference/kotlin/java/nio/file/Path#startsWith(java.nio.file.Path))method. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [startsWith](https://developer.android.com/reference/kotlin/java/nio/file/Path#startsWith(java.nio.file.Path))`(`other:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!`)` Tests if this path starts with the given path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [subpath](https://developer.android.com/reference/kotlin/java/nio/file/Path#subpath(kotlin.Int,%20kotlin.Int))`(`beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a relative`Path`that is a subsequence of the name elements of this path. |
| --- | --- |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [toAbsolutePath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toAbsolutePath())`()` Returns a`Path`object representing the absolute path of this path. |
| abstract [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [toFile](https://developer.android.com/reference/kotlin/java/nio/file/Path#toFile())`()` Returns a [File](https://developer.android.com/reference/kotlin/java/io/File.html#) object representing this path. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | [toRealPath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toRealPath(java.nio.file.LinkOption))`(`vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!`)` Returns the*real*path of an existing file. |
| --- | --- |
| abstract [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)! | [toUri](https://developer.android.com/reference/kotlin/java/nio/file/Path#toUri())`()` Returns a URI to represent this path. |

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareTo(other: Path!): Int
```

Compares two abstract paths lexicographically. The ordering defined by this method is provider specific, and in the case of the default provider, platform specific. This method does not access the file system and neither file is required to exist.

This method may not be used to compare paths that are associated with different file system providers.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the path compared to this path. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero if the argument is [equal](https://developer.android.com/reference/kotlin/java/nio/file/Path#) to this path, a value less than zero if this path is lexicographically less than the argument, or a value greater than zero if this path is lexicographically greater than the argument |

| Exceptions ||
|----------------------------------|------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the paths are associated with different providers |

### endsWith

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endsWith(other: String!): Boolean
```

Tests if this path ends with a`Path`, constructed by converting the given path string, in exactly the manner specified by the [endsWith(Path)](https://developer.android.com/reference/kotlin/java/nio/file/Path#endsWith(java.nio.file.Path))method. On UNIX for example, the path "`foo/bar`" ends with "`foo/bar`" and "`bar`". It does not end with "`r`" or "`/bar`". Note that trailing separators are not taken into account, and so invoking this method on the`Path`"`foo/bar`" with the`String`"`bar/`" returns`true`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the given path string |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this path ends with the given path; otherwise`false` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | If the path string cannot be converted to a Path. |

### endsWith

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endsWith(other: Path!): Boolean
```

Tests if this path ends with the given path.

If the given path has*N* elements, and no root component, and this path has*N* or more elements, then this path ends with the given path if the last*N*elements of each path, starting at the element farthest from the root, are equal.

If the given path has a root component then this path ends with the given path if the root component of this path*ends with*the root component of the given path, and the corresponding elements of both paths are equal. Whether or not the root component of this path ends with the root component of the given path is file system specific. If this path does not have a root component and the given path has a root component then this path does not end with the given path.

If the given path is associated with a different`FileSystem`to this path then`false`is returned.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the given path |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this path ends with the given path; otherwise`false` |

### getFileName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFileName(): Path!
```

Returns the name of the file or directory denoted by this path as a`Path`object. The file name is the*farthest*element from the root in the directory hierarchy.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | a path representing the name of the file or directory, or`null`if this path has zero elements |

### getFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFileSystem(): FileSystem!
```

Returns the file system that created this object.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------|
| [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | the file system that created this object |

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(index: Int): Path!
```

Returns a name element of this path as a`Path`object.

The`index`parameter is the index of the name element to return. The element that is*closest* to the root in the directory hierarchy has index`0`. The element that is*farthest* from the root has index [count](https://developer.android.com/reference/kotlin/java/nio/file/Path#getNameCount())`-1`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the element |

| Return ||
|-----------------------------------------------------------------------------|------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the name element |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`index`is negative,`index`is greater than or equal to the number of elements, or this path has zero name elements |

### getNameCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNameCount(): Int
```

Returns the number of name elements in the path.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in the path, or`0`if this path only represents a root component |

### getParent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParent(): Path!
```

Returns the*parent path* , or`null`if this path does not have a parent.

The parent of this path object consists of this path's root component, if any, and each element in the path except for the*farthest* from the root in the directory hierarchy. This method does not access the file system; the path or its parent may not exist. Furthermore, this method does not eliminate special names such as "." and ".." that may be used in some implementations. On UNIX for example, the parent of "`/a/b/c`" is "`/a/b`", and the parent of`"x/y/.`" is "`x/y`". This method may be used with the [normalize](https://developer.android.com/reference/kotlin/java/nio/file/Path#normalize())method, to eliminate redundant names, for cases where*shell-like*navigation is required.

If this path has one or more elements, and no root component, then this method is equivalent to evaluating the expression: 

```kotlin
subpath(0, getNameCount()-1);
  
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | a path representing the path's parent |

### getRoot

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRoot(): Path!
```

Returns the root component of this path as a`Path`object, or`null`if this path does not have a root component.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | a path representing the root component of this path, or`null` |

### isAbsolute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAbsolute(): Boolean
```

Tells whether or not this path is absolute.

An absolute path is complete in that it doesn't need to be combined with other path information in order to locate a file.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this path is absolute |

### iterator

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<Path!>
```

Returns an iterator over the name elements of this path.

The first element returned by the iterator represents the name element that is closest to the root in the directory hierarchy, the second element is the next closest, and so on. The last element returned is the name of the file or directory denoted by this path. The [root](https://developer.android.com/reference/kotlin/java/nio/file/Path#getRoot())component, if present, is not returned by the iterator.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!> | an iterator over the name elements of this path. |

### normalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalize(): Path!
```

Returns a path that is this path with redundant name elements eliminated.

The precise definition of this method is implementation dependent but in general it derives from this path, a path that does not contain*redundant* name elements. In many file systems, the "`.`" and "`..`" are special names used to indicate the current directory and parent directory. In such file systems all occurrences of "`.`" are considered redundant. If a "`..`" is preceded by a non-"`..`" name then both names are considered redundant (the process to identify such names is repeated until it is no longer applicable).

This method does not access the file system; the path may not locate a file that exists. Eliminating "`..`" and a preceding name from a path may result in the path that locates a different file than the original path. This can arise when the preceding name is a symbolic link.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting path or this path if it does not contain redundant name elements; an empty path is returned if this path does have a root component and all name elements are redundant |

**See Also**

- [#getParent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())
- [#toRealPath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toRealPath(java.nio.file.LinkOption)) 

### of

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(
    first: String!, 
    vararg more: String!
): Path!
```

Returns a`Path`by converting a path string, or a sequence of strings that when joined form a path string. If`more`does not specify any elements then the value of the`first`parameter is the path string to convert. If`more`specifies one or more elements then each non-empty string, including`first`, is considered to be a sequence of name elements and is joined to form a path string. The details as to how the Strings are joined is provider specific but typically they will be joined using the [name-separator](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getSeparator())as the separator. For example, if the name separator is "`/`" and`getPath("/foo","bar","gus")`is invoked, then the path string`"/foo/bar/gus"`is converted to a`Path`. A`Path`representing an empty path is returned if`first`is the empty string and`more`does not contain any non-empty strings.

The`Path`is obtained by invoking the [getPath](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getPath(kotlin.String,%20kotlin.String))method of the [default](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getDefault()) [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem).

Note that while this method is very convenient, using it will imply an assumed reference to the default`FileSystem`and limit the utility of the calling code. Hence it should not be used in library code intended for flexible reuse. A more flexible alternative is to use an existing`Path`instance as an anchor, such as: 

```kotlin
<code>Path dir = ...
      Path path = dir.resolve("file");
  </code>
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `first` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path string or initial part of the path string |
| `more` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:additional strings to be joined to form the path string |

| Return ||
|-----------------------------------------------------------------------------|---------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting`Path` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | if the path string cannot be converted to a`Path` |

**See Also**

- [java.nio.file.FileSystem#getPath](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getPath(kotlin.String,%20kotlin.String)) 

### of

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(uri: URI!): Path!
```

Returns a by converting a URI.

This method iterates over the [installed](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders())providers to locate the provider that is identified by the URI [scheme](https://developer.android.com/reference/kotlin/java/net/URI.html#getScheme())of the given URI. URI schemes are compared without regard to case. If the provider is found then its [getPath](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getPath(java.net.URI))method is invoked to convert the URI.

In the case of the default provider, identified by the URI scheme "file", the given URI has a non-empty path component, and undefined query and fragment components. Whether the authority component may be present is platform specific. The returned`Path`is associated with the [default](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getDefault())file system.

The default provider provides a similar*round-trip* guarantee to the [java.io.File](https://developer.android.com/reference/kotlin/java/io/File.html#) class. For a given`Path`*p*it is guaranteed that
`Path.of(`*p* `.` [toUri](https://developer.android.com/reference/kotlin/java/nio/file/Path#toUri())`()).equals(`*p* `.` [toAbsolutePath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toAbsolutePath())`())`so long as the original`Path`, the`URI`, and the new`Path`are all created in (possibly different invocations of) the same Java virtual machine. Whether other providers make any guarantees is provider specific and therefore unspecified.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:the URI to convert |

| Return ||
|-----------------------------------------------------------------------------|---------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting`Path` |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if preconditions on the`uri`parameter do not hold. The format of the URI is provider specific. |
| `java.nio.file.FileSystemNotFoundException` | The file system, identified by the URI, does not exist and cannot be created automatically, or the provider identified by the URI's scheme component is not installed |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission to access the file system |
| --- | --- |

### register

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun register(
    watcher: WatchService!, 
    vararg events: WatchEvent.Kind<*>!
): WatchKey!
```

Registers the file located by this path with a watch service.

An invocation of this method behaves in exactly the same way as the invocation 

```kotlin
watchable.<code><a docref="java.nio.file.Path$register(java.nio.file.WatchService, kotlin.Array((java.nio.file.WatchEvent.Kind((kotlin.Any)))), kotlin.Array((java.nio.file.WatchEvent.Modifier)))">register</a></code>(watcher, events, new WatchEvent.Modifier[0]);
  
```

**Usage Example:**Suppose we wish to register a directory for entry create, delete, and modify events: 

```kotlin
Path dir = ...
      WatchService watcher = ...
 
      WatchKey key = dir.register(watcher, ENTRY_CREATE, ENTRY_DELETE, ENTRY_MODIFY);
  
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `watcher` | [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!:The watch service to which this object is to be registered |
| `events` | [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\<\*\>!:The events for which this object should be registered |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | A key representing the registration of this object with the given watch service |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If unsupported events are specified |
| `java.lang.IllegalArgumentException` | If an invalid combination of events is specified |
| `java.nio.file.ClosedWatchServiceException` | If the watch service is closed |
| --- | --- |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file. |
| `java.nio.file.NotDirectoryException` | If the file is registered to watch the entries in a directory and the file is not a directory*(optional specific exception)* |
| --- | --- |

### register

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun register(
    watcher: WatchService!, 
    events: Array<WatchEvent.Kind<*>!>!, 
    vararg modifiers: WatchEvent.Modifier!
): WatchKey!
```

Registers the file located by this path with a watch service.

In this release, this path locates a directory that exists. The directory is registered with the watch service so that entries in the directory can be watched. The`events`parameter is the events to register and may contain the following events:

- [ENTRY_CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_CREATE:java.nio.file.WatchEvent.Kind)- entry created or moved into the directory
- [ENTRY_DELETE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_DELETE:java.nio.file.WatchEvent.Kind)- entry deleted or moved out of the directory
- [ENTRY_MODIFY](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_MODIFY:java.nio.file.WatchEvent.Kind)- entry in directory was modified

The [context](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#context())for these events is the relative path between the directory located by this path, and the path that locates the directory entry that is created, deleted, or modified.

The set of events may include additional implementation specific event that are not defined by the enum [StandardWatchEventKinds](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds)

The`modifiers`parameter specifies*modifiers* that qualify how the directory is registered. This release does not define any*standard*modifiers. It may contain implementation specific modifiers.

Where a file is registered with a watch service by means of a symbolic link then it is implementation specific if the watch continues to depend on the existence of the symbolic link after it is registered.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `watcher` | [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!:the watch service to which this object is to be registered |
| `events` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\<\*\>!\>!:the events for which this object should be registered |
| `modifiers` | [WatchEvent.Modifier](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Modifier)!:the modifiers, if any, that modify how the object is registered |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | a key representing the registration of this object with the given watch service |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if unsupported events or modifiers are specified |
| `java.lang.IllegalArgumentException` | if an invalid combination of events or modifiers is specified |
| `java.nio.file.ClosedWatchServiceException` | if the watch service is closed |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file. |
| `java.nio.file.NotDirectoryException` | if the file is registered to watch the entries in a directory and the file is not a directory*(optional specific exception)* |
| --- | --- |

### relativize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun relativize(other: Path!): Path!
```

Constructs a relative path between this path and a given path.

Relativization is the inverse of [resolution](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path)). This method attempts to construct a [relative](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path that when [resolved](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path))against this path, yields a path that locates the same file as the given path. For example, on UNIX, if this path is`"/a/b"`and the given path is`"/a/b/c/d"`then the resulting relative path would be`"c/d"`. Where this path and the given path do not have a [root](https://developer.android.com/reference/kotlin/java/nio/file/Path#getRoot())component, then a relative path can be constructed. A relative path cannot be constructed if only one of the paths have a root component. Where both paths have a root component then it is implementation dependent if a relative path can be constructed. If this path and the given path are [equal](https://developer.android.com/reference/kotlin/java/nio/file/Path#) then an*empty path*is returned.

For any two [normalized](https://developer.android.com/reference/kotlin/java/nio/file/Path#normalize())paths*p* and*q* , where*q*does not have a root component,
*p* .relativize(*p* .resolve(*q* )).equals(*q* )

When symbolic links are supported, then whether the resulting path, when resolved against this path, yields a path that can be used to locate the [same](https://developer.android.com/reference/kotlin/java/nio/file/Files#isSameFile(java.nio.file.Path,%20java.nio.file.Path))file as`other`is implementation dependent. For example, if this path is`"/a/b"`and the given path is`"/a/x"`then the resulting relative path may be`"../x"`. If`"b"`is a symbolic link then is implementation dependent if`"a/b/../x"`would locate the same file as`"/a/x"`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the path to relativize against this path |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting relative path, or an empty path if both paths are equal |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`other`is not a`Path`that can be relativized against this path |

### resolve

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolve(other: String!): Path!
```

Converts a given path string to a`Path`and resolves it against this`Path`in exactly the manner specified by the [resolve](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path))method. For example, suppose that the name separator is "`/`" and a path represents "`foo/bar`", then invoking this method with the path string "`gus`" will result in the`Path`"`foo/bar/gus`".

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path string to resolve against this path |

| Return ||
|-----------------------------------------------------------------------------|--------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting path |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | if the path string cannot be converted to a Path. |

**See Also**

- [java.nio.file.FileSystem#getPath](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getPath(kotlin.String,%20kotlin.String)) 

### resolve

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolve(other: Path!): Path!
```

Resolve the given path against this path.

If the`other`parameter is an [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path then this method trivially returns`other`. If`other`is an*empty path* then this method trivially returns this path. Otherwise this method considers this path to be a directory and resolves the given path against this path. In the simplest case, the given path does not have a [root](https://developer.android.com/reference/kotlin/java/nio/file/Path#getRoot())component, in which case this method*joins*the given path to this path and returns a resulting path that #endsWith with the given path. Where the given path has a root component then resolution is highly implementation dependent and therefore unspecified.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the path to resolve against this path |

| Return ||
|-----------------------------------------------------------------------------|--------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting path |

**See Also**

- [#relativize](https://developer.android.com/reference/kotlin/java/nio/file/Path#relativize(java.nio.file.Path)) 

### resolveSibling

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolveSibling(other: String!): Path!
```

Converts a given path string to a`Path`and resolves it against this path's [parent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())path in exactly the manner specified by the [resolveSibling](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolveSibling(java.nio.file.Path))method.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path string to resolve against this path's parent |

| Return ||
|-----------------------------------------------------------------------------|--------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting path |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | if the path string cannot be converted to a Path. |

**See Also**

- [java.nio.file.FileSystem#getPath](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getPath(kotlin.String,%20kotlin.String)) 

### resolveSibling

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolveSibling(other: Path!): Path!
```

Resolves the given path against this path's [parent](https://developer.android.com/reference/kotlin/java/nio/file/Path#getParent())path. This is useful where a file name needs to be*replaced* with another file name. For example, suppose that the name separator is "`/`" and a path represents "`dir1/dir2/foo`", then invoking this method with the`Path`"`bar`" will result in the`Path`"`dir1/dir2/bar`". If this path does not have a parent path, or`other`is [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute()), then this method returns`other`. If`other`is an empty path then this method returns this path's parent, or where this path doesn't have a parent, the empty path.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the path to resolve against this path's parent |

| Return ||
|-----------------------------------------------------------------------------|--------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | the resulting path |

**See Also**

- [#resolve(Path)](https://developer.android.com/reference/kotlin/java/nio/file/Path#resolve(java.nio.file.Path)) 

### startsWith

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startsWith(other: String!): Boolean
```

Tests if this path starts with a`Path`, constructed by converting the given path string, in exactly the manner specified by the [startsWith(Path)](https://developer.android.com/reference/kotlin/java/nio/file/Path#startsWith(java.nio.file.Path))method. On UNIX for example, the path "`foo/bar`" starts with "`foo`" and "`foo/bar`". It does not start with "`f`" or "`fo`".

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the given path string |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this path starts with the given path; otherwise`false` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | If the path string cannot be converted to a Path. |

### startsWith

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startsWith(other: Path!): Boolean
```

Tests if this path starts with the given path.

This path*starts* with the given path if this path's root component*starts* with the root component of the given path, and this path starts with the same name elements as the given path. If the given path has more name elements than this path then`false`is returned.

Whether or not the root component of this path starts with the root component of the given path is file system specific. If this path does not have a root component and the given path has a root component then this path does not start with the given path.

If the given path is associated with a different`FileSystem`to this path then`false`is returned.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `other` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)!:the given path |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this path starts with the given path; otherwise`false` |

### subpath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subpath(
    beginIndex: Int, 
    endIndex: Int
): Path!
```

Returns a relative`Path`that is a subsequence of the name elements of this path.

The`beginIndex`and`endIndex`parameters specify the subsequence of name elements. The name that is*closest* to the root in the directory hierarchy has index`0`. The name that is*farthest* from the root has index [count](https://developer.android.com/reference/kotlin/java/nio/file/Path#getNameCount())`-1`. The returned`Path`object has the name elements that begin at`beginIndex`and extend to the element at index`endIndex-1`.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------|
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first element, inclusive |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the last element, exclusive |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | a new`Path`object that is a subsequence of the name elements in this`Path` |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`beginIndex`is negative, or greater than or equal to the number of elements. If`endIndex`is less than or equal to`beginIndex`, or larger than the number of elements. |

### toAbsolutePath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toAbsolutePath(): Path!
```

Returns a`Path`object representing the absolute path of this path.

If this path is already [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())then this method simply returns this path. Otherwise, this method resolves the path in an implementation dependent manner, typically by resolving the path against a file system default directory. Depending on the implementation, this method may throw an I/O error if the file system is not accessible.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | a`Path`object representing the absolute path |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOError` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and this path is not absolute, then the security manager's [checkPropertyAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkPropertyAccess(kotlin.String))method is invoked to check access to the system property`user.dir` |

### toFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toFile(): File!
```

Returns a [File](https://developer.android.com/reference/kotlin/java/io/File.html#) object representing this path. Where this`Path`is associated with the default provider, then this method is equivalent to returning a`File`object constructed with the`String`representation of this path.

If this path was created by invoking the`File` [toPath](https://developer.android.com/reference/kotlin/java/io/File.html#toPath())method then there is no guarantee that the`File`object returned by this method is [equal](https://developer.android.com/reference/kotlin/java/nio/file/Path#) to the original`File`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | a`File`object representing this path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this`Path`is not associated with the default provider |

### toRealPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toRealPath(vararg options: LinkOption!): Path!
```

Returns the*real*path of an existing file.

The precise definition of this method is implementation dependent but in general it derives from this path, an [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path that locates the [same](https://developer.android.com/reference/kotlin/java/nio/file/Files#isSameFile(java.nio.file.Path,%20java.nio.file.Path))file as this path, but with name elements that represent the actual name of the directories and the file. For example, where filename comparisons on a file system are case insensitive then the name elements represent the names in their actual case. Additionally, the resulting path has redundant name elements removed.

If this path is relative then its absolute path is first obtained, as if by invoking the [toAbsolutePath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toAbsolutePath())method.

The`options`array may be used to indicate how symbolic links are handled. By default, symbolic links are resolved to their final target. If the option [NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) is present then this method does not resolve symbolic links. Some implementations allow special names such as "`..`" to refer to the parent directory. When deriving the*real path* , and a "`..`" (or equivalent) is preceded by a non-"`..`" name then an implementation will typically cause both names to be removed. When not resolving symbolic links and the preceding name is a symbolic link then the names are only removed if it guaranteed that the resulting path will locate the same file as this path.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!:options indicating how symbolic links are handled |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path#)! | an absolute path represent the*real*path of the file located by this object |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file does not exist or an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file, and where this path is not absolute, its [checkPropertyAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkPropertyAccess(kotlin.String))method is invoked to check access to the system property`user.dir` |

### toUri

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toUri(): URI!
```

Returns a URI to represent this path.

This method constructs an absolute [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#) with a [scheme](https://developer.android.com/reference/kotlin/java/net/URI.html#getScheme())equal to the URI scheme that identifies the provider. The exact form of the scheme specific part is highly provider dependent.

In the case of the default provider, the URI is hierarchical with a [path](https://developer.android.com/reference/kotlin/java/net/URI.html#getPath())component that is absolute. The query and fragment components are undefined. Whether the authority component is defined or not is implementation dependent. There is no guarantee that the`URI`may be used to construct a [java.io.File](https://developer.android.com/reference/kotlin/java/io/File.html#). In particular, if this path represents a Universal Naming Convention (UNC) path, then the UNC server name may be encoded in the authority component of the resulting URI. In the case of the default provider, and the file exists, and it can be determined that the file is a directory, then the resulting`URI`will end with a slash.

The default provider provides a similar*round-trip* guarantee to the [java.io.File](https://developer.android.com/reference/kotlin/java/io/File.html#) class. For a given`Path`*p*it is guaranteed that
[Paths.get](https://developer.android.com/reference/kotlin/java/nio/file/Paths#get(java.net.URI))(*p* .toUri()).equals(*p* . [toAbsolutePath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toAbsolutePath())()) so long as the original`Path`, the`URI`, and the new`Path`are all created in (possibly different invocations of) the same Java virtual machine. Whether other providers make any guarantees is provider specific and therefore unspecified.

When a file system is constructed to access the contents of a file as a file system then it is highly implementation specific if the returned URI represents the given path in the file system or it represents a*compound*URI that encodes the URI of the enclosing file system. A format for compound URIs is not defined in this release; such a scheme may be added in a future release.

| Return ||
|---------------------------------------------------------------------------|--------------------------------|
| [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)! | the URI representing this path |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOError` | if an I/O error occurs obtaining the absolute path, or where a file system is constructed to access the contents of a file as a file system, and the URI of the enclosing file system cannot be obtained |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [toAbsolutePath](https://developer.android.com/reference/kotlin/java/nio/file/Path#toAbsolutePath())method throws a security exception. |
