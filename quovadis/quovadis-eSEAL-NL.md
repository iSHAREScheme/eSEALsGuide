# Getting eSEAL eIDAS certificate in NL from Digicert QuoVadis

This manual explains how to procure qualified or advanced eSeals from Digicert QuoVadis.

> [!NOTE]
> This is guide based on experience and for latest process always check with Digicert QuoVadis.

## What you need to prepare

1. KvK uittreksel
2. Identity documents of 'bevoegd bestuurder(s)'
3. Identity documents of certificate manager (can also be the bestuurder)
4. Payment form (invoice, creditcard or iDeal)

## Application in Digicert webshop

1. Go to <https://certcentral.digicert.eu/>
2. Select EU Qualified seal (not the PSD2 variant)

### For advanced eSeals

4. Under key delivery method select 'Provide Certificate Signing Request (CSR)'
5. Upload your CSR (for more information about creating a CSR, see [this guide on CSRs](../CSR.md)).

> [!WARNING]
> Depending on your internal application architecture and security requirements you must ask for your digital certifcate in appropriate form. If you do use specific security instruments like HSMs or valuts the please select the right option or check with the CA for the right option. If you are not sure about it please ask for a digital certificate in a file which can be deployed in your application. Ofcourse do not forgot the appropriate security measures as per your organisations policies. 