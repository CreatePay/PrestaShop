# CreatePay for PrestaShop

A payment module for PrestaShop that enables merchants to accept payments through the Cardstream payment gateway.

## Compatibility

- **PrestaShop:** Version 1.7 and above

## Requirements

The following credentials and configuration details are required to set up the module:

- Merchant ID
- Signature/Secret Key (Passphrase)
- Gateway URL

**HTTPS is mandatory for processing direct payments.** Direct payments must not be processed over an unsecured HTTP connection.

If you already have a CreatePay account, please contact [createcommerce@createpay.com](mailto:createcommerce@createpay.com).

For all other enquiries, please contact [hello@createpay.com](mailto:hello@createpay.com).

## Installation

There are two ways to install the CreatePay PrestaShop module.

### Option 1: Install via the PrestaShop Admin Panel

#### Step 1: Upload the Module

1. Log in to your PrestaShop Admin Panel.
2. Navigate to **Modules > Modules Catalog** using the left-hand menu.
3. Click **Upload a module**.
4. Select the module's ZIP file and upload it.
5. Wait for the upload to complete.

#### Step 2: Install the Module

1. Once the module has been uploaded, locate the search box in the Modules Catalog.
2. Search for `Cardstream`.
3. When the module appears in the search results, click **Install**.
4. Wait for the installation to complete. The page should refresh automatically.
5. Click **Configure** to open the module settings.

#### Step 3: Configure the Module

Once the configuration page opens, enter the required details:

- **Merchant ID:** Your CreatePay merchant ID.
- **Passphrase:** Your payment gateway signature/secret key.
- **Frontend:** Enter a message to display to customers during checkout.

Examples of frontend messages include:

- `Process payments with Cardstream`
- `Cardstream`

**Important:** The Frontend field is mandatory. The module will not work unless this field is completed.

Click **Update Settings** to save your configuration.

### Option 2: Manual Installation

#### Step 1: Copy the Module Files

1. Locate the `httpdocs` folder included with the module.
2. Copy its contents into the root directory of your PrestaShop installation.
3. If prompted to replace existing files, select **Yes**.

#### Step 2: Install the Module

1. Log in to your PrestaShop Admin Panel.
2. Navigate to **Modules > Modules Catalog**.
3. Search for `Cardstream` using the search box.
4. When the module appears, click **Install**.
5. Wait for the installation to complete. The page should refresh automatically.
6. Click **Configure** to access the module settings.

#### Step 3: Configure the Module

Enter the following details in the module configuration page:

- **Merchant ID:** Your CreatePay merchant ID.
- **Passphrase:** Your payment gateway signature/secret key.
- **Frontend:** A message asking customers to pay using Cardstream.

For example:

```text
Process payments with Cardstream
```

Alternatively, you can simply use:

```text
Cardstream
```

Ensure that the Frontend field is completed, then click **Update Settings** to save your configuration.

## Configuration

Before using the module, ensure that all required settings have been entered and saved.

### Payment Configuration

| Setting | Description | Required |
| --- | --- | --- |
| Merchant ID | Your CreatePay merchant ID. | Yes |
| Passphrase | Your payment gateway signature/secret key. | Yes |
| Frontend | The message displayed to customers during checkout. | Yes |
| Gateway URL | The payment gateway endpoint required for your integration. | As applicable |

> **Important:** All settings must be saved before the module can be used. The Frontend field must not be left empty.

### HTTPS Requirements

Direct payments must only be processed over HTTPS.

Ensure that your PrestaShop installation has a valid SSL certificate and that HTTPS is enabled before processing direct payments.

## Branded Version

The PrestaShop module can be customised to meet individual customer requirements.

The module supports branding through its Settings API. This allows developers to change the module's displayed name and default configuration settings.

### Customising the Module

To customise the module, update the following files:

| File | Purpose |
| --- | --- |
| `httpdocs/modules/cardstream/config.php` | Update the module's default settings. |
| `httpdocs/modules/cardstream/config.xml` | Update how PrestaShop identifies and displays the module. |

#### 1. Update the Default Settings

Open:

```text
httpdocs/modules/cardstream/config.php
```

Modify the default settings as required for your branded version.

#### 2. Update the Module Information

Open:

```text
httpdocs/modules/cardstream/config.xml
```

The following fields can safely be modified to customise the module's appearance:

- `description`
- `displayName`
- `author`

These fields allow you to customise the module's description, displayed name and author information within PrestaShop.

> **Note:** Only modify the fields listed above in `config.xml` unless you have verified that other changes are compatible with the module.

After making your changes, save the files and ensure that the module is configured correctly before deploying it.

## Troubleshooting

### The Module Is Not Visible in the Modules Catalog

**Problem:** The Cardstream module does not appear in the PrestaShop Modules Catalog after installation.

**Solution:**

1. Ensure that the module files have been uploaded to the correct directory.
2. Verify that the module is installed correctly.
3. Search for `Cardstream` in the Modules Catalog again.
4. If the module is still missing, check the installation files and PrestaShop logs.

### The Module Is Not Working After Configuration

**Problem:** The module does not function correctly after installation.

**Solution:**

Check the following:

- Ensure that your Merchant ID is correct.
- Verify that the Passphrase has been entered correctly.
- Confirm that the Frontend field is populated.
- Ensure that all settings have been saved by clicking **Update Settings**.
- Verify that your payment gateway configuration is correct.

### Direct Payments Are Not Working

**Problem:** Direct payments cannot be processed.

**Solution:**

Ensure that HTTPS is enabled on your PrestaShop installation and that your website has a valid SSL certificate.

Direct payments over HTTP are not permitted.

If the problem persists, contact CreatePay Support.

## Disclaimer

The sample code, SDKs and modules provided are intended for reference purposes only.

Modules are developed and tested against standard, unmodified installations of the supported platform. Any additional compatibility requirements must be tested by the user, merchant or developer.

Version support is specified in the relevant **Compatibility** section.

All sample code, SDKs and modules provide foundational transaction functionality for merchants and developers to use as a guide or to adapt, enhance and extend to meet their requirements. Some desired functionality may not be available or supported.

All sample code, SDKs and modules must undergo complete end-to-end testing by the user, merchant or developer before being used in a live environment.

Cardstream accepts no responsibility, provides no warranty and accepts no liability arising from changes, modifications or errors in functionality resulting from the use of these sample materials.

By using any of the provided sample code, SDKs or modules, developers, merchants and other users accept these conditions.

## Support

For assistance with an existing CreatePay account, please contact:

- **Existing CreatePay accounts:** [createcommerce@createpay.com](mailto:createcommerce@createpay.com)
- **General enquiries:** [hello@createpay.com](mailto:hello@createpay.com)
