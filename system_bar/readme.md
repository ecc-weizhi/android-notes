`<item name="android:windowTranslucentStatus">true</item>`

Available only from api level 19 onward. When set to true, system bar will be grayish translucent and Views will be drawn behind system bar. False by default.

***

`<item name="android:windowDrawsSystemBarBackgrounds">true</item>`

Available only from api level 21 onward. When set to true, `android:statusBarColor` will be applied. True by default.

***

`<item name="android:statusBarColor">#0000ff</item>`

Available only from api level 21 onward. Set system bar color to the given color. Has no effect if `android:windowTranslucentStatus` is true.

***

`android:fitsSystemWindows="true"` is useless by itself. `android:fitsSystemWindows="true"` works for some layouts like `CoordinatorLayout` and `DrawerLayout` because they have some if-else logic to check for `android:fitsSystemWindows` and apply some additional paddings.