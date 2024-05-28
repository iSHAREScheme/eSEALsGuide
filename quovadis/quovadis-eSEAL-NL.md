# Getting eSEAL eIDAS certificate in NL from Quo-Vadis

> Note: this is guide based on experience and for latest process always check with Quovadis.


** What you need to prepare **
1. KvK uittreksel
2. Identity documents of 'bevoegd bestuurder(s)'
3. Identity documents of certificate manager (can also be the bestuurder)
4. Payment form (invoice, creditcard or iDeal)

** Application in Quovadis webshop **
1. Go to https://quovadissupport.nl/modules/
2. Select Quovadis Qualified eSeal certificaat
3. Walk through the process
4. If prompted, select the form factor **software** for the certificate, as this results into a digital certificate file. Not the HSM or USB version. Previously, the this option was called Non-QCSD, which resulted in a digital certificate file.

Depending on your internal application architecture and security requirements you must ask for your digital certifcate in appropriate form. If you do use specific security instruments like HSMs or valuts or if you are not sure about it please ask for a digital certificate file. 

** After application, you receive a request to generate a CSR **
If you selected form factor Software/Non-QSCD option, you will be asked to provide a CSR file, kindly follow the process mentioned below:

You can generate a CSR using following guide
[Refer to CSR guide here:](../CSR.md)
