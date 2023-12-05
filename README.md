# README #

This repository contains the content for the ClearBank openbanking developer portal. This portal
will primarily used by third party developers (TPP developers) to consume the openbanking APIs
exposed by ozone  (for ClearBank).

This repository can be used to tailor the content presented to the third party developers including
branding.
### How this repository is used ###

This repository is pulled by ozone and used to refresh the content being displayed on the developer portal.
The developer portal is maintained by ozone, this repository provides the content to be displayed on the portal.

If the API spec is changed, it is expected to update the swagger definitions checked into this repository.

```
Content placeholders
The following placeholders can be used for find/replace opperations:

Find:     {prod_contact_us_email}
Replace:  contact@prod-email-domain.com

Find:     {prod_domain_name}
Replace:  prod-domain.com

Find:     {sandbox_domain_name}
Replace:  sandbox-domain.com

Find:     {bank_name}
Replace:  Full Bank Name Limited

Find:     resource=dev-ui-portal
Replace   branch-name

```
