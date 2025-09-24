## Lambda code for API Gateway integration

### Code for root path (Python 3.11)
```py
import json

def lambda_handler(event, context):
    body = "Hello from Lambda! This is my root path"
    statusCode = 200
    return {
        "statusCode": statusCode,
        "body": json.dumps(body),
        "headers": {
            "Content-Type": "application/json"
        }
    }
```

### Code for cart path (you can use anything else)
```py
import json

def lambda_handler(event, context):
    body = "This is my shopping cart!"
    statusCode = 200
    return {
        "statusCode": statusCode,
        "body": json.dumps(body),
        "headers": {
            "Content-Type": "application/json"
        }
    }
```
