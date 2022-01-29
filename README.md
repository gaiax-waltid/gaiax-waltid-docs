# gaiax-waltid-docs



- Wallet integration: Delivery of a custodial wallet (incl. user interface) that enables people to connect to the marketplace.
- Issuer & Verifier Portals: Delivery of portals that enable users to
  - request the issuance of data (Verifiable Credentials) from the OCEAN marketplace into their wallet
  - present data (Verifiable Presentations) from the wallet to the OCEAN marketplace
- Credentials: Definition and implementation of selected Verifiable Credential types, including their publication in our “VC Lib” (library of typesafe credentials), e.g.:
   - KYC/B Credentials: Identification of individuals and legal entities (Know Your Customer / Business)
   - Membership Credentials (e.g. Gaia-X)
   - Data Service Provider Credentials (Provider Description)
   - Data Service Offering Credentials (Application Description)
   - Data Consortium / DAO Credentials (Dataspace X, DAO Y)
   - Data Security Credentials (ISO 27001)


| Credential    |  Schema |  Implementation |
|----------|:-------------:|------:|  
|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schema/DataConsortium.json)| [DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataConsortium.kt)| 
|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataSelfDescription.json)|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/DataSelfDescription.json)|[DataSelfDescription](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataSelfDescription.kt)|
|[DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataServiceOffering.json)|[DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/DataServiceOffering.json)| [DataServiceOffering](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/DataServiceOffering.kt)|
|[DataConsortium](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[GaiaxCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/GaiaxCredential.json)| [GaiaxCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/GaiaxCredential.kt)|
|[Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/Iso27001Certificate.json)|[Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/Iso27001Certificate.json)| [Iso27001Certificate](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/Iso27001Certificate.kt) |
|[KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/DataConsortium.json)|[KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KybCredential.json)| [KybCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KybCredential.kt) |
|[KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/KybMonoCredential.json)|[KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KybMonoCredential.json)| [KybMonoCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KybMonoCredential.kt) |
|[KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/KycCredential.json)|[KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/KycCredential.json)| [KycCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/KycCredential.kt) |
|[ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/serialized/ParticipantCredential.json)|[ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/tree/master/src/test/resources/schemas/ParticipantCredential.json)| [ParticipantCredential](https://github.com/walt-id/waltid-ssikit-vclib/blob/master/src/main/kotlin/id/walt/vclib/credentials/gaiax/ParticipantCredential.kt) |


- Verification Policies: Definition and implementation of custom verification policies (aligned with the “Credentials”) for customizable and granular access control.

