## KQL queries contributed by Microsoft employees within this chapter
#### Use the copy option (to the right of each code box) to copy the query to paste into your own environment

Why you should run it: 

Monitor EntraId dynamic group processing for membership changes. 

Contributed by: Some dude

```KQL

AuditLogs 
| where Category == "GroupManagement" 
| where TargetResources == "REPLACE" // group id you want to monitor 
| where ActivityDisplayName in ("Add member to group","Remove member from group") or ActivityDisplayName =="Update group" 
| summarize count() by TimeGenerated 
| render timechart
```

