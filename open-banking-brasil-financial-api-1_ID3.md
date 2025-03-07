%%%

    #
    # Open Finance Brasil Financial-grade API Security Profile 1.0 Implementers Draft 3
    # (open-banking-brasil-financial-api-1_ID3)
    #
    #

    title = "Open Finance Brasil Financial-grade API Security Profile 1.0 Implementers Draft 3"
    abbrev = "OFB-FAPI-1-ID3"
    ipr = "none"
    workgroup = "Open Finance Brasil GT Security"
    keyword = ["FAPI", "Open Finance Brasil GT Security"]

    [seriesInfo]
    name = "Internet-Draft"
    status = "standard"
    value = "open-banking-brasil-financial-api-1_ID3"

    [[author]]
    initials = "GT"
    surname = "Security"
    fullname = "OFBIS GT Security"
    organization = "Open Finance Brasil Initial Structure"
    abbrev = "OFBIS"
      [author.address]
      email = "gt-seguranca@openbankingbr.org"
      uri = "https://openbankingbrasil.org.br/"
%%%

.# Foreword

Este documento também está disponível em [português](https://openbanking-brasil.github.io/specs-seguranca/open-banking-brasil-financial-api-1_ID3-ptbr.html)

The Open Finance Brasil Initial Structure is responsible for creating standards and specifications necessary to meet the requirements and obligations of the Brasil Open Finance Legislation as originally outlined by the [Brasil Central Bank](https://www.bcb.gov.br/content/config/Documents/BCB_Open_Banking_Communique-April-2019.pdf). There is a possibility that some of the elements of this document may be the subject to patent rights. OFBIS shall not be held responsible for identifying any or all such patent rights.

Open Finance Brasil Financial-grade API Security Profile 1.0 consists of the following parts:

* Open Finance Brasil Financial-grade API Security Profile 1.0
* [Open Banking Brasil Dynamic Client Registration Profile 1.0][OFB-FAPI-DCR]

These parts are intended to be used with [RFC6749], [RFC6750], [RFC7636], [OIDC], [FAPI-1-Baseline] and [FAPI-1-Advanced]

.# Introduction

The Open Finance Brasil Financial-grade API is a highly secured OAuth profile that aims to provide specific implementation guidelines for security and interoperability which can be applied to APIs in the Brasil Open Finance area that require a higher level of privacy than provided by standard [Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced]. Among other enhancements, this specification addresses privacy considerations identified in [FAPI-1-Advanced] that are relevent in the Open Finance Brasil specifications but have not, so far, been required by other jurisdictions.

Although it is possible to code an OpenID Provider and Relying Party from first principles using this specification, the main audience for this specification is parties who already have a certified implementation of [Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced] and want to achieve certification for the Brasil Open Finance programme.

.# Notational Conventions

The key words "shall", "shall not",
"should", "should not", "may", and
"can" in this document are to be interpreted as described in
[ISO Directive Part 2][ISODIR2].

These key words are not to be used as lexicon terms such that any occurrence of them shall be interpreted as key words and are not to be interpreted with their natural language meanings.

{mainmatter}

# Scope

This document specifies the method of

* applications to obtain the OAuth tokens in an appropriately secure manner for higher risk access to data in a manner that meets the requirements of [Open Finance Brasil](https://www.in.gov.br/en/web/dou/-/resolucao-conjunta-n-1-de-4-de-maio-de-2020-255165055);
* applications to use OpenID Connect to identify the customer; and
* applications to use OpenID Connect to assert identity of the customer;

This document is applicable to all participants engaging in Open Finance in Brasil.

# Normative references

The following referenced documents are indispensable for the application of this document. For dated references, only the edition cited applied. For undated references, the latest edition of the referenced document (including any amendments) applies.

[ISODIR2] - ISO/IEC Directives Part 2
[ISODIR2]: <https://www.iso.org/sites/directives/current/part2/index.xhtml

[RFC6749] - The OAuth 2.0 Authorization Framework
[RFC6749]: <https://tools.ietf.org/html/rfc6749

[RFC6750] - The OAuth 2.0 Authorization Framework: Bearer Token Usage
[RFC6750]: <https://tools.ietf.org/html/rfc6750

[RFC7636] - Proof Key for Code Exchange by OAuth Public Clients
[RFC7636]: <https://tools.ietf.org/html/rfc7636

[RFC6819] - OAuth 2.0 Threat Model and Security Considerations
[RFC6819]: <https://tools.ietf.org/html/rfc6819

[RFC7515] - JSON Web Signature (JWS)
[RFC7515]:<https://tools.ietf.org/html/rfc7515

[RFC7519] - JSON Web Token (JWT)
[RFC7519]:<https://tools.ietf.org/html/rfc7519

[RFC7591] - OAuth 2.0 Dynamic Client Registration Protocol
[RFC7591]:<https://tools.ietf.org/html/rfc7591

[RFC7592] - OAuth 2.0 Dynamic Client Registration Management Protocol
[RFC7592]:<https://tools.ietf.org/html/rfc7592

[BCP195] - Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)
[BCP195]: <https://tools.ietf.org/html/bcp195

[OIDC] - OpenID Connect Core 1.0 incorporating errata set 1
[OIDC]: <https://openid.net/specs/openid-connect-core-1_0.html

[FAPI-CIBA] - Financial-grade API: Client Initiated Backchannel Authentication Profile
[FAPI-CIBA]: <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_CIBA.md

[OIDD] -  OpenID Connect Discovery 1.0 incorporating errata set 1
[OIDD]: <https://openid.net/specs/openid-connect-discovery-1_0.html

[OIDR] -  OpenID Connect Registration 1.0 incorporating errata set 1
[OIDR]: <https://openid.net/specs/openid-connect-registration-1_0.html

[RFC8705] - OAuth 2.0 Mutual TLS Client Authentication and Certificate Bound Access Tokens
[RFC8705]: <https://tools.ietf.org/html/rfc8705

[JARM] - Financial-grade API: JWT Secured Authorization Response Mode for OAuth 2.0 (JARM)
[JARM]: <https://bitbucket.org/openid/fapi/src/master/Financial_API_JWT_Secured_Authorization_Response_Mode.md

[PAR] - OAuth 2.0 Pushed Authorization Requests
[PAR]: <https://tools.ietf.org/html/draft-ietf-oauth-par

[JAR] - OAuth 2.0 JWT Secured Authorization Request
[JAR]: <https://tools.ietf.org/html/draft-ietf-oauth-jwsreq

[FAPI-1-Baseline] - Financial-grade API Security Profile 1.0 - Part 1: Baseline
[FAPI-1-Baseline]: <https://openid.net/specs/openid-financial-api-part-1-1_0.html

[FAPI-1-Advanced] - Financial-grade API Security Profile 1.0 - Part 2: Advanced
[FAPI-1-Advanced]: <https://openid.net/specs/openid-financial-api-part-2-1_0.html

[FAPI-2-Baseline] - Financial-grade API Security Profile 2.0 - Part 1: Baseline
[FAPI-2-Baseline]: <https://bitbucket.org/openid/fapi/src/master/FAPI_2_0_Baseline_Profile.md

[FAPI-2-Advanced] - Financial-grade API Security Profile 2.0 - Part 2: Advanced
[FAPI-2-Advanced]: <https://bitbucket.org/openid/fapi/src/master/FAPI_2_0_Advanced_Profile.md

[LIWP] - OIDF FAPI WG Lodging Intent Working Paper
[LIWP]: <https://bitbucket.org/openid/fapi/src/master/Financial_API_Lodging_Intent.md

[OFB-FAPI-DCR] - Open Banking Brasil Financial-grade API Dynamic Client Registration Profile 1.0
[OFB-FAPI-DCR]: <https://openbanking-brasil.github.io/specs-seguranca/open-banking-brasil-dynamic-client-registration-1_ID2.html

[RFC4648] - The Base16, Base32, and Base64 Data Encodings
[RFC4648]: <https://tools.ietf.org/html/rfc4648

# Terms and definitions

For the purpose of this document, the terms defined in [RFC6749], [RFC6750], [RFC7636], [OpenID Connect Core][OIDC] and ISO29100 apply.

# Symbols and Abbreviated terms

* **API** – Application Programming Interface
* **CSRF** - Cross Site Request Forgery
* **DCR** – Dynamic Client Registration
* **FAPI** - Financial-grade API
* **HTTP** – Hyper Text Transfer Protocol
* **MFA** - Multi-Factor Autentication
* **OFBIS** – Open Finance Brasil Initial Structure
* **OIDF** - OpenID Foundation
* **REST** – Representational State Transfer
* **TLS** – Transport Layer Security

# Brasil Open Finance Security Profile

## Introduction

The Brasil Open Finance Security profile specifies additional security and identity requirements for high risk API resources protected by the OAuth 2.0 Authorization Framework that consists of [RFC6749], [RFC6750], [RFC7636], [FAPI-1-Baseline], [FAPI-1-Advanced] and other specifications.

This profile describes security and features provisions for a server and client that are necessary for the Brasil Open Finance Programme by defining the measures to mitigate or address:

* attacks that address privacy considerations identified in clause 9.1 of [FAPI1 Advanced]
* the requirement to support fine-grained access to resources for data minimisation purposes
* the requirement to convey the Authentication Context Request that was performed by an OpenID Provider to a Client to enable a appropriate client management of customer conduct risk.
* the requirement for clients to assert a pre-existing customer relationship by asserting a customer identity claim as part of the authorization flow.

## Open Finance Brasil security provisions

### Introduction

Open Finance Brasil has a requirement to address privacy considerations that were identified but not addressed in the [FAPI-1-Advanced] final specification without imposing additional requirements on Authorisation Servers being proposed in [FAPI-2-Baseline].

Participants in this ecosystem have a need for clients to request an openid provider to confirm values of identity claims as part of an authorization request using the mechanism defined in clause 5.5.1 of [OIDC].

The use of the claims parameter to request explicit claims values requires clients to ensure that they encrypt the request object to avoid information leakage. This risk is identified in clause 7.4.1 of [FAPI-1-Baseline].

In addition this profile describes the specific scope, acr and client management requirements necessary to support the wider Open Finance Brasil ecosystem.

As a profile of the OAuth 2.0 Authorization Framework, this document mandates the following for the Brasil Open Finance Security profile.

### Authorization server

The Authorization Server shall support the provisions specified in clause 5.2.2 of [Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced]

In addition, the Authorization Server

1. shall support a signed and encrypted JWE request object passed by value or shall require pushed authorization requests [PAR];
2. shall distribute discovery metadata (such as the authorization endpoint) via the metadata document as specified in [OIDD] and [RFC8414] (".well-known");
3. shall support the claims parameter as defined in clause 5.5 [OpenID Connect Core][OIDC];
4. shall support the oidc standard claim "cpf" as defined in clause 5.2.2.2 of this document;
5. shall support the oidc standard claim "cnpj" as defined in clause 5.2.2.3 of this document if the institution provides accounts for legal person;
6. shall support the acr "urn:brasil:openbanking:loa2" as defined in clause 5.2.2.4 of this document;
7. should support the acr "urn:brasil:openbanking:loa3" as defined in clause 5.2.2.4 of this document;
8. shall implement the userinfo endpoint as defined in clause 5.3 [OpenID Connect Core][OIDC];
9. shall support parameterized OAuth 2.0 resource scope _consent_ as defined in clause 6.3.1 [OIDF FAPI WG Lodging Intent Pattern][LIWP];
10. may support [Financial-grade API: Client Initiated Backchannel Authentication Profile][FAPI-CIBA];
11. (withdrawn temporarily);
12. shall support refresh tokens;
13. shall issue access tokens with an expiry no greater than 900 seconds and no less than 300 seconds;
14. shall always include an acr claim in the `id_token`;
15. shall support the `response_type` value `code id_token`;
16. may support `response_type` value `code` in conjunction with the `response_mode` value `jwt`;
17. should offer the possibility to disable the rotation of `refresh token`;
18. shall ensure that, in case of sharing the Authorization Server for other services, in addition to Open Finance, it does not disclose and/or allow the use of non-certified methods in the Open Finance environment;
19. shall ensure that the settings disclosed to other participants through `OpenID Discovery` (indicated by the `Well-Known` file registered in the Directory) are restricted to the operating modes to which the institution has certified;
    1. shall keep in your settings the methods for which there are still active clients;
    2. shall update the records that use non-certified methods, through bilateral treatment between the institutions involved.
20. shall refuse requests, for the Open Finance environment, that are outside the modes of operation to which the institution has certified its Authorization Server;
21. must refuse authentication requests that include an id_token_hint, as the id_token held by the requester may contain Personally Identifiable Information, which could be sent unencrypted by the public client.

#### ID Token as detached signature

The Authorization Server shall support the provisions specified in clause 5.2.2.1 of [Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced]

In addition, if the `response_type` value `code id_token` is used, the Authorization Server:

1. should not return sensitive PII in the ID Token in the authorization response, but if it needs to,
then it shall encrypt the ID Token;
2. Personally Identifiable Information may include, but is not limited to,:
    1. Claim `sub` if you use information that makes it possible to identify the natural person;
    2. The default Claims defined in clause 5.1 [OIDC], which may contain data such as date of birth, address or telephone;
    3. The new Claim CPF, defined in the next section.
3. If a Claim containing Personally Identifiable Information is requested:
    1. If this is marked as essential, if there is no encryption key registered for the Customer, the request must fail if requested at the Authorization Endpoint. There are no impediments if the request is made by the Confidential Client through the Token Endpoint;
    2. If this is not marked as essential, the Authorization Server must omit it on the Authorization Endpoint, and it can be answered on the Token Endpoint called by the Confidential Client.
4. For the encryption of the id_token, a key available in the `JWKS` informed in the `jwks_uri` parameter during the client registration must be used, indicated through the `kid` header of the JWT document;
5. The use of other headers to indicate the key used, such as `x5u`, `x5c`, `jku` or `jkw` is prohibited as defined in clause 2 [OIDC].


#### Requesting the "cpf" Claim

This profile defines "cpf" as a new standard claim as per
 clause 5.1 [OIDC]

The **CPF** number (Cadastro de Pessoas Físicas, [sepeˈɛfi]; Portuguese for "Natural Persons Register") is the **Brazilian** individual taxpayer registry identification. This number is attributed by the **Brazilian** Federal Revenue to Brazilians and resident aliens who, directly or indirectly, pay taxes in **Brazil**.

In the Brasil Open Finance identity model, the cpf is a string consisting of numbers that is 11 characters long and may start with a 0.

If the cpf Claim is requested as an Essential Claim for the ID Token or UserInfo response with a values parameter requesting a specific cpf value, the Authorization Server MUST return a cpf Claim Value that matches the requested value.

If the cpf Claim is requested as an Essential Claim for the ID Token or UserInfo response,
 the Authorization Server shall return a cpf Claim Value with the authenticated user cpf value.

If this is an Essential Claim and the requirement cannot be met or is not compatible with the one requested, then the Authorization Server shall treat that outcome as a failed authentication attempt.

Name: cpf, Type: String, Regex: '^\d{11}$'

#### Requesting the "cnpj" Claim

This profile defines "cnpj" as a new standard claim as per
 clause 5.1[OIDC]

**CNPJ**, short for Cadastro Nacional de Pessoas Jurídicas, is an identification number
 of **Brazilian** companies issued by the **Brazilian** Ministry of Revenue, **in**
 Portuguese "Secretaria da Receita Federal" or "Ministério da Fazenda". In the Brasil Open Finance identity model, individuals can associated with 0 or more CNPJs. A CNPJ is a string consisting of numbers that is 14 digits long and may start with a 0, the first eight digits identify the company, the four digits after the slash identify the branch or
 subsidiary ("0001" defaults to the headquarters), and the last two are checksum digits.
 For this profile, the cnpj claim must be requested and supplied as the 14 digit number.

If the **cnpj** Claim is requested as an Essential Claim for the ID Token or UserInfo response with a values parameter requesting a specific **cnpj** value, the Authorization Server **SHALL** return a **cnpj** Claim Value that contains a **set** of CNPJs one of which must match the requested value.

If the **cnpj** Claim is requested as an Essential Claim for the ID Token or UserInfo
 the Authorization Server MUST return a cnpj Claim Value that contains a **set** of CNPJs one of which must match a CNPJ belonging to the authenticated user's account.

If this is an Essential Claim and the requirement cannot be met, then the Authorization Server shall treat that outcome as a failed authentication attempt.

Name: cnpj, Type: Array of Strings, Array Element Regex: '^\d{14}$'

#### Requesting the "urn:brasil:openbanking:loa2" or "urn:brasil:openbanking:loa3" Authentication Context Request

This profile defines "urn:brasil:openbanking:loa2" and "urn:brasil:openbanking:loa3" as
 new Authentication Context Request (ACR) classes.

* **LoA2:** Authentication performed using single factor;
* **LoA3:** Authentication performed using multi factor (MFA)

The following rules are applicable to the authentication mechanism of Open Finance Brazil API´s:

* In accordance to Art. 17 of [Joint Resolution nº 01 - Open Banking Brasil](https://www.in.gov.br/en/web/dou/-/resolucao-conjunta-n-1-de-4-de-maio-de-2020-255165055), institutions must adopt procedures and controls for client authentication **compatible with those applicable in their electronic service channels**.
* In accorcdance with the regulation, it is suggested that:
   * **For Read-Only APIs  (Phase 2)**: the _Authorization Servers_ **should** adopt, at least, an authentication method compatible with `LoA2`; and
   * **For Read-Write API´s (subsequent phases)**: the _Authorization Servers_ **should** adopt an authentication method compatible with `LoA3` or higher.

In all cases, the adoption of a more rigorous authentication mechanism (`LoA3` or higher) is at the discretion of the Bank (ASPSP), according to its risk assessment and in a manner compatible with the mechanisms usually employed.

**Authentication factors clarification**

The authentication methods are:

* Something **you know**, such as password or phrase
* Something **you have**, such as token, smartcard or device
* Something **you are**, meaning an authentication that makes use of physical characteristics, such as biometric validation.

To performe a MFA authentication is necessary that the end user presents at least two different methods as listed above. A unique method used more than once - ie. presenting passwords - is not accepted as MFA.

### Confidential client

A confidential client shall support the provisions specified in clause 5.2.3 of
[Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced],

In addition, the confidential client

1. shall support _encrypted_ request objects;
2. shall support Pushed Authorisation Requests [PAR];
3. shall use _encrypted_ request objects if not using [PAR];
4. shall support parameterized OAuth 2.0 resource scope _consent_ as defined in clause 6.3.1 [OIDF FAPI WG Lodging Intent Pattern][LIWP];
5. shall support refresh tokens;
6. shall not populate the `acr` claim with required values;
7. shall require the `acr` claim as an essential claim;
8. shall support all authentication methods specified in clause 5.2.2-14 of [Financial-grade API Security Profile 1.0 - Part 2: Advanced][FAPI-1-Advanced] including diferent combinations of the methods to send requests (using [PAR] or not - item 11);
9. shall not allow `refresh tokens` rotation feature;
10. should not request authentication requests that include an id_token_hint, as the id_token to be used may contain Personally Identifiable Information, which could be sent unencrypted through the public client.

# Security considerations

Participants shall support all security considerations specified in clause 8
 [Financial-grade API Security Profile 1.0 - Part 1: Advanced][FAPI-1-Advanced] and the [Brazilian Central Bank Open Banking Security Manual](https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?tipo=Instru%C3%A7%C3%A3o%20Normativa%20BCB&numero=134).
 The Brazilian ICP issues RSA x509 certificates only therefor section removes for simplicity support for EC algorithms
 and requires that only IANA recommended encryption algorithms be used.

## Message Content Signing Considerations (JWS) {#jws}

1. JWS standad defined in [RFC7515] shall be adopted to ensure integrity and non-repudiation of information processed in sensitive **API's (message sign requirement is indicated at API´s documentation/swagger)**, which includes:
  * Header (_JSON Object Signing and Encryption – JOSE Header_), which defines the algorithm used and includes information about the public key or certificate that can be used to validate the signature;
  * Payload (_JWS Payload_): content itself as detailed in the API specification;
  * Digital signature (_JWS Signature_): digital signature, performed according to header parameters.
2. Each of elements above must be encoded using the Base64url pattern [RFC4648](https://tools.ietf.org/html/rfc4648#section-5) and the elements must be concatenated with “.” (JWS Compact Serialization method as defined in [RFC7515]).

3. The payload of signed messages (request _JWT_ and response _JWT_) shall include the following claims as defined at [RFC7519] (JWT):
  * **aud** (in the _JWT_ request): the Resource Provider (eg the institution holding the account) must validate if the value of the **aud** field matches the endpoint being triggered;
   * **aud** (in _JWT_ response): the API client (eg initiating institution) shall validate if the value of the **aud** field matches its own `organisationId` listed in the directory;
   * **iss** (in the _JWT_ request and in the _JWT_ response): the receiver of the message shall validate if the value of the **iss** field matches the `organisationId` of the sender;
   * **jti** (in the _JWT_ request and in the _JWT_ response): the value of the **jti** field shall be filled with the UUID defined by the institution according to [RFC4122] version 4;
   * **iat** (in the _JWT_ request and in the _JWT_ response): the **iat** field  shall be filled with the message generation time and according to the standard established in [RFC7519](https:// datatracker.ietf.org/doc/html/rfc7519#section-2) to the _NumericDate_ format.

4. The HTTP content-type of requests and responses with JWS messages shall be defined as: "application/jwt".

5. The JOSE header must contain the following attributes:
   * **alg** - shall be filled with the value `PS256`";
   * **kid** - shall be filled with the key identifier value used for the signature;
   * **typ** - shall be filled with the value `JWT`.

* In case of error in signature validation by `Resource Provider` the API provider shall return HTTP error message with `status code` **400** and the `ResponseError` content shall include, in the `code` property, the content `BAD_SIGNATURE`.
* Errors in validating the signed messages received by the client application (eg payment initiator) must be logged and the `Resource Provider` (eg account holding institution) must be notified.

6. The receiver shall validate the consistency of the JWS message's digital signature **exclusively based on the information obtained from the directory**, that is, based on the keys published in the institution's JWKS in the directory.

7. Signatures must be performed using the digital signature certificate specified in the [Open Finance Brazil Certificates Standard](https://github.com/OpenBanking-Brasil/specs-seguranca/blob/main/open-banking-brasil -certificate-standards-1_ID1-ptbr.md#certificate-of-signing-certificatesignature);

8. the _iat_ claim must be numeric in Unix Time format GMT+0 with a tolerance of +/- 60 seconds;

9. the _jti_ claim must be unique for a _clientId_ within a time frame of 86,400 seconds (24h), and cannot be reused within this period. In case of reuse, the HTTP error code 403 shall be return. Any other case must follow RFC 6749 instructions in item 5.2.

## Signing algorithm considerations

For JWS, both clients and Authorization Servers

1. shall use PS256 algorithm;

### Encryption algorithm considerations

For JWE, both clients and Authorization Servers

1. shall use RSA-OAEP with A256GCM

### Secure Use of Transport Layer Security considerations

For TLS, Authorization Server endpoints and Resource Server endpoints used directly by the Client

1. shall support `TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256`
2. shall support `TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384`
3. The "TLS Session Resumption" e "TLS Renegotiation" features shall be disabled

# Data Sharing Considerations

## Authorisation Mechanism

### Introduction

Existing mechanisms for appropriately managing access to resources defined in [RFC6749] are insufficient to meet the requirements for a modern data sharing ecosystem. Leveraging static scope strings does not provide consumers control of sufficient granularity to share with third parties. Open Finance Brasil have elected to implement a [Consent API](https://openbanking-brasil.github.io/areadesenvolvedor/swagger/swagger_consents_apis.yaml) as a OAuth 2.0 protected resource that can be used to manage fine grain access to resources. The reference to the Consent Resource will be conveyed as part of an OAuth 2.0 dynamic resource scope.

### Dynamic Consent Scope Definition

This profile defines OAuth 2.0 dynamic scope "consent" as follows:

* string 'consent'; and
* delimiter of a colon ":"; and
* Consent API REST Resource Id as returned by a successful creation of [Open Finance Consent Resource](https://openbanking-brasil.github.io/areadesenvolvedor/#fase-2-apis-do-open-banking-brasil-api-consentimento);

In addition:

* the Consent Resource Id must include url safe characters only;
* the Consent Resource Id must be namespaced;
* the Consent Resource Id must have the properties of a nonce [Nonce](https://openid.net/specs/openid-connect-core-1_0.html#NonceNotes);

### Dynamic Consent Scope Example

consent:urn:bancoex:C1DD33123

## Authorisation Life Cycle

### Introduction

The Consent Resource has a life cycle that is managed seperately and distinctly from the OAuth 2.0 Authorisation Framework. The state transitions and expected behaviours and error conditions expected of REST Resources protected with this profile are defined in the functional API specifications published by Open Finance Brasil.

### Authorization server

In addition to the requirements outlined in Open Finance Brasil security provisions the Authorization Server

1. shall only issue _access_tokens_ on presentation of a _refresh_token_ when the consent resource the refresh token is bound to is active and with "AUTHORIZED" status;
2. shall only share access to resources when presented with an _access_token_ linked to an active and valid consent;
   2.1. In the Invalid Token Receive scenario, status code 401 should be returned.
3. shall revoke _refresh tokens_ and, _access tokens_ where aplicable, when the linked Consent Resource is deleted;
4. shall ensure _access tokens_ are issued with sufficient scope necessary for access to data specified in the _Permission_ element of a linked Consent Resource object;
5. shall not reject an authorisation request requesting _scopes_ broader than those necessary to access data specified in the Permissions element of a linked Consent Resource object;
6. may reduce requested scope to a level sufficient to enable access to data resources specified in the Permissions element of a linked Consent Resource object;
7. shall retain a complete audit history of the consent resource in accordance with current Central Bank brazilian regulation;
8. shall return authentication failure and return code _access_denied_ in the _error_ parameter (as specified in section 4.1.2.1 of [RFC6749]) if the CPF of the authenticated user is not the same as indicated in the _loggedUser_ element of the Consent Resource Object;
9. shall return authentication failure and return code _access_denied_ in the _error_ parameter (as specified in section 4.1.2.1 of [RFC6749]) if the _businessEntity_ element has not been populated in the related Consent Resource Object and the user has selected or authenticated by using a credential related to a business account;
10. an autenticated or selected business account´s CNPJ must match the value present in the _businessEntity_ element of the Consent Resource Object. In case of divergence authorization server shall return authentication failure and return code _access_denied_ in the _error_ parameter (as specified in section 4.1.2.1 of [RFC6749]);
11. shall ensure _refresh_tokens_ expiration time is at least equal to the linked consent resource expiration time.

### Confidential Client

In addition to the requirements outlined in Open Finance Brasil security provisions the Confidential Client

1. shall revoke where possible and cease usage of _refresh_ and _access tokens_ that are bound to a Consent Resource that has been deleted;
1. shall delete Consent Resource that are expired;

# Acknowledgements

With thanks to all who have set the foundations for secure and safe data sharing through the formation of the OpenID Foundation FAPI Working Group, the Open Finance Brasil GT Security and to the pioneers who will stand on their shoulders.

The following people contributed to this document:

* Alexandre Siqueira (Mercado Pago)
* Joseph Heenan (Authlete)
* Marcos Rodrigues (Itaú)
* Mário Ginglass (BNDES)
* Nic Marcondes (Quanto)
* Ralph Bragg (Raidiam)

{backmatter}

# Notices

Copyright (c) 2022 Open Finance Brasil Initial Structure.

The Open Finance Brasil Initial Structure (OFBIS) grants to any Contributor, developer, implementer, or other interested party a non-exclusive, royalty-free, worldwide copyright license to reproduce, prepare derivative works from, distribute, perform and display, this Implementers Draft or Final Specification solely for the purposes of (i) developing specifications, and (ii) implementing Implementers Drafts and Final Specifications based on such documents, provided that attribution be made to the OFBIS as the source of the material, but that such attribution does not indicate an endorsement by the OFBIS.

The technology described in this specification was made available from contributions from various sources, including members of the OpenID Foundation, the Open Finance Brasil GT Security Working Group and others. Although the Open Finance Brasil Initial Structure has taken steps to help ensure that the technology is available for distribution, it takes no position regarding the validity or scope of any intellectual property or other rights that might be claimed to pertain to the implementation or use of the technology described in this specification or the extent to which any license under such rights might or might not be available; neither does it represent that it has made any independent effort to identify any such rights. The Open Finance Brasil Initial Structure and the contributors to this specification make no (and hereby expressly disclaim any) warranties (express, implied, or otherwise), including implied warranties of merchantability, non-infringement, fitness for a particular purpose, or title, related to this specification, and the entire risk as to implementing this specification is assumed by the implementer. The Open Finance Brasil Intellectual Property Rights policy requires contributors to offer a patent promise not to assert certain patent claims against other contributors and against implementers. The Open Finance Brasil Initial Structure invites any interested party to bring to its attention any copyrights, patents, patent applications, or other proprietary rights that may cover technology that may be required to practice this specification.
