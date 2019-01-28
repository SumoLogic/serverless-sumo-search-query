Work in progress:
- Doesn't actually create proper CSV output
- Should send SNS notification at the end

In the meantime:

```
npm install -g serverless
git clone git@github.com:SumoLogic/serverless-query.git
cd serverless-query
npm install # Ignore warnings
serverless deploy
serverless invoke stepf -n sumosearch --data \
'{"endpoint": "us2", "accessId": "[access-id]", "accessKey": "[access-key]", \
"query": "error | count", "from": "2019-01-19T16:00:00", "to": "2019-01-19T16:01:00", \
"timeZone": "Asia/Kolkata", "s3Bucket": "[your-bucket]]", "s3KeyPrefix": "[your-prefix]]"}'
```

Note: Need to have AWS credentials in `~/.aws/credentials`.