Supposed there are different ways to implement something due to api level, implement it like this:

```java
public void foobar() {
    if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.something1) {
        // Implementation for latest api level now
    } else if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.something2) {
        // Implementation for 2nd latest api level
    } else {
        // Implementation for your min api level
    }
}
```

In the future when your minSdk increase, just delete away the old unused path.