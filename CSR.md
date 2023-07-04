# Generating CSR to be sent to you CA

When requested by your CA, you must generate a CSR for your ceritificate request. There are various ways through which you can generate one. 
>Never generate one using online tools!

Refer to following link which lists various options on how to generate a CSR [https://www.digicert.com/kb/csr-creation.htm]

For convenience I have listed process for how to do it on Mac OS and what options to use. If you use another method, please note the options used below
For MacOS users:

- Open Keychain Access app (you can use cmd+space to search for the keychain access app or find in "Other" folder under your "Launchpad")
- On the menu --> Keychain Access --> Certificate Assistant --> Request a certificate from a certificate authority
- A wizard opens, follow the wizard to generate CSR
- Make sure not to put personal information, but instead put company information. Common name should be your company name
- Choose saved to disk and check "let me specify  key pair information"
- Provide a name and select where the csr file must be stored (remember this location and file name)
- Key size must be minimum 2048 bits
- Algorithm must be RSA
- Done.

The CSR file is generated and saved at the choosen location. This file must be sent to your CA (or uploaded on their portal)
The Private key is also stored in the keychain and can be exported from it.

>BEWARE: on the system you generate your CSR you also generate and store the private key. It is important to keep private key secure at all times. 
