# Generating CSR to be sent to you CA

When requested by your CA, you must generate a CSR for your certificate request. There are various ways through which you can generate one:

1. Using a CSR generator offered by a Keyvault.
2. Using OpenSSL.
3. Using MacOS Keychain.

>[!WARNING]
>Never generate a CSR using online tools!

## Specific eIDAS certificate requirements

When creating a CSR, make sure you comply with eIDAS specific requirements for certificates. The following requirements are relevant:

- Include mandatory attributes for legal persons ([ETSI EN 319 412-2](https://www.etsi.org/deliver/etsi_en/319400_319499/31941202/02.02.02_60/en_31941202v020202p.pdf)):
  - organizationName (2.5.4.10)
  - countryName (2.5.4.6)
  - organizationIdentifier (2.5.4.97)
- Include organizationIdentifier in valid format ([ETSI EN 319 412-1](https://www.etsi.org/deliver/etsi_en/319400_319499/31941201/01.04.02_60/en_31941201v010402p.pdf))

Summary for eIDAS Qualified eSeal Certificates:

| Attribute                | OID      | Required | Example        |
| ------------------------ | -------- | -------- | -------------- |
| `organizationName`       | 2.5.4.10 | Yes      | Test B.V.      |
| `countryName`            | 2.5.4.6  | Yes      | NL             |
| `organizationIdentifier` | 2.5.4.97 | Yes      | NTRNL-12345678 |
| `commonName`             | 2.5.4.3  | Optional | Test B.V.      |

## 1. CSR creation from Keyvault

We don't offer specific information about creating CSRs in specific Keyvaults. More background information is available in [this article about using eSeals and Keyvaults](https://trustbok.ishare.eu/apply-ishare/eseals-and-key-vaults).

## 2. CSR creation with OpenSSL

The following section has been tested with OpenSSL 3.3.2 on Windows (find installable [here](https://github.com/openssl/openssl/wiki/Binaries)) and should work with OpenSSL 3.x on any system. 

Use the following config file as a template and fill it with your own information. Store as `openssl-csr-config.cnf`. Available as download [here](./openssl-csr-config.cnf).

```ini
[ req ]
default_bits = 2048
prompt = no
distinguished_name = dn
req_extensions = v3_req
oid_section = custom_oids

[ custom_oids ]
organizationIdentifier = 2.5.4.97

[ dn ]
C = NL                                  #Replace with actual 2 letter country code
O = Test B.V.                           #Replace with company name
CN = Test B.V.                          #Replace with company name
organizationIdentifier = NTRNL-12345678 #Replace with ETSI EN 319 412-1 compliant organization identifier

[ v3_req ]
keyUsage = critical, digitalSignature, nonRepudiation
```

>[!NOTE]
>DN can be extended with other known attributes if preferred/required

Then run the following command to create a private key:

```bash
openssl genpkey -algorithm RSA -out private.key -pkeyopt rsa_keygen_bits:2048 -aes256
```

>[!NOTE]
>If you don't want to secure the private key with a password, omit the -aes256 option.

Finally run the following command to create the CSR:

```bash
openssl req -new -key private.key -out testbv.csr -config openssl-csr-config.cnf
```

## 3. CSR creation with MacOS Keychain

For convenience here is the process for how to do it on Mac OS and what options to use. If you use another method, please note the options used below

For MacOS users:

- Open Keychain Access app (you can use cmd+space to search for the keychain access app or find in "Other" folder under your "Launchpad")
- On the menu --> Keychain Access --> Certificate Assistant --> Request a certificate from a certificate authority
- A wizard opens, follow the wizard to generate CSR
- Make sure not to put personal information, but instead put company information.Common name should be your company name
- Choose saved to disk and check "let me specify  key pair information"
- Provide a name and select where the csr file must be stored (remember this location and file name)
- Key size must be minimum 2048 bits
- Algorithm must be RSA
- Done.

The CSR file is generated and saved at the chosen location. This file must be sent to your CA (or uploaded on their portal)
The Private key is also stored in the keychain and can be exported from it.

>[!WARNING]
>BEWARE: on the system you generate your CSR you also generate and store the private key. It is important to keep private key secure at all times.

## Additional information

More information about CSRs is available here: [https://www.digicert.com/kb/csr-creation.htm](https://www.digicert.com/kb/csr-creation.htm).
