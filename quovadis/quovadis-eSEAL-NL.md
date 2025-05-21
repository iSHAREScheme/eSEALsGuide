# Getting eSEAL eIDAS certificate in NL from Digicert QuoVadis

This manual explains how to procure qualified or advanced eSeals from Digicert QuoVadis.

> [!NOTE]
> This is guide based on experience and for latest process always check with Digicert QuoVadis.

## What you need to prepare

1. KvK uittreksel
2. Identity documents of 'bevoegd bestuurder(s)'
3. Identity documents of certificate manager (can also be the bestuurder)
4. Payment form (invoice, creditcard or iDeal)

## Application in Digicert QuoVadis webshop

1. Go to <https://www.digicert.com/qualified-certificates/compare-eu-document-signing?ev_comparision_chart=active>
2. Select EU Qualified seal (not the PSD2 variant)
3. Walk through the process

### For advanced eSeals

4. If prompted, select the form factor **software** for the certificate (also called Non-QCSD), as this results into a digital certificate file. Not the HSM or USB version.
5. After application, if you selected form factor Software/Non-QSCD option, you will be asked to provide a CSR file, kindly refer to [this guide on CSRs](../CSR.md).

> [!WARNING]
> Depending on your internal application architecture and security requirements you must ask for your digital certifcate in appropriate form. If you do use specific security instruments like HSMs or valuts the please select the right option or check with the CA for the right option. If you are not sure about it please ask for a digital certificate in a file which can be deployed in your application. Ofcourse do not forgot the appropriate security measures as per your organisations policies. 