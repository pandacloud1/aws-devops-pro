## CUSTOM METRIC TO CREATE NAMESPACE

Run below command in CloudShell
```sh
aws cloudwatch put-metric-data --metric-name buffers --namespace MyNamespace --unit Bytes -- value 231434333 --dimensions InstanceID=<instance-id>, InstanceType=t2.micro
```
