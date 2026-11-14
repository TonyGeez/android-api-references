# Uri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Uri

Kotlin| [Java](Uri.md) 
| --- | --- |

```
abstract class Uri : Comparable<Uri!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.Uri](Uri.md) |

Immutable URI reference. A URI reference includes a URI and a fragment, the component of the URI following a '#'. Builds and parses URI references which conform to [RFC 2396](http://www.faqs.org/rfcs/rfc2396.html).

In the interest of performance, this class performs little to no validation. Behavior is undefined for invalid input. This class is very forgiving--in the face of invalid input, it will return garbage rather than throw an exception unless otherwise specified.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/Uri.Builder.md) Helper class for building or manipulating URI references. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Uri.Builder](../android/net/Uri.Builder.md)! | [buildUpon](Uri.md))`()` Constructs a new builder, copying the attributes from this Uri. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Uri.md))`(`other:` ` [Uri](Uri.md)!`)` Compares the string representation of this Uri with that of another. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [decode](Uri.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Decodes '%'-escaped octets in the given string using the UTF-8 scheme. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [encode](Uri.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes characters in the given string as '%'-escaped octets using the UTF-8 scheme. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [encode](Uri.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `allow:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes characters in the given string as '%'-escaped octets using the UTF-8 scheme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Uri.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this Uri to another object for equality. |
| --- | --- |
| openstatic [Uri](Uri.md)! | [fromFile](Uri.md))`(`file:` ` [File](../java.io/File.md)!`)` Creates a Uri from a file. |
| openstatic [Uri](Uri.md)! | [fromParts](Uri.md))`(`scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ssp:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an opaque Uri from the given components. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getAuthority](Uri.md))`()` Gets the decoded authority part of this URI. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBooleanQueryParameter](Uri.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Searches the query string for the first value with the given key and interprets it as a boolean value. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEncodedAuthority](Uri.md))`()` Gets the encoded authority part of this URI. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEncodedFragment](Uri.md))`()` Gets the encoded fragment part of this URI, everything after the '#'. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEncodedPath](Uri.md))`()` Gets the encoded path. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEncodedQuery](Uri.md))`()` Gets the encoded query component from this URI. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncodedSchemeSpecificPart](Uri.md))`()` Gets the scheme-specific part of this URI, i. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEncodedUserInfo](Uri.md))`()` Gets the encoded user information from the authority. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFragment](Uri.md))`()` Gets the decoded fragment part of this URI, everything after the '#'. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHost](Uri.md))`()` Gets the encoded host from the authority for this URI. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getLastPathSegment](Uri.md))`()` Gets the decoded last segment in the path. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPath](Uri.md))`()` Gets the decoded path. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPathSegments](Uri.md))`()` Gets the decoded path segments. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](Uri.md))`()` Gets the port from the authority for this URI. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getQuery](Uri.md))`()` Gets the decoded query component from this URI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getQueryParameter](Uri.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Searches the query string for the first value with the given key. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getQueryParameterNames](Uri.md))`()` Returns a set of the unique names of all query parameters. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getQueryParameters](Uri.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Searches the query string for parameter values with the given key. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getScheme](Uri.md))`()` Gets the scheme of this URI. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSchemeSpecificPart](Uri.md))`()` Gets the scheme-specific part of this URI, i. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUserInfo](Uri.md))`()` Gets the decoded user information from the authority. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Uri.md))`()` Hashes the encoded string represention of this Uri consistently with [equals(java.lang.Object)](Uri.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbsolute](Uri.md))`()` Returns true if this URI is absolute, i. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHierarchical](Uri.md))`()` Returns true if this URI is hierarchical like "http://google. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](Uri.md))`()` Returns true if this URI is opaque like "mailto:nobody@google. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRelative](Uri.md))`()` Returns true if this URI is relative, i. |
| open [Uri](Uri.md)! | [normalizeScheme](Uri.md))`()` Return an equivalent URI with a lowercase scheme component. |
| openstatic [Uri](Uri.md)! | [parse](Uri.md))`(`uriString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a Uri which parses the given encoded URI string. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Uri.md))`()` Returns the encoded string representation of this URI. |
| openstatic [Uri](Uri.md)! | [withAppendedPath](Uri.md))`(`baseUri:` ` [Uri](Uri.md)!`, `pathSegment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new Uri by appending an already-encoded path segment to a base Uri. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Uri.md))`(`out:` ` [Parcel](../android.os/Parcel.md)!`, `uri:` ` [Uri](Uri.md)!`)` Writes a Uri to a Parcel. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android.os/Parcelable.md))`()` <br /> Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android.os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android.os/Parcelable.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Uri](Uri.md)!\> | [CREATOR](Uri.md) Reads Uris from Parcels. |
| static [Uri](Uri.md)! | [EMPTY](Uri.md) The empty URI, equivalent to "". |

