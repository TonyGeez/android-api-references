# Package

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Package

```
open class Package : AnnotatedElement
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Package](../java/lang/Package.md) |

`Package`objects contain version information about the implementation and specification of a Java package. This versioning information is retrieved and made available by the [ClassLoader](../java/lang/ClassLoader.md) instance that loaded the class(es). Typically, it is stored in the manifest that is distributed with the classes.

The set of classes that make up the package may implement a particular specification and if so the specification title, version number, and vendor strings identify that specification. An application can ask if the package is compatible with a particular version, see the [isCompatibleWith](../java/lang/Package.md))method for details.

Specification version numbers use a syntax that consists of nonnegative decimal integers separated by periods ".", for example "2.0" or "1.2.3.4.5.6.7". This allows an extensible number to be used to represent major, minor, micro, etc. versions. The version specification is described by the following formal grammar:

*SpecificationVersion:*
: *Digits RefinedVersionopt*

*RefinedVersion:*
: `.`*Digits*
: `.`*Digits RefinedVersion*

*Digits:*
: *Digit*
: *Digits*

*Digit:*
: any character for which java.lang.Character#isDigit returns`true`, e.g. 0, 1, 2, ...

The implementation title, version, and vendor strings identify an implementation and are made available conveniently to enable accurate reporting of the packages involved when a problem occurs. The contents all three implementation strings are vendor specific. The implementation version strings have no specified syntax and should only be compared for equality with desired version identifiers.

Within each`ClassLoader`instance all classes from the same java package have the same Package object. The static methods allow a package to be found by name or the set of all packages known to the current class loader to be found.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openA? | [getAnnotation](../java/lang/Package.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<A>`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getAnnotations](../java/lang/Package.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\>! | [getAnnotationsByType](../java/lang/Package.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<A>`)` <br /> |
| --- | --- |
| openA? | [getDeclaredAnnotation](../java/lang/Package.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<A>`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](../java/lang/Package.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\>! | [getDeclaredAnnotationsByType](../java/lang/Package.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<A>`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getImplementationTitle](../java/lang/Package.md))`()` Return the title of this package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getImplementationVendor](../java/lang/Package.md))`()` Returns the name of the organization, vendor or company that provided this implementation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getImplementationVersion](../java/lang/Package.md))`()` Return the version of this implementation. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/lang/Package.md))`()` Return the name of this package. |
| openstatic [Package](../java/lang/Package.md)! | [getPackage](../java/lang/Package.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Find a package by name in the callers`ClassLoader`instance. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Package](../java/lang/Package.md)!\>! | [getPackages](../java/lang/Package.md))`()` Get all the packages currently known for the caller's`ClassLoader`instance. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSpecificationTitle](../java/lang/Package.md))`()` Return the title of the specification that this package implements. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSpecificationVendor](../java/lang/Package.md))`()` Return the name of the organization, vendor, or company that owns and maintains the specification of the classes that implement this package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSpecificationVersion](../java/lang/Package.md))`()` Returns the version number of the specification that this package implements. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/Package.md))`()` Return the hash code computed from the package name. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](../java/lang/Package.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` Returns true if an annotation for the specified type is*present*on this element, else false. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompatibleWith](../java/lang/Package.md))`(`desired:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compare this package's specification version with a desired version. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSealed](../java/lang/Package.md))`()` Returns true if this package is sealed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSealed](../java/lang/Package.md))`(`url:` ` [URL](../java/net/URL.md)!`)` Returns true if this package is sealed with respect to the specified code source url. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/lang/Package.md))`()` Returns the string representation of this Package. |
| --- | --- |

## Public methods

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Annotation!> getAnnotation(annotationClass: Class<A>): A?
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>:the Class object corresponding to the annotation type |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| A? | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnnotations(): Array<Annotation!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations present on this element |

### getAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Annotation!> getAnnotationsByType(annotationClass: Class<A>): Array<A>!
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<A>! | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Annotation!> getDeclaredAnnotation(annotationClass: Class<A>): A?
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>:the Class object corresponding to the annotation type |

