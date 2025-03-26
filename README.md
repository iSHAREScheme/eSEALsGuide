# eSEAL certificate procurement guide

>[!WARNING]
>This guide assumes that the reader has some basic understanding of Digital Certificates and PKI (public key infrastructure, private/public key pairs). If you are not familiar with it, then kindly familiarise yourself (out of scope of this guide) or ask your trusted colleague with this knowledge before proceeding.

The [iSHARE Framework](https://framework.ishare.eu) requires participants that take part in machine-to-machine (M2M) communication (for instance the consumption of APIs) to use advanced or qualified eIDAS eSeals (as stated in the [admission criteria](https://framework.ishare.eu/detailed-descriptions/operational/operational-processes/admission#admission-admissioncriteria)). This repository explains how qualified and advanced eIDAS eSeals can be purchased and used in the context of the iSHARE Framework. This repo furthermore contains a registration of self experience with qualified eSeal providers and aims to lower barriers to procure and use eIDAS eSeals.

> [!NOTE]  
> This guide is provided as a help to participants and provided based on personal experience or with the CA's themselves. Although all care is being taken while providing the content, neither iSHARE Foundation nor the contributors can be held liable for any incorrectness or errors or any loss you may incur. It is highly encouraged of you to also contribute to this guide for new content or provide correct/latest information to help fellow participants.

## Choosing the right Certificate Authority and the right issuer

The complete list of all eIDAS qualified eSeal providers is available from the [EU eIDAS trust services browser](https://eidas.ec.europa.eu/efda/trust-services/browse/eidas/tls/search/type?step=3&searchCriteria=eyJzZXJ2aWNlU2NvcGUiOiJBTEwiLCJjb3VudHJ5Q29kZXMiOlsiQVQiLCJCRSIsIkJHIiwiSFIiLCJDWSIsIkNaIiwiREsiLCJFRSIsIkZJIiwiRlIiLCJERSIsIkVMIiwiSFUiLCJJUyIsIklFIiwiSVQiLCJMViIsIkxJIiwiTFQiLCJMVSIsIk1UIiwiTkwiLCJOTyIsIlBMIiwiUFQiLCJSTyIsIkVTIiwiU0siLCJTSSIsIlNFIiwiVUsiXSwic2VydmljZVR5cGVzIjpbIlFDZXJ0RVNlYWwiXX0%3D).

If the link above does not automatically bring you to the list of eIDAS eSeal providers, the browse to [https://eidas.ec.europa.eu/efda/trust-services/browse/eidas/tls](https://eidas.ec.europa.eu/efda/trust-services/browse/eidas/tls) and start you search from there.

## Delivery methods of eSeals

### Qualified eSeals

An eSeal consists of a public key (certificate) and a private key. For qualified eSeals, the private key is provided in and can only be used through a Qualified Electronic Seal Creation Device (QESCD). These devices come in the form of:

- USB-tokens
- Smartcards
- HSMs (Hardware Security Modules)

If you plan on using a qualified eSeal, make sure that your application can use the QESCD to seal communication (iSHARE JWTs). With qualified eSeals the private key is **never** delivered as a file.

### Advanced eSeals

Some parties also provide eiDAS advanced eSeals. For these kinds of eSeals the private key can be delivered as a file, or (better) using Certificate Signing Requests (CSR) where the you create the private key yourself and the key never leaves the system.

### Make sure you will be able to use the eSeal

Before ordering and paying for a certificate, please make sure that you are able to use the eSeal in your application. This means either using the QESCD to seal (for qualified eSeals) or using the public/private keypair as files to seal (for advanced eSeals). Note that you will need the eSeal to be configured into your application with appropriate security measures as per your organisations security policy. Alternatively, if you plan to use (Cloud based) Hardware Security Modules (HSM) or Vaults please check the provider manual on best way to request for certificate using inbuilt mechanisms.

## Country/Certificate Authority specific guide

Process to get eSEAL from specific CA is listed below by the name of the CA. Each CA or users must add their own process documentation along with country specifics if applicable to their own folder

### The Netherlands

| Certificate Authority | Qualified eSeal                  | Advanced eSeal | Issuer process                                |
|-----------------------|----------------------------------|----------------|-----------------------------------------------|
| Digicert QuoVadis     | Yes (USB, HSM, QuoVadis HSM)     | Yes            | [link](./quovadis/quovadis-eSEAL-NL.md)       |
| Digidentity           | Yes (Digidentity HSM)            | No             | [link](./digidentity/digidentity-eSeal-NL.md) |
| KPN                   | Yes (USB, Smartcard, Phone, HSM) | No             | [link](./kpn/kpn-eSeal-NL.md)                 |

> [!NOTE]
> iSHARE Foundation has no affiliation with any provider (CA) and nor promotes them in any way. The guides here are provided based on experience to acquire eSEAL certificates and are provided for educational purposes only. Additional providers' process can be contributed by either themselves or by community members for benefit of others.

### Generating CSR when requested by your Certificate Authority

Often when requesting the certificate in file format (for advanced eSeals), the requestor is needed to provide a Certificate Singing Request (CSR) to the issuing CA. This is necessary to keep your private key private and secure as it must never be shared with others.

[Please refer to CSR guide here](CSR.md)
