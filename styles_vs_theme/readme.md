### Declaring styles and themes

Both are declared in the same way usually in `styles.xml`.

This is a theme:
```xml
<style name="Base.V0.AppTheme" parent="Theme.MaterialComponents.DayNight.NoActionBar">
    <!-- Non api level specific attributes -->
    <item name="colorPrimary">@color/colorPrimary</item>
    <item name="colorPrimaryVariant">@color/colorPrimaryVariant</item>
    <item name="colorSecondary">@color/colorSecondary</item>
    <item name="colorSecondaryVariant">@color/colorSecondaryVariant</item>
    <item name="android:colorBackground">@color/colorBackground</item>
    <item name="colorSurface">@color/colorSurface</item>
    <item name="colorError">@color/colorError</item>
    <item name="colorOnPrimary">@color/colorOnPrimary</item>
    <item name="colorOnSecondary">@color/colorOnSecondary</item>
    <item name="colorOnBackground">@color/colorOnBackground</item>
    <item name="colorOnSurface">@color/colorOnSurface</item>
    <item name="colorOnError">@color/colorOnError</item>

    <item name="drawerArrowStyle">@style/DrawerArrowStyle</item>
</style>
```

This is a style:
```xml
<style name="BottomButtonStyle">
    <item name="android:background">?attr/colorPrimary</item>
    <item name="android:foreground">?selectableItemBackground</item>
    <item name="android:gravity">center</item>
    <item name="android:textAllCaps">true</item>
    <item name="android:textColor">?attr/colorOnPrimary</item>
    <item name="android:textSize">@dimen/text_bigger</item>
</style>
```

### Using styles and themes

- A Theme and Style declaration is indistinguishable from the app/IDE/compiler perspective. the difference lies in how they are used.

In this example, MyTheme can contain both theme attributes such as `colorPrimary` and view's attribute such as `android:orientation`. Both theme attributes and view's attributes will be applied to LinearLayout itself and childView of LinearLayout.
```xml
<LinearLayout android:theme="@style/MyTheme">
    
    <!-- Anything here will also have a MyTheme applied -->
    
</LinearLayout>
```

In this example, MyStyle can only contain view's attribute (you can have theme attributes in MyStyle but they will not be applied). MyStyle will be applied only to LinearLayout itself.
```xml
<LinearLayout style="@style/MyStyle">

	<!-- Anything here will NOT have MyStyle applied -->
    
</LinearLayout>
```