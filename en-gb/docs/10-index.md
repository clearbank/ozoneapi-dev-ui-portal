# Introduction

```
Find:     contact@clear.bank -- UK
Replace:  contact@prod-email-domain.com

Find:     {prod_domain_name}
Replace:  https://www.prod-domain.com

Find:     {sandbox_domain_name}
Replace:  https://www.sandbox-domain.com

Find:     Clear.Bank
Replace:  Full Bank Name Limited

```

## ClearBank API Documentation

ClearBank’s Open Banking services powered by Ozone follows the Open Banking specifications found here:

- [Dynamic Client Registration (DCR) Specification](https://openbankinguk.github.io/dcr-docs-pub/v3.2/dynamic-client-registration.html): Use this specification to register your TPP client to use our APIs
- [Open ID Foundation's Financial Grade API (FAPI) Profile](https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md): This specification enables user authentication of consents for open banking
- Open Banking API Specification: Based on Open Banking Read/Write API Specification v3.1.2, this specification describes the resources that are available on our service:
  - [Accounts & Transaction Information API](../swagger/account-info-openapi.yaml)
  - [Payments Initiation Services API](../swagger/payment-initiation-openapi.yaml)

## Getting started

We recommend that you start off by accessing our [Sandbox](./docs/40-sandbox.md).

Our ClearBank Sandbox powered by Ozone fully reflects the production environment and provides an easy route to testing out your proposition.

To access the production environment, you must be a TPP authorised by the FCA or passported into the UK. Instructions for accessing our Production APIs are [here](./docs/30-production.md).

See our [Getting Started](./docs/20-getting-started.md) page for instructions on accessing our sandbox and production APIs

If you require test accounts please contact customercare@clear.bank