## Public methods

### buildUpon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun buildUpon(): Uri.Builder!
```

Constructs a new builder, copying the attributes from this Uri. 

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: Uri!): Int
```

Compares the string representation of this Uri with that of another.

| Parameters ||
|-----|----------------------------|
| `o` | the object to be compared. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decode(s: String!): String!
```

Decodes '%'-escaped octets in the given string using the UTF-8 scheme. Replaces invalid octets with the unicode replacement character ("\\\\uFFFD").

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:encoded string to decode |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the given string with escaped octets decoded, or null if s is null |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encode(s: String!): String!
```

Encodes characters in the given string as '%'-escaped octets using the UTF-8 scheme. Leaves letters ("A-Z", "a-z"), numbers ("0-9"), and unreserved characters ("_-!.\~'()\*") intact. Encodes all other characters.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to encode |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | an encoded version of s suitable for use as a URI component, or null if s is null |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encode(
    s: String!, 
    allow: String!
): String!
```

Encodes characters in the given string as '%'-escaped octets using the UTF-8 scheme. Leaves letters ("A-Z", "a-z"), numbers ("0-9"), and unreserved characters ("_-!.\~'()\*") intact. Encodes all other characters with the exception of those specified in the allow argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to encode |
| `allow` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:set of additional characters to allow in the encoded form, null if no characters should be skipped |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | an encoded version of s suitable for use as a URI component, or null if s is null |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this Uri to another object for equality. Returns true if the encoded string representations of this Uri and the given Uri are equal. Case counts. Paths are not normalized. If one Uri specifies a default port explicitly and the other leaves it implicit, they will not be considered equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### fromFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromFile(file: File!): Uri!
```

Creates a Uri from a file. The URI has the form "file://". Encodes path characters with the exception of '/'.

Example: "file:///tmp/android.txt"

<br />

| Return ||
|-------------------------------------------------------------------------|--------------------------|
| [Uri](Uri.md)! | a Uri for the given file |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if file is null |

### fromParts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromParts(
    scheme: String!, 
    ssp: String!, 
    fragment: String!
): Uri!
```

Creates an opaque Uri from the given components. Encodes the ssp which means this method cannot be used to create hierarchical URIs.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of the URI |
| `ssp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:scheme-specific-part, everything between the scheme separator (':') and the fragment separator ('#'), which will get encoded |
| `fragment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:fragment, everything after the '#', null if undefined, will get encoded |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------|-----------------------------------------------------|
| [Uri](Uri.md)! | Uri composed of the given scheme, ssp, and fragment |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if scheme or ssp is null |

**See Also**

- [android.net.Uri.Builder](../android/net/Uri.Builder.md) 

### getAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAuthority(): String?
```

Gets the decoded authority part of this URI. For server addresses, the authority is structured as follows:`[ userinfo '@' ] host [ ':' port ]`

Examples: "google.com", "bob@google.com:80"

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the authority for this URI or null if not present |

