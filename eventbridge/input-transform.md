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

Leverage the variables in a template
```
{
  "instance" : <instance>,
  "state" : <state>,
"ruleArn" : <aws.events.rule-arn>,
"ruleName" : <aws.events.rule-name>,
"originalEvent" : <aws.events.event.json>
}
```
