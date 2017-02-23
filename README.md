# Prefs
[![](https://jitpack.io/v/GrenderG/Prefs.svg)](https://jitpack.io/#GrenderG/Prefs) [![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Prefs-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/3570)

Simple Android `SharedPreferences` wrapper.

Repository
--

Add this in your root `build.gradle` file (**not** your module `build.gradle` file):

```gradle
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```

Dependency
--

Add this to your module's `build.gradle` file (make sure the version matches the JitPack badge above):

```gradle
dependencies {
	...
	compile 'com.github.GrenderG:Prefs:1.2'
}
```

Usage
--
This is the basic usage, you can read values (specifying a default value or not) and write values like so:
``` java
  Prefs.with(yourContext).readInt(YOUR_KEY_VALUE);
  Prefs.with(yourContext).readInt(YOUR_KEY_VALUE, defaultValue);
  
  Prefs.with(yourContext).writeInt(YOUR_KEY_VALUE, valueToStore);
```
You can also specify a custom name for the preferences' name:
``` java
  Prefs.with(yourContext, "CUSTOM_NAME").readInt(YOUR_KEY_VALUE);
```
And force the re-instantiation of the Prefs instance:
``` java
  Prefs.with(yourContext, true).readInt(YOUR_KEY_VALUE);
  Prefs.with(yourContext, "CUSTOM_NAME", true).readInt(YOUR_KEY_VALUE);
```
You can also set and retrieve `ordered String sets` and `unordered String sets`.
