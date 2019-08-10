## `api` vs `implementation`

Supposed we have 3 module: `app`, `mylibrary` and `internallibrary`.

`app\build.gradle`
```
dependencies {
    implementation 'app.eccweizhi:mylibrary:1.0'
}
```

`mylibrary\build.gradle`
```
dependencies {
    implementation 'app.eccweizhi:internallibrary:1.0'
}
```

1. `app` will not be able to access `internallibrary`
2. When `internallibrary` code changes, `app` will not need to be recompiled.

***

Supposed we have 3 module: `app`, `mylibrary` and `internallibrary`.

`app\build.gradle`
```
dependencies {
    implementation 'app.eccweizhi:mylibrary:1.0'
}
```

`mylibrary\build.gradle`
```
dependencies {
    api 'app.eccweizhi:internallibrary:1.0'
}
```

1. `app` will be able to access `internallibrary`.
2. When `internallibrary` code changes, `app` will need to be recompiled. 