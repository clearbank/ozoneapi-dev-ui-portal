# PISP API Overview

The following section outlines the requirements for passing a payment through ClearBank’s PIS services.  

## Base URL
The base URL for all PIS APIs is: `https://rs1.openbanking.clearbankgb.com/open-banking/v3.1/pisp/**`

## Supported Payment Types
ClearBank's Open Banking API powered by Ozone currently supports only the following endpoints:
- Domestic Payments
- Payment Details

ClearBank's Open Banking API powered by Ozone **does not** support the following endpoints:
- International Payments
- File & Bulk Payments
- Domestic Scheduled Payments
- Domestic Standing Orders

## Overview
The following fields are mandatory for all domestic payment consents:

### `InstructedAmount/Amount`
The ClearBank Open Banking API mandates a maximum amount in `InstructedAmount/Amount`. As ClearBank will be processing your payments through Faster Payments (FPS), ClearBank mandates a maximum amount per payment of £1,000,000. ClearBank recommends that PISP notify the PSU of the limits applied on payments. 

It is possible that a `domestic-payment-consents` is authorised, but the payment initiation fails due to account limits.

### `InstructedAmount/Currency`
`InstructedAmount/Currency` must be `GBP` for UK domestic transactions. 

### `RemittanceInformation/Reference`
`RemittanceInformation/Reference` is a mandatory field and must adhere to the following:
- Valid characters:
  - A-Z
  - a-z
  - 0-9
  - "space"
  - The characters "&", "-", ".", "/"
  
- Contiguous characters – user enters 6 or more valid characters but without contiguous string of at least 6 alphanumeric characters
- Must contain a contiguous string of at least 6 alphanumeric characters
- Homogeneous string – user enters 6 or more valid characters (including valid non-alphanumeric characters) - After stripping out non-alphanumeric characters the resulting string cannot consist of all the same character

The PISP may also opt to populate reference field on behalf of the PSU.

### `CreditorAccount`
Domestic-payment-consents will only be authorised if the `CreditorAccount` details are sent or received. If a consent contains recipient information that does not meet this criteria then an error will be returned to the front end, the consent will remain in status `AwaitingAuthorisation` and the PSU will not be redirected.

### `Account.SchemeName`
The only supported `Account.SchemeName` is `UK.OBIE.SortCodeAccountNumber` for both `DebtorAccount` and `CreditorAccount`. Any other enum provided will return an error.

### `Structured Debtor Address`
- Description: The full postal address of the account holder. For UK addresses, the order of this information must be: country, town, city, state/province/municipality, street name, building number and/or name, postal code. 
- Minimum length: 1
- Maximum length: 140
- Pattern: ^[a-z;A-Z,0-9,|/.|-?:().,'+_]*$

## Payment dates
Payments can be made on all days including Saturdays, Sundays and Bank Holidays.

