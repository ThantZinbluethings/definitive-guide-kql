## KQL queries contributed by Microsoft employees within this chapter
#### Use the copy option (to the right of each code box) to copy the query to paste into your own environment


```KQL
SecurityEvent
```

The following statement demonstrates the **search** operator:

```KQL
search "new"
```

The following statement demonstrates searching across tables: 

```KQL
search in (SecurityEvent,App*) "new"
```
