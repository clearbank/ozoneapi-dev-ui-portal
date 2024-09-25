# AISP API Overview

## Base URL
The base URL for all AIS APIs is: `https://rs1.{prod_domain_name}/open-banking/v3.1/aisp/**`

## Account Access Consents
[Account Access Consents API](https://developer.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/en-eu/swagger/account-info-openapi.yaml#account-access)

## Accounts
[Accounts API](https://developer.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/en-eu/swagger/account-info-openapi.yaml#accounts)

ClearBank  members will have one or more of the following accounts:
- Operating Account
- Customer Segregated Account or Customer Designated Account

## Balance
The [Balances API](https://developer.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/en-eu/swagger/account-info-openapi.yaml#balances) endpoint shows the account balance value. 

`InterimAvailable` balance is the value displayed most widely to our members within the ClearBank apps.

## Transactions
The [Transactions API](https://developer.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/en-eu/swagger/account-info-openapi.yaml#transactions) endpoint shows the list of transactions processed by the account. 

Note that pagination is supported on GET /accounts/{AccountId}/transactions endpoint with a page size of 100 transactions. Please also note that GET /transactions endpoint is not supported.

## Functions not supported by ClearBank
Please note the following functions are currently not supported by ClearBank via the AISP API:
- Beneficiaries: viewing the beneficiaries of an account
- Direct Debits: viewing all subscribed direct debits
- Standing Orders: viewing a list of standing orders
- Scheduled Payments: viewing a list of scheduled payments
- Statements: viewing account statements 
