# Sandbox

Our API Sandbox contains a full simulation of our APIs but without connecting to any real customer accounts. Any developer can access this Sandbox using their own self signed certificates.

## Try our API in the Sandbox

We provide a regulatory sandbox that fully reflects our production APIs.

### Regulatory Sandbox

- Authorisation Server 1: Provides both strict and permissive client profiles in headless and non headless options.
- OIDC Well Known endpoint: https://auth1.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/.well-known/openid-configuration
- baseUrl: https://auth1.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/

### Step by Step guide to connect to sandbox

#### Step 1: Pre-Requisites for TPP
Ensure that the following pre-requisites are met before onboarding with ClearBank.
- The TPP has registered on the Directory Sandbox - https://directory.openbanking.org.uk/s/login/
- The TPP has at least one software statement created on the Directory Sandbox environment
- The TPP has at least one transport certificate created for each of its software statements.
- The TPP has at least one redirect URI for each of its software statements.
- The TPP has a copy of the OB root and issuing certificate attached.

#### Step 2: TPP should contact our Open Banking support team
We do not offer Dynamic Client Registration in the EU. Please contact our Open Banking support team to be onboarded, customercare@clear.bank.

#### Step 3: Import Environment Files and Collections To Postman
3.1. Import Environment Files and Collections into Postman
![postmanimage](/assets/images/postmanimport1.png)

![](/assets/images/postmanimport2.png)

3.2) Check URLs and Environments are loaded successfully

3.3) Add Client Certificates
Add the following ASPSP end points into Postman;
https://rs1.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk
https://auth1.sandbox.clrb.uk-hub-prod.ozoneapi.co.uk/token

The CRT should be set to the transport certificate downloaded from the open banking directory. The Key value should be set to the private key for the transport certificate.


3.4) SSL Certificate Verification (TPP)
In Postman settings ensure SSL Certificate Verification is set to off.

#### Step 4: Account Information Flow

4.1) Client Credentials Grant

![](/assets/images/ccg.png)

4.2) Account Access Consent

![](/assets/images/accountaccess.png)

4.3) PSU Consent Flow
TPPs can generate the consent flow URL by postman

![](/assets/images/consent1.png)

Once the URL is constructed, open the URL to initiate the PSU consent flow

Authenticate user

![](/assets/images/consent2.png)

Sandbox User Accounts

| user | password |
|------|----------|
| rora |	rora.   |
| mits |	mits.   |
| ivsa |	ivsa.   |

Select accounts

![](/assets/images/consent3.png)

Once the PSU consent is successful, ClearBank will redirect back to the redirect URI. Copy the Authcode from the URL

![](/assets/images/consent4.png)

4.4) Generate the access token

![](/assets/images/accesstoken.png)

#### Step 5: Retrieve Account and Transaction Data
Retrieve Account Data

![](/assets/images/accounts.jpeg)

![](/assets/images/transactions.jpeg)
