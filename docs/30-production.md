# Production

Below are the paths of our well-known endpoints for the production environment.

Our production authorisation server uses the strict profile defined above and testable in the Sandbox.

## Authorisation Server URLs
- OIDC Well Known endpoint: https://auth1.api.gb-ob.zing.me/.well-known/openid-configuration
- baseUrl: https://auth1.api.gb-ob.zing.me/
- Authorisation URL: https://api.gb-ob.zing.me/u/openbanking

## Resource Server URLs
- Account Information Services API: https://rs1.api.gb-ob.zing.me/open-banking/v3.1/aisp/**

- Payment initiation services API: https://rs1.api.gb-ob.zing.me/open-banking/v3.1/pisp/**

- Confirmation of Funds API: https://rs1.api.gb-ob.zing.me/open-banking/v3.1/cbpii/**

## Test accounts
If you require test accounts please contact mailto:{prod_contact_us_email}