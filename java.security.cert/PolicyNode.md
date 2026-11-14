# PolicyNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicyNode

```
interface PolicyNode
```

| [java.security.cert.PolicyNode](PolicyNode.md) |

An immutable valid policy tree node as defined by the PKIX certification path validation algorithm.

One of the outputs of the PKIX certification path validation algorithm is a valid policy tree, which includes the policies that were determined to be valid, how this determination was reached, and any policy qualifiers encountered. This tree is of depth*n* , where*n*is the length of the certification path that has been validated.

Most applications will not need to examine the valid policy tree. They can achieve their policy processing goals by setting the policy-related parameters in`PKIXParameters`. However, the valid policy tree is available for more sophisticated applications, especially those that process policy qualifiers.

[PKIXCertPathValidatorResult.getPolicyTree](PKIXCertPathValidatorResult.md))returns the root node of the valid policy tree. The tree can be traversed using the [getChildren](PolicyNode.md))and [getParent](PolicyNode.md))methods. Data about a particular node can be retrieved using other methods of`PolicyNode`.

**Concurrent Access**

All`PolicyNode`objects must be immutable and thread-safe. Multiple threads may concurrently invoke the methods defined in this class on a single`PolicyNode`object (or more than one) with no ill effects. This stipulation applies to all public fields and methods of this class and any added or overridden by subclasses.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [PolicyNode](PolicyNode.md)!\>! | [getChildren](PolicyNode.md))`()` Returns an iterator over the children of this node. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDepth](PolicyNode.md))`()` Returns the depth of this node in the valid policy tree. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getExpectedPolicies](PolicyNode.md))`()` Returns the set of expected policies that would satisfy this node's valid policy in the next certificate to be processed. |
| --- | --- |
| abstract [PolicyNode](PolicyNode.md)! | [getParent](PolicyNode.md))`()` Returns the parent of this node, or`null`if this is the root node. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [PolicyQualifierInfo](PolicyQualifierInfo.md)!\>! | [getPolicyQualifiers](PolicyNode.md))`()` Returns the set of policy qualifiers associated with the valid policy represented by this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValidPolicy](PolicyNode.md))`()` Returns the valid policy represented by this node. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCritical](PolicyNode.md))`()` Returns the criticality indicator of the certificate policy extension in the most recently processed certificate. |

## Public methods

### getChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildren(): MutableIterator<PolicyNode!>!
```

Returns an iterator over the children of this node. Any attempts to modify the children of this node through the`Iterator`'s remove method must throw an`UnsupportedOperationException`.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [PolicyNode](PolicyNode.md)!>! | an iterator over the children of this node |

### getDepth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDepth(): Int
```

Returns the depth of this node in the valid policy tree.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the depth of this node (0 for the root node, 1 for its children, and so on) |

### getExpectedPolicies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getExpectedPolicies(): MutableSet<String!>!
```

Returns the set of expected policies that would satisfy this node's valid policy in the next certificate to be processed.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an immutable`Set`of expected policy`String`OIDs. For the root node, this method always returns a`Set`with one element, the special anyPolicy OID: "2.5.29.32.0". |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParent(): PolicyNode!
```

Returns the parent of this node, or`null`if this is the root node.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [PolicyNode](PolicyNode.md)! | the parent of this node, or`null`if this is the root node |

### getPolicyQualifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPolicyQualifiers(): MutableSet<out PolicyQualifierInfo!>!
```

Returns the set of policy qualifiers associated with the valid policy represented by this node.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [PolicyQualifierInfo](PolicyQualifierInfo.md)!>! | an immutable`Set`of`PolicyQualifierInfo`s. For the root node, this is always an empty`Set`. |

### getValidPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValidPolicy(): String!
```

Returns the valid policy represented by this node.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the`String`OID of the valid policy represented by this node. For the root node, this method always returns the special anyPolicy OID: "2.5.29.32.0". |

### isCritical

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCritical(): Boolean
```

Returns the criticality indicator of the certificate policy extension in the most recently processed certificate.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if extension marked critical,`false`otherwise. For the root node,`false`is always returned. |
