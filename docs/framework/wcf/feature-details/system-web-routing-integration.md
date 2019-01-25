---
title: System.Web.Routing-Integration
ms.date: 03/30/2017
ms.assetid: 31fe2a4f-5c47-4e5d-8ee1-84c524609d41
ms.openlocfilehash: 0ace776b8be64f42c05918bc234d39cd96bf8782
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688184"
---
# <a name="systemwebrouting-integration"></a><span data-ttu-id="64a5d-102">System.Web.Routing-Integration</span><span class="sxs-lookup"><span data-stu-id="64a5d-102">System.Web.Routing Integration</span></span>
<span data-ttu-id="64a5d-103">Beim Hosten eines Windows Communication Foundation (WCF)-Diensts in Internet Information Service (IIS) platzieren Sie eine SVC-Datei in das virtuelle Verzeichnis ein.</span><span class="sxs-lookup"><span data-stu-id="64a5d-103">When hosting a Windows Communication Foundation (WCF) service in Internet Information Service (IIS) you place a .svc file in the virtual directory.</span></span> <span data-ttu-id="64a5d-104">Diese SVC-Datei gibt die zu verwendende Diensthostfactory sowie die Klasse an, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="64a5d-104">This .svc file specifies the service host factory to use as well as the class that implements the service.</span></span> <span data-ttu-id="64a5d-105">Bei Anforderungen an den Dienst geben Sie die SVC-Datei im URI an, z. B.: `http://contoso.com/EmployeeServce.svc`.</span><span class="sxs-lookup"><span data-stu-id="64a5d-105">When making requests to the service you specify the .svc file in the URI, for example: `http://contoso.com/EmployeeServce.svc`.</span></span> <span data-ttu-id="64a5d-106">Für Programmierer, die REST-Dienste schreiben, ist dieser Typ von URI nicht optimal.</span><span class="sxs-lookup"><span data-stu-id="64a5d-106">For programmers writing REST services this type of URI is not optimal.</span></span> <span data-ttu-id="64a5d-107">URIs für REST-Dienste geben eine bestimmte Ressource an und verfügen normalerweise nicht über Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="64a5d-107">URIs for REST services specify a specific resource and normally do not have any extensions.</span></span> <span data-ttu-id="64a5d-108">Die <xref:System.Web.Routing> -Integrationsfunktion können Sie zum Hosten eines WCF REST-Diensts, der auf URIs ohne Erweiterung reagiert.</span><span class="sxs-lookup"><span data-stu-id="64a5d-108">The <xref:System.Web.Routing> integration feature allows you to host a WCF REST service that responds to URIs without an extension.</span></span> <span data-ttu-id="64a5d-109">Weitere Informationen zu routing finden Sie unter [ASP.NET-Routing](https://go.microsoft.com/fwlink/?LinkId=184660).</span><span class="sxs-lookup"><span data-stu-id="64a5d-109">For more information about routing see [ASP.NET Routing](https://go.microsoft.com/fwlink/?LinkId=184660).</span></span>  
  
## <a name="using-systemwebrouting-integration"></a><span data-ttu-id="64a5d-110">Verwenden der System.Web.Routing-Integration</span><span class="sxs-lookup"><span data-stu-id="64a5d-110">Using System.Web.Routing Integration</span></span>  
 <span data-ttu-id="64a5d-111">Für die <xref:System.Web.Routing>-Integrationsfunktion verwenden Sie die <xref:System.ServiceModel.Activation.ServiceRoute>-Klasse, um eine oder mehrere Routen zu erstellen und diese dem <xref:System.Web.Routing.RouteTable>-Objekt in einer Global.asax-Datei hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="64a5d-111">To use the <xref:System.Web.Routing> integration feature, you use the <xref:System.ServiceModel.Activation.ServiceRoute> class to create one or more routes and add them to the <xref:System.Web.Routing.RouteTable> in a Global.asax file.</span></span> <span data-ttu-id="64a5d-112">Diese Routen geben die relativen URIs an, auf die der Dienst reagiert.</span><span class="sxs-lookup"><span data-stu-id="64a5d-112">These routes specify the relative URIs that the service responds to.</span></span> <span data-ttu-id="64a5d-113">Das folgende Beispiel zeigt die dazu erforderliche Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="64a5d-113">The following example shows how to do this.</span></span>  
  
```  
<%@ Application Language="C#" %>  
<%@ Import Namespace="System.Web.Routing" %>  
<%@ Import Namespace="System.ServiceModel.Activation" %>  
<%@ Import Namespace="System.ServiceModel.Web " %>  
  
<script RunAt="server">  
    void Application_Start(object sender, EventArgs e)  
    {  
        RegisterRoutes(RouteTable.Routes);  
    }  
  
    private void RegisterRoutes(RouteCollection routes)  
    {  
        routes.Add(new ServiceRoute("Customers", new WebServiceHostFactory(), typeof(Service)));   
   }  
</script>  
```  
  
 <span data-ttu-id="64a5d-114">Hier werden alle Anforderungen mit einem relativen URI, die mit "Customers" beginnen, an den `Service`-Dienst weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="64a5d-114">This routes all requests with a relative URI that begins with Customers to the `Service` service.</span></span>  
  
 <span data-ttu-id="64a5d-115">In der Datei "Web.config" müssen Sie das `System.Web.Routing.UrlRoutingModule`-Modul hinzufügen, das `runAllManagedModulesForAllRequests`-Attribut auf `true` setzen und dem `UrlRoutingHandler`-Element den `<system.webServer>`-Handler hinzufügen. Dies wird im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="64a5d-115">In your Web.config file you must add the `System.Web.Routing.UrlRoutingModule` module, set the `runAllManagedModulesForAllRequests` attribute to `true`, and add the `UrlRoutingHandler` handler to the `<system.webServer>` element as shown in the following example.</span></span>  
  
```xml  
<system.webServer>  
      <modules runAllManagedModulesForAllRequests="true">  
        <add name="UrlRoutingModule" type="System.Web.Routing.UrlRoutingModule, System.Web, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a" />  
      </modules>  
      <handlers>  
        <add name="UrlRoutingHandler" preCondition="integratedMode" verb="*" path="UrlRouting.axd"/>  
      </handlers>  
    </system.webServer>  
```  
  
 <span data-ttu-id="64a5d-116">Es werden ein Modul und ein Handler geladen, die für das Routing erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="64a5d-116">This loads a module and handler required for routing.</span></span> <span data-ttu-id="64a5d-117">Weitere Informationen finden Sie unter [Routing](../../../../docs/framework/wcf/feature-details/routing.md).</span><span class="sxs-lookup"><span data-stu-id="64a5d-117">For more information, see [Routing](../../../../docs/framework/wcf/feature-details/routing.md).</span></span> <span data-ttu-id="64a5d-118">Außerdem müssen Sie das `aspNetCompatibilityEnabled`-Attribut wie im folgenden Beispiel gezeigt im `true`-Element auf `<serviceHostingEnvironment>` setzen.</span><span class="sxs-lookup"><span data-stu-id="64a5d-118">You must also set the `aspNetCompatibilityEnabled` attribute to `true` in the `<serviceHostingEnvironment>` element as shown in the following example.</span></span>  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="true"/>  
        <!-- ... -->  
    </system.serviceModel>  
```  
  
 <span data-ttu-id="64a5d-119">Die Klasse, die den Dienst implementiert, muss die ASP.NET-Kompatibilitätsanforderungen wie im folgenden Beispiel gezeigt aktivieren.</span><span class="sxs-lookup"><span data-stu-id="64a5d-119">The class that implements the service must enable ASP.NET compatibility requirements as shown in the following example.</span></span>  
  
```  
[ServiceContract]  
[AspNetCompatibilityRequirements(RequirementsMode=AspNetCompatibilityRequirementsMode.Allowed)]  
    public class Service  
    {  
        // ...  
    }  
```  
  
## <a name="see-also"></a><span data-ttu-id="64a5d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64a5d-120">See also</span></span>
- [<span data-ttu-id="64a5d-121">WCF-Web-HTTP-Programmiermodell</span><span class="sxs-lookup"><span data-stu-id="64a5d-121">WCF Web HTTP Programming Model</span></span>](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
- [<span data-ttu-id="64a5d-122">ASP.NET-Routing</span><span class="sxs-lookup"><span data-stu-id="64a5d-122">ASP.NET Routing</span></span>](https://go.microsoft.com/fwlink/?LinkId=184660)
