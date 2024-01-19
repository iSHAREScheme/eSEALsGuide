# eSEAL certificate procurement guide.

This repo is collection of processes from various CAs who list out how to procure eSEALs certificates. Currently, in iSHARE only eIDAS eSEALs are supported.

> [!NOTE]  
> This guide is provided as a help to participants and provided based on personal experience or based on knowledge. Although all care is being taken while providing the content, neither iSHARE Foundation nor the contributors can be held liable for any incorrectness or errors or any loss you may incur. It is highly encouraged of you to also contribute to this guide for new content or provide correct/latest information to help fellow participants. 

### Choosing the right Certificate Authority and the right issuer 

eIDAS provides a link to find the current issuers per country (Trusted Issuer Browser List):

Browse to the link below and select your country --> select the preferred **Certificate Authority** then expand the section with the title **"Qualified certificate for electronic seal"** and it shows the names of the issuer who can issue this kind of certificate. When requesting certificate from your CA, please make sure to ask them that the resulting certificate will be issued by one of the issuers mentioned in this link. **This is important as only certificates issued by issuers listed on the link above are accepted.**

[eIDAS Trusted Issuer Browser List](https://eidas.ec.europa.eu/efda/tl-browser/#/screen/home) (ctrl/cmd + click to open in new tab/window)

>[!WARNING]  
>Before ordering and paying for a certificate, please make sure to check with the Certificate Authority (Certificate Provider) that the eSEAL certificate can be obtained as a certificate file! Note that you will need the certificate file to be configured into your application with appropriate security measures as per your organisations security policy. Alternatively, if you plan to use (Cloud based) Hardware Security Modules (HSM) or Vaults please check the provider manual on best way to request for certificate using inbuilt mechanisms.

### Country/Certificate Authority specific guide

Process to get eSEAL from specific CA is listed below by the name of the CA. Each CA or users must add their own process documentation along with country specifics if applicable to their own folder

| Certificate Authority | Country | Issuer process |
| ----------------------|---------|---------------------------------------|
| QuoVadis Trustlink B.V. | Netherlands | [QuoVadis EU Issuing Certification Authority G4](quovadis/quovadis-eSEAL-NL.md)|

> **_NOTE:_** iSHARE Foundation has no affliation with QuoVadis and nor promotes it in any way. The guide here to acquire eSEAL certificate is provided based on experience iSHARE Foundation itself had in the process of acquiring the certificate and is provided for educational purposes only. Other providers process can be contributed by either themselves or by community memnbers for benefit of others.



### Generating CSR when requested by your Certificate Authority

[Please refer to CSR guide here](CSR.md)
