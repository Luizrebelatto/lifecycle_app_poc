# Android LifeCycle

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
