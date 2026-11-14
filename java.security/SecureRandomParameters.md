# SecureRandomParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureRandomParameters

```
interface SecureRandomParameters
```

| [java.security.SecureRandomParameters](SecureRandomParameters.md) |

| Known Direct Subclasses [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md), [DrbgParameters.NextBytes](../java/security/DrbgParameters.NextBytes.md), [DrbgParameters.Reseed](../java/security/DrbgParameters.Reseed.md) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------| | [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md) | DRBG parameters for instantiation. | | [DrbgParameters.NextBytes](../java/security/DrbgParameters.NextBytes.md) | DRBG parameters for random bits generation. | | [DrbgParameters.Reseed](../java/security/DrbgParameters.Reseed.md) | DRBG parameters for reseed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A marker interface for parameters used in various`SecureRandom`methods.

Some`SecureRandom`implementations might require additional operational parameters. Objects of classes which implement this interface can be passed to those implementations that support them.

## Summary
