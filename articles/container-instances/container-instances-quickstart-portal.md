---
title: Quickstart - Create your first Azure Container Instances container with the Azure portal
description: In this quickstart, you use the Azure portal to deploy a container in Azure Container Instances
services: container-instances
author: mmacy
manager: timlt

ms.service: container-instances
ms.topic: quickstart
ms.date: 04/02/2018
ms.author: marsma
ms.custom: mvc
---

# Quickstart: Create your first container in Azure Container Instances

Azure Container Instances makes it easy to create and manage containers in Azure. In this quickstart, you create a container in Azure and expose it to the internet with a public IP address. This operation is completed by using the Azure portal. With just a few clicks, you will see this in your browser:

![App deployed using Azure Container Instances viewed in browser][aci-portal-07]

## Log in to Azure

Log in to the Azure portal at http://portal.azure.com.

## Create a container instance

Select the **Create a resource** > **Containers** > **Azure Container Instances**.

![Begin creating a new container instance in the Azure portal][aci-portal-01]

Enter the following values in the **Container name**, **Container image**, and **Resource group** text boxes. Leave the other values at their defaults, then click **OK**.

* Container name: `mycontainer`
* Container image: `microsoft/aci-helloworld`
* Resource group: `myResourceGroup`

![Configuring basic settings for a new container instance in the Azure portal][aci-portal-03]

You can create both Windows and Linux containers in Azure Container Instances. In this quickstart, we'll leave the default setting of **Linux** since we specified a Linux-based container (`microsoft/aci-helloworld`) in the previous step.

Leave the other settings in **Configuration** at their defaults, then click **OK** to validate the configuration.

![Configuring a new container instance in the Azure portal][aci-portal-04]

When the validation completes, you are shown a summary of your container settings. Select **OK** to submit your container deployment request.

![Settings summary for a new container instance in the Azure portal][aci-portal-05]

When deployment starts, a tile is placed on your portal dashboard indicating deployment progress. Once deployment completes, the tile is updated to show your new **mycontainer-myc1** container group.

![Creation progress of a new container instance in the Azure portal][aci-portal-08]

Select the **mycontainer-myc1** container group to display the container group properties. Take note of the **IP address** of the container group, as well as the **STATE** of your container.

![Container group overview in the Azure portal][aci-portal-06]

Once the container moves to the **Running** state, navigate to the IP address you noted in the previous step to display the application hosted in your new container.

![App deployed using Azure Container Instances viewed in browser][aci-portal-07]

## Delete the container
When you are done with the container, select the **mycontainer-myc1** container group and then click **Delete**.

![Deleting the container instance in the Azure portal][aci-portal-09]

This will launch a confirmation dialog box, select **Yes** when prompted.

![Delete confirmation of a container instance in the Azure portal][aci-portal-10]

<!-- IMAGES -->
[aci-portal-01]: ./media/container-instances-quickstart-portal/qs-portal-01.png
<!--[aci-portal-02]: ./media/container-instances-quickstart-portal/qs-portal-02.png-->
[aci-portal-03]: ./media/container-instances-quickstart-portal/qs-portal-03.png
[aci-portal-04]: ./media/container-instances-quickstart-portal/qs-portal-04.png
[aci-portal-05]: ./media/container-instances-quickstart-portal/qs-portal-05.png
[aci-portal-06]: ./media/container-instances-quickstart-portal/qs-portal-06.png
[aci-portal-07]: ./media/container-instances-quickstart-portal/qs-portal-07.png
[aci-portal-08]: ./media/container-instances-quickstart-portal/qs-portal-08.png
[aci-portal-09]: ./media/container-instances-quickstart-portal/qs-portal-09.png
[aci-portal-10]: ./media/container-instances-quickstart-portal/qs-portal-10.png

## Next steps

In this quickstart, you created an Azure Container Instance from an image in a public Docker Hub repository. If you'd like to try building a container yourself and deploy it to Azure Container Instances using the Azure Container Registry, continue to the Azure Container Instances tutorial.

> [!div class="nextstepaction"]
> [Azure Container Instances tutorials](./container-instances-tutorial-prepare-app.md)