| Return ||
|----|------------------------------------------------------------------------------------------------------------|
| A? | this element's annotation for the specified annotation type if directly present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeclaredAnnotations(): Array<Annotation!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaredAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Annotation!> getDeclaredAnnotationsByType(annotationClass: Class<A>): Array<A>!
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly or indirectly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<A\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<A>! | all this element's annotations for the specified annotation type if directly or indirectly present on this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getImplementationTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImplementationTitle(): String!
```

Return the title of this package.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the title of the implementation, null is returned if it is not known. |

### getImplementationVendor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImplementationVendor(): String!
```

Returns the name of the organization, vendor or company that provided this implementation.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the vendor that implemented this package.. |

### getImplementationVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImplementationVersion(): String!
```

Return the version of this implementation. It consists of any string assigned by the vendor of this implementation and does not have any particular syntax specified or expected by the Java runtime. It may be compared for equality with other package version strings used for this implementation by this vendor for this package.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the version of the implementation, null is returned if it is not known. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Return the name of this package.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The fully-qualified name of this package as defined in section 6.5.3 of The Java™ Language Specification, for example,`java.lang` |

### getPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPackage(name: String!): Package!
```

Find a package by name in the callers`ClassLoader`instance. The callers`ClassLoader`instance is used to find the package instance corresponding to the named class. If the callers`ClassLoader`instance is null then the set of packages loaded by the system`ClassLoader`instance is searched to find the named package.

Packages have attributes for versions and specifications only if the class loader created the package instance with the appropriate attributes. Typically, those attributes are defined in the manifests that accompany the classes.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a package name, for example, java.lang. |

| Return ||
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Package](../java/lang/Package.md)! | the package of the requested name. It may be null if no package information is available from the archive or codebase. |

### getPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPackages(): Array<Package!>!
```

Get all the packages currently known for the caller's`ClassLoader`instance. Those packages correspond to classes loaded via or accessible by name to that`ClassLoader`instance. If the caller's`ClassLoader`instance is the bootstrap`ClassLoader`instance, which may be represented by`null`in some implementations, only packages corresponding to classes loaded by the bootstrap`ClassLoader`instance will be returned.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Package](../java/lang/Package.md)!>! | a new array of packages known to the callers`ClassLoader`instance. An zero length array is returned if none are known. |

### getSpecificationTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpecificationTitle(): String!
```

Return the title of the specification that this package implements.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the specification title, null is returned if it is not known. |

### getSpecificationVendor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpecificationVendor(): String!
```

Return the name of the organization, vendor, or company that owns and maintains the specification of the classes that implement this package.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the specification vendor, null is returned if it is not known. |

### getSpecificationVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpecificationVersion(): String!
```

Returns the version number of the specification that this package implements. This version string must be a sequence of nonnegative decimal integers separated by "."'s and may have leading zeros. When version strings are compared the most significant numbers are compared.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the specification version, null is returned if it is not known. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Return the hash code computed from the package name.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code computed from the package name. |

### isAnnotationPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAnnotationPresent(annotationClass: Class<out Annotation!>): Boolean
```

Returns true if an annotation for the specified type is*present*on this element, else false. This method is designed primarily for convenient access to marker annotations.

The truth value returned by this method is equivalent to:`getAnnotation(annotationClass) != null`

The body of the default method is specified to be the code above.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `annotationClass` | [Class](../java/lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isCompatibleWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCompatibleWith(desired: String!): Boolean
```

Compare this package's specification version with a desired version. It returns true if this packages specification version number is greater than or equal to the desired version number.

Version numbers are compared by sequentially comparing corresponding components of the desired and specification strings. Each component is converted as a decimal integer and the values compared. If the specification value is greater than the desired value true is returned. If the value is less false is returned. If the values are equal the period is skipped and the next pair of components is compared.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `desired` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the version string of the desired version. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this package's version number is greater than or equal to the desired version number |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------|
| `java.lang.NumberFormatException` | if the desired or current version is not of the correct dotted form. |

### isSealed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSealed(): Boolean
```

Returns true if this package is sealed.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the package is sealed, false otherwise |

### isSealed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSealed(url: URL!): Boolean
```

Returns true if this package is sealed with respect to the specified code source url.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `url` | [URL](../java/net/URL.md)!:the code source url |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this package is sealed with respect to url |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the string representation of this Package. Its value is the string "package " and the package name. If the package title is defined it is appended. If the package version is defined it is appended.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of the package. |
