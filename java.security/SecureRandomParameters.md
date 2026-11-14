# SecureRandomParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureRandomParameters

```
interface SecureRandomParameters
```

| [java.security.SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters#) |

| Known Direct Subclasses [DrbgParameters.Instantiation](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.Instantiation), [DrbgParameters.NextBytes](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.NextBytes), [DrbgParameters.Reseed](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.Reseed) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------| | [DrbgParameters.Instantiation](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.Instantiation) | DRBG parameters for instantiation. | | [DrbgParameters.NextBytes](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.NextBytes) | DRBG parameters for random bits generation. | | [DrbgParameters.Reseed](https://developer.android.com/reference/kotlin/java/security/DrbgParameters.Reseed) | DRBG parameters for reseed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for parameters used in various`SecureRandom`methods.

Some`SecureRandom`implementations might require additional operational parameters. Objects of classes which implement this interface can be passed to those implementations that support them.

## Summary
