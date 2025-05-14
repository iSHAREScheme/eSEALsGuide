# Digidentity eSeal procurement guide

This file explains how to procure an eIDAS Qualified eSeal from Digidentity. When procuring an eSeal from Digidentity, the eSeal is provided in the Digidentity cloud HSM and not on a USB token or smartcard.

## Procurement process

- Product information is available [here](https://www.digidentity.eu/nl/services/e-signatures/e-seal-qualified-and-autosign)
- Click on this page on 'Direct eSeal aanvragen' to start the procurement process
- The onboarding process is fully digitized and requires no paperwork
- Reach out to Digidentity to request access to the Autosigner

> [!NOTE]
> When using the Digidentity Autosigner, usage charges may apply.

## Using the eSeal

The eSeal can be used to sign JWTs using the [autosigner API](https://docs.digidentity.com/#912f1f8e-8e93-4e5c-ba14-1b0ae7175fca).

- Example implementation [here](https://ishare-digidentity-signing-pilot.azurewebsites.net/)
- Source code [here](https://github.com/gerardishare/digidentity-jwt-sign-poc)