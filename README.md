# Repro steps

1. `./gradlew compileKotlin --rerun`

## Expected

no warnings

## Actual

false positive warning:

```
$ ./gradlew compileKotlin --rerun
> Task :checkKotlinGradlePluginConfigurationErrors SKIPPED

> Task :compileKotlin
w: file:///usr/local/google/home/aurimas/Code/temp/kotlin-can-be-val-repro/src/main/kotlin/Repro.kt:3:9 This 'var' property is never written to, it can be declared as 'val'.
```
