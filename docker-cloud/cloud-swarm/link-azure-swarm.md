---
previewflag: cloud-swarm
description: Link your Microsoft Azure account
keywords: Azure, Cloud, link
title: Link Microsoft Azure Cloud Services to Docker Cloud
---

You can link your [Microsoft Azure Cloud Services](https://portal.azure.com/) account so that Docker Cloud can provision and
manage swarms on your behalf.

For this, you will need an SSH key and your Azure subscription ID to authenticate Docker to your service provider. Also, you need to enable your Azure subscription on behalf of Docker Cloud.

## Create or locate the SSH key you want to use

When you are ready to create and deploy swarms, you must have an [SSH](`/engine/reference/glossary.md#ssh`) key to authenticate Docker Cloud to your Azure account. See the topic [Set up SSH keys](/docker-cloud/cloud-swarm/ssh-key-setup.md) to learn how to check for existing keys or set up a new one, and copy the public key.

## Find your Azure subscription ID

You will also need your Azure Cloud Services subscription ID to provide to
Docker Cloud. There are a few ways to navigate to it on Azure.

You can click a resource from the Dashboard and find the subscription ID under
"Essentials" on the resulting display. Alternatively, from the left menu, go to
**Billing -> Subscriptions -> Subscription ID** or simply click
**Subscriptions**, then click a subscription in the list to drill down.

![](images/azure-subscription-id.png)

When you are ready to add your subscription ID to Docker Cloud,
copy it from your Azure Dashboard.

## Add your Azure account credentials to Docker Cloud

Go to Docker Cloud to connect the account.

1. In Docker Cloud, click the account menu at upper right and select **Cloud settings**.
2. In the **Service Providers** section, click the plug icon next to Microsoft Azure.

    ![](images/azure-id-wizard.png)

3. Provide your subscription ID.

    You will be redirected to [Azure Cloud Services](portal.azure.com).

4. Log in to your Azure account.

5. Click **Accept** to grant Docker Cloud access to your Microsoft Azure account.

    ![](images/azure-permissions.png)

6. Your Microsoft Azure login credentials will automatically populate to
Docker Cloud under **Service Providers -> Microsoft Azure**.

    ![](images/azure-creds-cloud.png)

7. Click **Save**.

## Enable your Azure subscription for Docker Cloud

You need to verify Microsoft Azure terms of use and manually enable your Azure subscription on behalf of Docker Cloud.

1.  Go to the [Microsoft Azure Marketplace](https://portal.azure.com/#blade/Microsoft_Azure_Marketplace/GalleryFeaturedMenuItemBlade/selectedMenuItemId/home) and search for **Docker**, or specifically **Docker for Azure CE**.

    ![](images/azure-eula-1-marketplace.png)

2. Select **Docker for Azure CE** and click the option on the lower right to deploy programmatically.

    ![](images/azure-eula-2-deploy-vm.png)

3. Read the terms of use, click **Enable** for your subscription, and click **Save**.

    ![](images/azure-eula-3-enable-subscription.png)

4. Verify that your subscription is enabled.

    Go to **Dashboard -> Subscriptions** to view details on your current subscriptions. Docker for Azure CE should be listed as enabled Programmatic deployment.

    ![](images/azure-eula-4-verify.png)

You're now ready to deploy a swarm!

## Where to go next

**Ready to create swarms on Azure?** See [Create a new swarm on Microsoft Azure in Docker Cloud](create-cloud-swarm-azure.md).

You'll need an SSH key to provide to Docker Cloud during the swarm create
process. If you haven't done so yet, check out how to [Set up SSH
keys](ssh-key-setup.md).

You can get an overivew of topics on [swarms in Docker Cloud](index.md).
