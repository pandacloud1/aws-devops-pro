## Session Manager

* ### Can we restrict Session Manager to specific EC2?
Yes, we can by creating custom policy & adding the condition

```json
{
  "Version": "2012-10-17",
  "Statement": [
     {
       "Effect": "Allow",
       "Action": "ssm:StartSession",
       "Resource": "<EC2-instance-ARN>/*",
       "Condition": {
          "StringLike": {
             "ssm:resourceTag/Environment": ["Dev"]
          }
       }
     }
  ] 
}
```
