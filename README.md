# ThemeDemo

<img src="https://raw.githubusercontent.com/PuniCharana/ThemeDemo/master/images/theme_demo.png" alt="Theme Demo" width="300px">

## Issues

1. **StatusBar** background becomes white  

<img src="https://raw.githubusercontent.com/PuniCharana/ThemeDemo/master/images/scrolling.png" alt="Theme Demo" width="300px">

2. **Title and back button** is not visible 

<img src="https://raw.githubusercontent.com/PuniCharana/ThemeDemo/master/images/settings.png" alt="Theme Demo" width="300px">

## Solution

```xml
<resources>
    <!-- Base application theme. -->

    <!-- Solution 1. change Theme.AppCompat.DarkActionBar to Theme.AppCompat.Light-->

    <style name="AppTheme" parent="Theme.AppCompat.Light">
        <!-- Customize your theme here. -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>

        <!-- Solution 2. add textColorPrimary-->
        <item name="android:textColorPrimary">@color/colorAccent</item>

        <item name="android:windowLightStatusBar">true</item>
    </style>

    <style name="AppTheme.NoActionBar">
        <item name="windowActionBar">false</item>
        <item name="windowNoTitle">true</item>
        <item name="android:statusBarColor">@android:color/transparent</item>
    </style>

    <style name="AppTheme.AppBarOverlay" parent="ThemeOverlay.AppCompat.Dark.ActionBar">
    	<!-- Solution 2. add textColorPrimary-->
        <item name="android:textColorPrimary">@color/colorAccent</item>
    </style>

    <style name="AppTheme.PopupOverlay" parent="ThemeOverlay.AppCompat.Light">
        <!-- Solution 2. add textColorPrimary-->
        <item name="android:textColorPrimary">@color/colorAccent</item>
    </style>

</resources>
```

<img src="https://raw.githubusercontent.com/PuniCharana/ThemeDemo/master/images/solution_scrolling.png" alt="Theme Demo" width="300px">


<img src="https://raw.githubusercontent.com/PuniCharana/ThemeDemo/master/images/solution_settings.png" alt="Theme Demo" width="300px">