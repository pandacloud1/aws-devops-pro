## Input Transformation

Define variables to Input Path
```
{
  "timestamp" : "$.time",
  "instance" : "$.detail.instance-id",
  "state" : "$.detail.state",
  "resource" : "$.resources[0]"
}
```

Template
```
{
  "timestamp": <timestamp>,
  "message": "<instance> is in state <state> at <timestamp>, with arn <resource>."
}
```
