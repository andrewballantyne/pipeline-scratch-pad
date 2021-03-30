# Install Steps

Have 4.5+ cluster (or at least OpenShift Pipelines Operator 0.11+)

Prereq: Apply Trigger Resources from nested folders here / add it through OpenShift Console UI

## Secure Hook

1. Setup a GitHub token
1. Manually create this with a token

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: webhook-secret
stringData:
  token: YOUR-GITHUB-ACCESS-TOKEN
  secret: random-string-data
```

## Github Setup

Couple things you need to do on GitHub to get it to trigger.

1. Generate a Token on your account to use in the secret / webhook
    * Github => Settings => Developer Settings => Generate Token
1. Add the webhook
    * Github/Repo => Settings => Webhook
