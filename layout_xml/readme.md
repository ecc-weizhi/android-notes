## Using `<include>` tag

Supposed we have this:

```xml
<include
    android:id="@+id/mainContentLayout"
    android:background="@color/amber_200"
    layout="@layout/activity_main_content"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

- LayoutParams attributes like `android:layout_something` in `@layout/activity_main_content` will be ignored.
- LayoutParams attributes like `android:layout_something` in `<include>` tag will take effect.
- `android:id` in both `<include>` tag and `@layout/activity_main_content` will be applied. `android:id` in `<include>` tag will overwrite `android:id` in `@layout/activity_main_content`.
- Non LayoutParams attributes in `<include>` tag will have no effect.
