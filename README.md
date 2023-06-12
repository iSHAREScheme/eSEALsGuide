# eSEAL certificate procurement guide.

This repo is collection of processes from various CAs who list out how to procure eSEALs certificates. Currently, in iSHARE only eIDAS eSEALs are supported.


### Choosing the right Certificate Authority and the right issuer 

eIDAS provides a link to find the current issuers per country:

[https://eidas.ec.europa.eu/efda/tl-browser/#/screen/home]

Browse to the link above and select your country --> select the preferred Certificate Authority then expand the section with the title **"Qualified certificate for electronic seal"** and it shows the names of the issuer who can issue this kind of certificate. When requesting certificate from your CA, please make sure to ask them that the resulting certificate will be issued by one of the issuers mentioned in this link. This is important as only certificates issued by issuers listed on the link above are accepted.

### Country/Certificate Authority specific guide

Process to get eSEAL from specific CA is listed below by the name of the CA. Each CA must add their own process documentation along with country specifics if applicable to their own folder

| Certificate Authority | Country | Issuer process |
| ----------------------|---------|---------------------------------------|
| QuoVadis Trustlink B.V. | Netherlands | [QuoVadis EU Issuing Certification Authority G4](quovadis/quovadis-eSEAL-NL.md)|

> **_NOTE:_** iSHARE Foundation has no affliation with QuoVadis and nor promotes it in any way. The guide here to acquire eSEAL certificate is provided based on experience iSHARE Foundation itself had in the process of acquiring the certificate and is provided for educational purposes only. Other providers process can be contributed by either themselves or by community memnbers for benefit of others.



### Generating CSR when requested by your Certificate Authority

[Please refer to CSR guide here](CSR.md)
