## Cache Invalidation
- Cache invalidation means to clear the cache in API Gateway
- This can be done immediately
- We can also make use of header max=0 to clear the cache
- Use below policy to clear the cache

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
    "Effect": "Allow",
    "Action": [
       "execute-api:InvalidateCache"
    ],
    "Resource": [
       "<API-ARN>"
     ],
    }
  ]
}
```
