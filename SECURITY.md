# Security

Report a suspected vulnerability privately to the code owners listed in [`.github/CODEOWNERS`](.github/CODEOWNERS). Do not open a public issue or discuss it in a pull request.

Include what you found, where (file, service, URL), how to reproduce it, and the impact you expect. You will get an acknowledgement, and the fix will land through the normal pull-request flow with the details withheld until it is deployed.

Never commit secrets, tokens or customer data to this repository. Configuration comes from environment variables and Secret Manager; see the README's "Configuration" section.
