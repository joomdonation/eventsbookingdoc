---
title: Payrexx
visible: true
published: true
media_order: payrexx-webhook.png
---

## Installation

After purchasing the plugin, go to **Events Booking -> Payment Plugins** and install **os_eb_payrexx.zip**. See [Install Payment Plugin](https://eventbookingdoc.joomservices.com/basic-setup/payment-plugins#install-new-payment-plugin) for the steps.

## Configuration

1. Open the payment plugin, enter the following parameters, then publish the plugin and save your changes:

    - **Instance Name**: This is part of the URL you use to access Payrexx. For example, if the URL is `https://joomdonation.payrexx.com`, the **Instance Name** is **joomdonation**.
    - **API Key**: Log in to Payrexx and go to **Integrations -> API & Plugins** to get your API key.

2. Go to **Integrations -> Webhooks** and create a webhook with the following settings.

    - **Webhook URL**: Enter the following URL, replacing `https://domain.com/` with your site's URL:

        ```text
        https://domain.com/index.php?option=com_eventbooking&task=payment_confirm&payment_method=os_payrexx
        ```

    - **Events**: Select only **Transactions**.
    - **Webhook Type**: Select **Normal (PHP-Post)**.

    ![Payrexx webhook settings](payrexx-webhook.png "Payrexx webhook settings")
