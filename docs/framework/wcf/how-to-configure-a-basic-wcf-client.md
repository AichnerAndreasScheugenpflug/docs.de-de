---
title: 'Vorgehensweise: Konfigurieren einer grundlegenden Windows Communication Foundation-Clients'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 18acec48b2af78877f99335da38ccb0ae8942824
ms.sourcegitcommit: 0069cb3de8eed4e92b2195d29e5769a76111acdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2019
ms.locfileid: "56332317"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a><span data-ttu-id="523aa-102">Vorgehensweise: Konfigurieren einer grundlegenden Windows Communication Foundation-Clients</span><span class="sxs-lookup"><span data-stu-id="523aa-102">How to: Configure a Basic Windows Communication Foundation Client</span></span>

<span data-ttu-id="523aa-103">Dies ist die fünfte von sechs Aufgaben, die zum Erstellen einer grundlegenden Windows Communication Foundation (WCF)-Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="523aa-103">This is the fifth of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="523aa-104">Eine Übersicht über alle sechs Aufgaben finden Sie im Artikel [Getting Started Tutorial (Tutorial: Erste Schritte)](../../../docs/framework/wcf/getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="523aa-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="523aa-105">In diesem Thema wird erläutert, die Clientkonfigurationsdatei, die generiert wurde, mithilfe der **Hinzufügen eines Dienstverweises** Funktionalität von Visual Studio oder der [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span><span class="sxs-lookup"><span data-stu-id="523aa-105">This topic discusses the client configuration file that was generated using the **Add Service Reference** functionality of Visual Studio or the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="523aa-106">Für die Konfiguration des Clients muss der Endpunkt angegeben werden, den der Client verwendet, um auf den Dienst zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="523aa-106">Configuring the client consists of specifying the endpoint that the client uses to access the service.</span></span> <span data-ttu-id="523aa-107">Ein Endpunkt verfügt über eine Adresse, einer Bindung und einen Vertrag aus, und jede dieser muss beim Konfigurieren des Clients angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="523aa-107">An endpoint has an address, a binding, and a contract, and each of these must be specified in the process of configuring the client.</span></span>

## <a name="configure-a-windows-communication-foundation-client"></a><span data-ttu-id="523aa-108">Konfigurieren eines Windows Communication Foundation-Clients</span><span class="sxs-lookup"><span data-stu-id="523aa-108">Configure a Windows Communication Foundation client</span></span>

<span data-ttu-id="523aa-109">Öffnen Sie die generierte Konfigurationsdatei (App.config) aus dem GettingStartedClient-Projekt.</span><span class="sxs-lookup"><span data-stu-id="523aa-109">Open the generated configuration file (App.config) from the GettingStartedClient project.</span></span> <span data-ttu-id="523aa-110">Im folgenden Beispiel wird der Inhalt der generierten Konfiguration gezeigt.</span><span class="sxs-lookup"><span data-stu-id="523aa-110">The following example is a view of the generated configuration file.</span></span> <span data-ttu-id="523aa-111">Unter den [ \<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) Abschnitt, suchen Sie nach der [ \<Endpunkt >](../configure-apps/file-schema/wcf/endpoint-element.md) Element.</span><span class="sxs-lookup"><span data-stu-id="523aa-111">Under the [\<system.serviceModel>](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, find the [\<endpoint>](../configure-apps/file-schema/wcf/endpoint-element.md) element.</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

<span data-ttu-id="523aa-112">In diesem Beispiel wird den Endpunkt, den der Client verwendet, um den Zugriff auf den Dienst, der sich unter folgender Adresse befindet: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="523aa-112">This example configures the endpoint that the client uses to access the service that is located at the following address: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span></span>

<span data-ttu-id="523aa-113">Das Endpunktelement gibt an, dass für die Kommunikation zwischen dem WCF-Client und dem Dienst der `ServiceReference1.ICalculator`-Dienstvertrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="523aa-113">The endpoint element specifies that the `ServiceReference1.ICalculator` service contract is used for communication between the WCF client and service.</span></span> <span data-ttu-id="523aa-114">Der WCF-Kanal wird mit der vom System bereitgestellten <xref:System.ServiceModel.WSHttpBinding> konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="523aa-114">The WCF channel is configured with the system-provided <xref:System.ServiceModel.WSHttpBinding>.</span></span> <span data-ttu-id="523aa-115">Dieser Vertrag wurde mithilfe von generiert **Hinzufügen eines Dienstverweises** in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="523aa-115">This contract was generated by using **Add Service Reference** in Visual Studio.</span></span> <span data-ttu-id="523aa-116">Es handelt sich eigentlich um eine Kopie des Vertrags, der im GettingStartedLib-Projekt definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="523aa-116">It is essentially a copy of the contract that was defined in the GettingStartedLib project.</span></span> <span data-ttu-id="523aa-117">Die <xref:System.ServiceModel.WSHttpBinding>-Bindung gibt HTTP als Transport, interoperable Sicherheit und weitere Einzelheiten der Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="523aa-117">The <xref:System.ServiceModel.WSHttpBinding> binding specifies HTTP as the transport, interoperable security, and other configuration details.</span></span>

<span data-ttu-id="523aa-118">Weitere Informationen zur Verwendung des generierten Clients mit dieser Konfiguration finden Sie unter [Vorgehensweise: Verwenden Sie einen Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="523aa-118">For more information about how to use the generated client with this configuration, see [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="523aa-119">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="523aa-119">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="523aa-120">Vorgehensweise: Verwenden Sie einen WCF-client</span><span class="sxs-lookup"><span data-stu-id="523aa-120">How to: Use a WCF client</span></span>](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="523aa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="523aa-121">See also</span></span>

- [<span data-ttu-id="523aa-122">Verwenden von Bindungen, um Dienste und Clients zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="523aa-122">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="523aa-123">ServiceModel Metadata Utility-Tool (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="523aa-123">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="523aa-124">Vorgehensweise: Erstellen Sie einen Client</span><span class="sxs-lookup"><span data-stu-id="523aa-124">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="523aa-125">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="523aa-125">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="523aa-126">Selbst gehostete Dienste</span><span class="sxs-lookup"><span data-stu-id="523aa-126">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)