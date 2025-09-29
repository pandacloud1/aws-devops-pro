## Commonly used CloudWatch Log Insights Queries

25 most recently added log events
```
fields @timestamp, @message
| sort @timestamp desc
| limit 25
```
 
Number of exceptions logged every 5 minutes
``` 
filter @message like /Exception/
| stats count(*) as exceptionCount by bin(5m)
| sort exceptionCount desc
```
 
 
List of log events that are not exceptions
```
fields @message
| filter @message not like /Exception/
```
