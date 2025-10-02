## SCP Policies

Policy to deny DynamoDB
```json
{
  "Version":"2012-10-17",		 	 	 
  "Statement": [
    {
      "Sid": "AllowAllActions",
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    },
    {
      "Sid": "DenyDynamoDB",
      "Effect": "Deny",
      "Action": "dynamodb:*",
      "Resource": "*"
    }
  ]
}
```

Policy to allow only EC2 & CloudWatch
```json
{
  "Version":"2012-10-17",		 	 	 
  "Statement": [
    {
      "Sid": "AllowAllActions",
      "Effect": "Allow",
      "Action": [
        "ec2:*",
        "cloudwatch:*",
      ],
      "Resource": "*"
    }
  ]
}
```
