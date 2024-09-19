# AISP API Overview

## Base URL
The base URL for all AIS APIs is: `https://rs1.{prod_domain_name}/open-banking/v3.1/aisp/**`

## Account Access Consents
[Account Access Consents API](/perry/developer/documentation?resource=ukhub-clrb-portal&document=swagger/account-info-openapi.yaml#operations-tag-Account_Access)

## Accounts
[Accounts API](/perry/developer/documentation?resource=ukhub-clrb-portal&document=swagger/account-info-openapi.yaml#operations-tag-Accounts)

ClearBank  members will have one or more of the following accounts:
- Operating Account
- Customer Segregated Account or Customer Designated Account
- Client Money Account
- Multi-Currency Account
- Safeguarding Account

## Balance
The [Balances API](/perry/developer/documentation?resource=ukhub-clrb-portal&document=swagger/account-info-openapi.yaml#operations-tag-Balances) endpoint shows the account balance value. 

`InterimAvailable` balance is the value displayed most widely to our members within the ClearBank apps.

## Transactions
The [Transactions API](/perry/developer/documentation?resource=ukhub-clrb-portal&document=swagger/account-info-openapi.yaml#/operations-tag-Transactions) endpoint shows the list of transactions processed by the account. 

Note that pagination is supported on GET /accounts/{AccountId}/transactions endpoint with a page size of 100 transactions. Please also note that GET /transactions endpoint is not supported.

## Functions not supported by ClearBank
Please note the following functions are currently not supported by ClearBank via the AISP API:
- Beneficiaries: viewing the beneficiaries of an account
- Direct Debits: viewing all subscribed direct debits
- Standing Orders: viewing a list of standing orders
- Scheduled Payments: viewing a list of scheduled payments
- Statements: viewing account statements 