### getBooleanQueryParameter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBooleanQueryParameter(
    key: String!, 
    defaultValue: Boolean
): Boolean
```

Searches the query string for the first value with the given key and interprets it as a boolean value. "false" and "0" are interpreted as`false`, everything else is interpreted as`true`.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:which will be decoded |
| `defaultValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the default value to return if there is no query parameter for key |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the boolean interpretation of the query parameter key |

### getEncodedAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedAuthority(): String?
```

Gets the encoded authority part of this URI. For server addresses, the authority is structured as follows:`[ userinfo '@' ] host [ ':' port ]`

Examples: "google.com", "bob@google.com:80"

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the authority for this URI or null if not present |

### getEncodedFragment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedFragment(): String?
```

Gets the encoded fragment part of this URI, everything after the '#'.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the encoded fragment or null if there isn't one |

### getEncodedPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedPath(): String?
```

Gets the encoded path.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the encoded path, or null if this is not a hierarchical URI (like "mailto:nobody@google.com") or the URI is invalid |

### getEncodedQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedQuery(): String?
```

Gets the encoded query component from this URI. The query comes after the query separator ('?') and before the fragment separator ('#'). This method would return "q=android" for "http://www.google.com/search?q=android".

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the encoded query or null if there isn't one |

### getEncodedSchemeSpecificPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedSchemeSpecificPart(): String!
```

Gets the scheme-specific part of this URI, i.e. everything between the scheme separator ':' and the fragment separator '#'. If this is a relative URI, this method returns the entire URI. Leaves escaped octets intact.

Example: "//www.google.com/search?q=android"

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the encoded scheme-specific-part |

### getEncodedUserInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodedUserInfo(): String?
```

Gets the encoded user information from the authority. For example, if the authority is "nobody@google.com", this method will return "nobody".

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the user info for this URI or null if not present |

### getFragment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFragment(): String?
```

Gets the decoded fragment part of this URI, everything after the '#'.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the decoded fragment or null if there isn't one |

### getHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHost(): String?
```

Gets the encoded host from the authority for this URI. For example, if the authority is "bob@google.com", this method will return "google.com".

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the host for this URI or null if not present |

### getLastPathSegment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLastPathSegment(): String?
```

Gets the decoded last segment in the path.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the decoded last segment or null if the path is empty |

### getPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPath(): String?
```

Gets the decoded path.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the decoded path, or null if this is not a hierarchical URI (like "mailto:nobody@google.com") or the URI is invalid |

### getPathSegments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPathSegments(): MutableList<String!>!
```

Gets the decoded path segments.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | decoded path segments, each without a leading or trailing '/' |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPort(): Int
```

Gets the port from the authority for this URI. For example, if the authority is "google.com:80", this method will return 80.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port for this URI or -1 if invalid or not present |

### getQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getQuery(): String?
```

Gets the decoded query component from this URI. The query comes after the query separator ('?') and before the fragment separator ('#'). This method would return "q=android" for "http://www.google.com/search?q=android".

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the decoded query or null if there isn't one |

### getQueryParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueryParameter(key: String!): String?
```

Searches the query string for the first value with the given key.

**Warning:**Prior to Jelly Bean, this decoded the '+' character as '+' rather than ' '.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:which will be encoded |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the decoded value or null if no parameter is found |

| Exceptions ||
|-------------------------------------------|----------------------------------|
| `java.lang.UnsupportedOperationException` | if this isn't a hierarchical URI |
| `java.lang.NullPointerException` | if key is null |

### getQueryParameterNames

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueryParameterNames(): MutableSet<String!>!
```

Returns a set of the unique names of all query parameters. Iterating over the set will return the names in order of their first occurrence.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a set of decoded names |

| Exceptions ||
|-------------------------------------------|----------------------------------|
| `java.lang.UnsupportedOperationException` | if this isn't a hierarchical URI |

### getQueryParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQueryParameters(key: String!): MutableList<String!>!
```

