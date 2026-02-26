# Android LifeCycle

- onCreate → onStart → onResume

### OnCreate()

- called when the Activity is first created

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)

    Log.d("LIFECYCLE", "onCreate")
}
```

- init UI and setup
- Config listeners
- init variables

## OnStart()

- when the activity becomes visible to the user
- UI already exist but the user is still not interacting.

```kotlin
override fun onStart() {
    super.onStart()
    Log.d("LIFECYCLE", "onStart")
}
```

## OnResume()

- App in foreground
- init animations
- init sensor(GPS, camera)

```kotlin
override fun onResume() {
    super.onResume()
    Log.d("LIFECYCLE", "onResume")
}
```

## onPause()

```kotlin
override fun onPause() {
    super.onPause()
    Log.d("LIFECYCLE", "onPause")
}
```

## onStop()

- activity arent visible
- remove observers

```kotlin
override fun onStop() {
    super.onStop()
    Log.d("LIFECYCLE", "onStop")
}
```

## onDestroy()

- Activity is being destroyed
- equivalent to Unmount (React)
- free up memory
- cancel processes

```kotlin
override fun onDestroy() {
    super.onDestroy()
    Log.d("LIFECYCLE", "onDestroy")
}
```
