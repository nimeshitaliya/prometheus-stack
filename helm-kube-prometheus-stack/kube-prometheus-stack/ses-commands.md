# Configure email notification on alertmanager using AWS SES

## Prerequisite
- [Verifying an email address identity](https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#just-verify-email-proc)
- [Create your SMTP credentials](https://docs.aws.amazon.com/ses/latest/dg/smtp-credentials.html)

## Required configuration in ivari-sandbox-values.yaml
```yaml
alertmanager:
  config:
    receivers:
    - name: 'email-notifications'
      email_configs:
      - to: "${TO_EMAIL_ADDRESS}"      # you@example.com
        from: "${FROM_EMAIL_ADDRESS}"  # alertmanager@example.com
        smarthost: "email-smtp.${SES_SMTP_REGION}.amazonaws.com:587"
        auth_username: "${SES_SMTP_USERNAME}"
        auth_password: "${SES_SMTP_PASSWORD}"
        send_resolved: true
```
