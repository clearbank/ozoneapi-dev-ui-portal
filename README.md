# README #

This repository contains the content for the Clear.Bank OpenBanking Developer Portal. This portal
will primarily used by Third Party Developers (TPP developers) to consume the OpenBanking APIs
exposed by Ozone (for Clear.Bank).

This repository can be used to tailor the content presented to the third party developers including
branding.

### How this repository is used ###

This repository is pulled by Ozone and used to refresh the content being displayed on the developer portal.
The developer portal is maintained by Ozone, this repository provides the content to be displayed on the portal.

If the API specification is changed, it is expected to update the swagger definitions checked into this repository.

```
Content placeholders
The following placeholders can be used for find/replace opperations:

Find:     contact@clear.bank
Replace:  contact@prod-email-domain.com

Find:     {prod_domain_name}
Replace:  prod-domain.com

Find:     {sandbox_domain_name}
Replace:  sandbox-domain.com

Find:     Clear.Bank
Replace:  Full Bank Name Limited

Find:     resource=ukhub-clrb-portal
Replace   branch-name

```
