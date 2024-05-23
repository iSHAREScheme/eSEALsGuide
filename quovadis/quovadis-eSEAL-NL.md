# Getting eSEAL eIDAS certificate in NL from Quo-Vadis

> Note: the previously described process is not currently recommended by Quovadis staff. 


** What you need to prepare **
1. KvK uittreksel
2. Identity documents of 'bevoegd bestuurder(s)'
3. Identity documents of certificate manager (can also be the bestuurder)
4. Payment form (invoice, creditcard or iDeal)

** Application in Quovadis webshop **
1. Go to https://quovadissupport.nl/modules/
2. Select Quovadis Qualified eSeal certificaat
3. Walk through the process
4. If prompted, select the formfactor **software** for the certificate. Not the HSM or USB version. Previously, the software version was called the Non-QCSD. For asking digital certificate file make sure to select "Non-QCSD" option so that you recive digital certificate file.

Depending on your internal application architecture and security requirements you must ask for your digital certifcate in appropriate form. If you do use specific security instruments like HSMs or valuts or if you are not sure about it please ask for a digital certificate file. 

** After application, you receive a request to generate a CSR **
If you selected Non-QSCD option, you will be asked to provide a CSR file, kindly follow the process mentioned below:

You can generate a CSR using following guide
[Refer to CSR guide here:](../CSR.md)
