This is mainly about theming for the entire app, however similar technique can also be applied for other styling.

### AndroidManifest.xml
```xml
<!-- Set android:theme to @style/AppTheme -->
<application
    ...
    android:theme="@style/AppTheme">
    <activity android:name=".MainActivity">
        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
    </activity>
</application>
```

### `/res/values/styles.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>

	<!-- Create a style AppTheme with parents set to Base.V0.AppTheme. The parent for -->
	<!-- AppTheme will be the the base style for this file. -->
    <style name="AppTheme" parent="Base.V0.AppTheme" />

    <!-- Create a base style Base.V0.AppTheme. This will be where we will be placing all our -->
    <!-- non api level specific attributes. Naming convention v0 means that these attributes -->
    <!-- has min api level 0 -->
    <style name="Base.V0.AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
        <!-- Non api level specific attributes -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
        <item name="android:windowBackground">@color/white</item>
    </style>

</resources>
```

### `/res/values-v19/styles.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>

	<!-- Create a style AppTheme with parents set to Base.V19.AppTheme. The parent for -->
	<!-- AppTheme will be the the base style for this file. -->
    <style name="AppTheme" parent="Base.V19.AppTheme" />

	<!-- This will inherit from the last base style. We will add new attributes specific to -->
	<!-- api level 19 here. -->
    <style name="Base.V19.AppTheme" parent="Base.V0.AppTheme">
        <!-- API 19 specific attributes -->
        <item name="android:windowTranslucentStatus">false</item>
    </style>

</resources>
```

### `/res/values-v21/styles.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>

	<!-- Create a style AppTheme with parents set to Base.V21.AppTheme. The parent for -->
	<!-- AppTheme will be the the base style for this file. -->
    <style name="AppTheme" parent="Base.V21.AppTheme" />

	<!-- This will inherit from the last base style. We will add new attributes specific to -->
	<!-- api level 21 here. -->
    <style name="Base.V21.AppTheme" parent="Base.V19.AppTheme">
        <!-- API 21 specific attributes -->
        <item name="android:windowDrawsSystemBarBackgrounds">true</item>
        <item name="android:statusBarColor">@color/colorPrimaryDark</item>
    </style>

</resources>
```