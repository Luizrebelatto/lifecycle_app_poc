# Lifecycle Events

"Life" moments of a component, from the moment of creation to destruction

3 States

![Lifecycle Diagram](assets/images/lifecycleDiagram.png)

- Mounting
- Updating
- UnMounting

## Mounting

When created, an instance of a component is added to the DOM tree
its called some functions when `Mount` is called

```javascript
(useState(),
  useEffect(() => {
    console.log("MOUNT");
  }, []));
```

When passing an empty dependency in useEffect, it only executes at the initial moment. A use case would be to call the event once, such as feature flags or listening to events.
