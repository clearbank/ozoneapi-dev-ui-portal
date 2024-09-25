# Getting started

## Dynamic Client Registration

ClearBank’s API powered by Ozone does not allow dynamic client registration in the EU. ClearBank will manually onboard TPPs and verify their Software Statement Assertions (SSAs).

## Production security profile

As defined further in the ClearBank Open Banking API Specification

- ID Token Signing Algorithm: `PS256`
- Response Types: `code id_token`
- Request Object Signing Algorithms: `PS256`
- Token Endpoint Auth Singing Algorithms: `PS256`
- Token Endpoint Auth Methods: `private_key_jwt`, `tls_client_auth`

> For private_key_jwt - the `aud` claim is the url of the token endpoint as specified in OIDC client authentication
> The request object used in OIDC flows the aud claim is the issuer url from the ClearBank ASPSP .wellknown endpoint (linked below).

> Note: The Sandbox API also offers less strict profiles to assist with integration testing. See below for more details.

## Certificate Support