Searches the query string for parameter values with the given key.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:which will be encoded |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a list of decoded values |

| Exceptions ||
|-------------------------------------------|----------------------------------|
| `java.lang.UnsupportedOperationException` | if this isn't a hierarchical URI |
| `java.lang.NullPointerException` | if key is null |

### getScheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getScheme(): String?
```

Gets the scheme of this URI. Example: "http"

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the scheme or null if this is a relative URI |

### getSchemeSpecificPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSchemeSpecificPart(): String!
```

Gets the scheme-specific part of this URI, i.e. everything between the scheme separator ':' and the fragment separator '#'. If this is a relative URI, this method returns the entire URI. Decodes escaped octets.

Example: "//www.google.com/search?q=android"

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the decoded scheme-specific-part |

### getUserInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUserInfo(): String?
```

Gets the decoded user information from the authority. For example, if the authority is "nobody@google.com", this method will return "nobody".

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the user info for this URI or null if not present |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Hashes the encoded string represention of this Uri consistently with [equals(java.lang.Object)](Uri.md)).

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isAbsolute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAbsolute(): Boolean
```

Returns true if this URI is absolute, i.e. if it contains an explicit scheme.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this URI is absolute, false if it's relative |

### isHierarchical

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isHierarchical(): Boolean
```

Returns true if this URI is hierarchical like "http://google.com". Absolute URIs are hierarchical if the scheme-specific part starts with a '/'. Relative URIs are always hierarchical. 

### isOpaque

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpaque(): Boolean
```

Returns true if this URI is opaque like "mailto:nobody@google.com". The scheme-specific part of an opaque URI cannot start with a '/'. 

### isRelative

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRelative(): Boolean
```

Returns true if this URI is relative, i.e. if it doesn't contain an explicit scheme.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this URI is relative, false if it's absolute |

### normalizeScheme

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun normalizeScheme(): Uri!
```

Return an equivalent URI with a lowercase scheme component. This aligns the Uri with Android best practices for intent filtering.

For example, "HTTP://www.android.com" becomes "http://www.android.com"

All URIs received from outside Android (such as user input, or external sources like Bluetooth, NFC, or the Internet) should be normalized before they are used to create an Intent.

This method does*not*validate bad URIs, or 'fix' poorly formatted URIs - so do not use it for input validation. A Uri will always be returned, even if the Uri is badly formatted to begin with and a scheme component cannot be found.

| Return ||
|-------------------------------------------------------------------------|-----------------------------|
| [Uri](Uri.md)! | normalized Uri (never null) |

**See Also**

- [android.content.Intent#setData](../android.content/Intent.md))
- [android.content.Intent#setDataAndNormalize](../android.content/Intent.md)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(uriString: String!): Uri!
```

Creates a Uri which parses the given encoded URI string.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `uriString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an RFC 2396-compliant, encoded URI |

| Return ||
|-------------------------------------------------------------------------|-------------------------------|
| [Uri](Uri.md)! | Uri for this given uri string |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if uriString is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toString(): String
```

Returns the encoded string representation of this URI. Example: "http://google.com/"

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### withAppendedPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withAppendedPath(
    baseUri: Uri!, 
    pathSegment: String!
): Uri!
```

Creates a new Uri by appending an already-encoded path segment to a base Uri.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `baseUri` | [Uri](Uri.md)!:Uri to append path segment to |
| `pathSegment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:encoded path segment to append |

| Return ||
|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Uri](Uri.md)! | a new Uri based on baseUri with the given segment appended to the path |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if baseUri is null |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeToParcel(
    out: Parcel!, 
    uri: Uri!
): Unit
```

Writes a Uri to a Parcel.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `out` | [Parcel](../android.os/Parcel.md)!:parcel to write to |
| `uri` | [Uri](Uri.md)!:to write, can be null |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Uri!>
```

Reads Uris from Parcels. 

### EMPTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMPTY: Uri!
```

The empty URI, equivalent to "".
