# Production

Below are the paths of our well-known endpoints for the production environment.

Our production authorisation server uses the strict profile defined below and testable in the Sandbox.

## Authorisation Server URLs
- OIDC Well Known endpoint: https://auth1.{prod_domain_name}/.well-known/openid-configuration
- baseUrl: https://auth1.{prod_domain_name}/
- Authorisation URL: https://{prod_domain_name}/u/openbanking

## Resource Server URLs
- Account Information Services API: https://rs1.{prod_domain_name}/open-banking/v3.1/aisp/**

- Payment initiation services API: https://rs1.{prod_domain_name}/open-banking/v3.1/pisp/**

- Confirmation of Funds API: https://rs1.{prod_domain_name}/open-banking/v3.1/cbpii/**

## Test accounts
If you require test accounts please contact customercare@clear.bank.
