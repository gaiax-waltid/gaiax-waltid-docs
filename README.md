# Gaia-X Self-Sovereign Identity powered by the Ocean Protocol

This documentation outlines the usage of the walt.id SSI stack to build a SSI-based user-authentication solution. The demo-use case shows the Gaia-X Portal, which authenticates users by processing their presented _ParticipantCredential_ (see below).
The architecture is built upon the SSI standards ([W3C Decentralized Identifiers (DIDs)](https://www.w3.org/TR/did-core/), [W3C Verifiable Credentials (VCs)](https://www.w3.org/TR/vc-data-model/),[Self-Issued OpenID Provider v2 (SIOPv2)](https://openid.net/specs/openid-connect-self-issued-v2-1_0-06.html), [OpenID Connect for Verifiable Presentations (OIDC4VP)](https://openid.net/specs/openid-connect-4-verifiable-presentations-1_0-07.html)) and utilizes the [Ocean Protocol](https://oceanprotocol.com/) as foundation.


## Integration and Demo

This video demos the SSI wallet integration with the Gaia-X portal. https://www.youtube.com/watch?v=kXsUhzFIksU
[![Gaia-X Portal SSI-Integration Demo](https://img.youtube.com/vi/kXsUhzFIksU/0.jpg)](https://www.youtube.com/watch?v=kXsUhzFIksU "Gaia-X Portal SSI-Integration Demo")

The demo can be accessed by the following links and credentials:

- Gaia-X portal: https://gaiax-portal.walt.id
- Web Wallet: https://wallet.walt.id

Wallet-account with valid credential: **auth-ok@example.com**
Wallet-account with invalid credential: **auth-fail@example.com**

In both cases you can type any password as this demo has no authentication-solution for the wallet enabled.

## Credentials for Gaia-X

- The following Verifiable Credentials for the Gaia-X use case were definition and implementation in our “VC Lib” (library of typesafe credentials), e.g.: https://github.com/walt-id/waltid-ssikit-vclib
   - KYC/B Credentials: Identification of individuals and legal entities (Know Your Customer / Business)
   - Membership Credentials (e.g. Gaia-X)
   - Data Service Provider Credentials (Provider Description)
   - Data Service Offering Credentials (Application Description)
   - Data Consortium / DAO Credentials (Dataspace X, DAO Y)
   - Data Security Credentials (ISO 27001)


| Credential    |  Schema |  Implementation |
|----------|:-------------:|------:|  
|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/test/resources/schemas/DataConsortium.json)| [DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataConsortium.kt)| 
|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataSelfDescription.json)|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/DataSelfDescription.json)|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataSelfDescription.kt)|
|[DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataServiceOffering.json)|[DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/DataServiceOffering.json)| [DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataServiceOffering.kt)|
|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[GaiaxCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/GaiaxCredential.json)| [GaiaxCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/GaiaxCredential.kt)|
|[Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/Iso27001Certificate.json)|[Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/Iso27001Certificate.json)| [Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/Iso27001Certificate.kt) |
|[KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KybCredential.json)| [KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KybCredential.kt) |
|[KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/KybMonoCredential.json)|[KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KybMonoCredential.json)| [KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KybMonoCredential.kt) |
|[KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/KycCredential.json)|[KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KycCredential.json)| [KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KycCredential.kt) |
|[ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/ParticipantCredential.json)|[ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/ParticipantCredential.json)| [ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/ParticipantCredential.kt) |




