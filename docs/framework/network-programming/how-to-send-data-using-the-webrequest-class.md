---
title: 'Vorgehensweise: Senden von Daten mithilfe der WebRequest-Klasse'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WebRequest class, sending data to a host
- Sending data to a host, using WebRequest class
ms.assetid: 66686878-38ac-4aa6-bf42-ffb568ffc459
ms.openlocfilehash: dac372ce4f9da99b91b6f8d140d69ce9f1238f30
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54562897"
---
# <a name="how-to-send-data-using-the-webrequest-class"></a><span data-ttu-id="e94eb-102">Vorgehensweise: Senden von Daten mithilfe der WebRequest-Klasse</span><span class="sxs-lookup"><span data-stu-id="e94eb-102">How to: Send Data Using the WebRequest Class</span></span>
<span data-ttu-id="e94eb-103">In diesem Thema wird die Vorgehensweise zum Senden von Daten an einen Server beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e94eb-103">The following procedure describes the steps used to send data to a server.</span></span> <span data-ttu-id="e94eb-104">Die Prozedur wird häufig verwendet, um einer Webseite Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e94eb-104">This procedure is commonly used to post data to a Web page.</span></span>  
  
### <a name="to-send-data-to-a-host-server"></a><span data-ttu-id="e94eb-105">Senden von Daten an einen Hostserver</span><span class="sxs-lookup"><span data-stu-id="e94eb-105">To send data to a host server</span></span>  
  
1.  <span data-ttu-id="e94eb-106">Erstellen Sie eine <xref:System.Net.WebRequest>-Instanz, indem Sie <xref:System.Net.WebRequest.Create%2A> mit dem URI der Ressource aufrufen, die Daten akzeptiert, wie z.B. ein Skript oder eine ASP.NET-Seite.</span><span class="sxs-lookup"><span data-stu-id="e94eb-106">Create a <xref:System.Net.WebRequest> instance by calling <xref:System.Net.WebRequest.Create%2A> with the URI of the resource that accepts data, for example, a script or ASP.NET page.</span></span>  
  
    ```csharp  
    WebRequest request = WebRequest.Create("http://www.contoso.com/");  
    ```  
  
    ```vb  
    Dim request as WebRequest = WebRequest.Create("http://www.contoso.com/")  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="e94eb-107">.NET Framework stellt von **WebRequest** und **WebResponse** abgeleitete protokollspezifische Klassen für URIs bereit, die mit „http:“, „https:“, „ftp:“ und „file:“ beginnen.</span><span class="sxs-lookup"><span data-stu-id="e94eb-107">The .NET Framework provides protocol-specific classes derived from **WebRequest** and **WebResponse** for URIs that begin with "http:", "https:'', "ftp:", and "file:".</span></span> <span data-ttu-id="e94eb-108">Wenn Sie mit anderen Protokollen auf Ressourcen zugreifen möchten, müssen Sie protokollspezifische Klassen implementieren, die von **WebRequest** und **WebResponse** abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="e94eb-108">To access resources using other protocols, you must implement protocol-specific classes that derive from **WebRequest** and **WebResponse**.</span></span> <span data-ttu-id="e94eb-109">Weitere Informationen finden Sie unter [Programming Pluggable Protocols (Programmieren austauschbarer Protokolle)](../../../docs/framework/network-programming/programming-pluggable-protocols.md).</span><span class="sxs-lookup"><span data-stu-id="e94eb-109">For more information, see [Programming Pluggable Protocols](../../../docs/framework/network-programming/programming-pluggable-protocols.md) .</span></span>  
  
2.  <span data-ttu-id="e94eb-110">Legen Sie alle Eigenschaftswerte, die Sie brauchen, in **WebRequest** fest.</span><span class="sxs-lookup"><span data-stu-id="e94eb-110">Set any property values that you need in the **WebRequest**.</span></span> <span data-ttu-id="e94eb-111">Legen Sie z.B. zum Aktivieren der Authentifizierung die Eigenschaft **Anmeldeinformationen** auf eine Instanz der Klasse <xref:System.Net.NetworkCredential> fest.</span><span class="sxs-lookup"><span data-stu-id="e94eb-111">For example, to enable authentication, set the **Credentials** property to an instance of the <xref:System.Net.NetworkCredential> class.</span></span>  
  
    ```csharp  
    request.Credentials = CredentialCache.DefaultCredentials;  
    ```  
  
    ```vb  
    request.Credentials = CredentialCache.DefaultCredentials  
    ```  
  
     <span data-ttu-id="e94eb-112">In den meisten Fällen ist die **WebRequest**-Instanz selbst ausreichend, um Daten zu senden.</span><span class="sxs-lookup"><span data-stu-id="e94eb-112">In most cases, the **WebRequest** instance itself is sufficient to send data.</span></span> <span data-ttu-id="e94eb-113">Wenn Sie dennoch protokollspezifische Eigenschaften festlegen müssen, wandeln Sie **WebRequest** in einen protokollspezifischen Typ um.</span><span class="sxs-lookup"><span data-stu-id="e94eb-113">However, if you need to set protocol-specific properties, you must cast the **WebRequest** to the protocol-specific type.</span></span> <span data-ttu-id="e94eb-114">Wandeln Sie z.B. **WebRequest** in einen **HttpWebRequest**-Verweis um, wenn Sie auf die HTTP-spezifischen Eigenschaften von <xref:System.Net.HttpWebRequest> zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="e94eb-114">For example, to access the HTTP-specific properties of <xref:System.Net.HttpWebRequest>, cast the **WebRequest** to an **HttpWebRequest** reference.</span></span> <span data-ttu-id="e94eb-115">Das folgende Codebeispiel veranschaulicht, wie die HTTP-spezifische Eigenschaft <xref:System.Net.HttpWebRequest.UserAgent%2A> festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e94eb-115">The following code example shows how to set the HTTP-specific <xref:System.Net.HttpWebRequest.UserAgent%2A> property.</span></span>  
  
    ```csharp  
    ((HttpWebRequest)request).UserAgent = ".NET Framework Example Client";  
    ```  
  
    ```vb  
    Ctype(request,HttpWebRequest).UserAgent = ".NET Framework Example Client"  
    ```  
  
3.  <span data-ttu-id="e94eb-116">Geben Sie eine Protokollmethode an, die das Senden von Daten mit einer Anforderung ermöglicht, wie z.B. die HTTP-Methode **POST**.</span><span class="sxs-lookup"><span data-stu-id="e94eb-116">Specify a protocol method that permits data to be sent with a request, such as the HTTP **POST** method.</span></span>  
  
    ```csharp  
    request.Method = "POST";  
    ```  
  
    ```vb  
    request.Method = "POST"  
    ```  
  
4.  <span data-ttu-id="e94eb-117">Legen Sie die **ContentLength**-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e94eb-117">Set the **ContentLength** property.</span></span>  
  
    ```csharp  
    request.ContentLength = byteArray.Length;  
    ```  
  
    ```vb  
    request.ContentLength = byteArray.Length  
    ```  
  
5.  <span data-ttu-id="e94eb-118">Legen Sie die **ContentType**-Eigenschaft auf einen geeigneten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e94eb-118">Set the **ContentType** property to an appropriate value.</span></span>  
  
    ```csharp  
    request.ContentType = "application/x-www-form-urlencoded";  
    ```  
  
    ```vb  
    request.ContentType = "application/x-www-form-urlencoded"  
    ```  
  
6.  <span data-ttu-id="e94eb-119">Rufen Sie den Datenstrom ab, der die Anforderungsdaten enthält, indem Sie die Methode <xref:System.Net.WebRequest.GetRequestStream%2A> aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e94eb-119">Get the stream that holds request data by calling the <xref:System.Net.WebRequest.GetRequestStream%2A> method.</span></span>  
  
    ```csharp  
    Stream dataStream = request.GetRequestStream ();  
    ```  
  
    ```vb  
    Stream dataStream = request.GetRequestStream ()  
    ```  
  
7.  <span data-ttu-id="e94eb-120">Schreiben Sie die Daten in das von dieser Methode zurückgegebene <xref:System.IO.Stream>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e94eb-120">Write the data to the <xref:System.IO.Stream> object returned by this method.</span></span>  
  
    ```csharp  
    dataStream.Write (byteArray, 0, byteArray.Length);  
    ```  
  
    ```vb  
    dataStream.Write (byteArray, 0, byteArray.Length)  
    ```  
  
8.  <span data-ttu-id="e94eb-121">Schließen Sie den Anforderungsdatenstrom durch Aufrufen der **Stream.Close**-Methode.</span><span class="sxs-lookup"><span data-stu-id="e94eb-121">Close the request stream by calling the **Stream.Close** method.</span></span>  
  
    ```csharp  
    dataStream.Close ();  
    ```  
  
    ```vb  
    dataStream.Close ()  
    ```  
  
9. <span data-ttu-id="e94eb-122">Senden Sie die Anforderung an den Server durch Aufrufen von <xref:System.Net.WebRequest.GetResponse%2A>.</span><span class="sxs-lookup"><span data-stu-id="e94eb-122">Send the request to the server by calling <xref:System.Net.WebRequest.GetResponse%2A>.</span></span> <span data-ttu-id="e94eb-123">Diese Methode gibt ein Objekt zurück, das die Antwort des Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="e94eb-123">This method returns an object containing the server's response.</span></span> <span data-ttu-id="e94eb-124">Der Typ des zurückgegebenen <xref:System.Net.WebResponse>-Objekts wird durch das URI-Schema der Anforderung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e94eb-124">The returned <xref:System.Net.WebResponse> object's type is determined by the scheme of the request's URI.</span></span>  
  
    ```csharp  
    WebResponse response = request.GetResponse();  
    ```  
  
    ```vb  
    Dim response As WebResponse = request.GetResponse()  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="e94eb-125">Wenn Sie ein <xref:System.Net.WebResponse>-Objekt nicht mehr benötigen, schließen Sie es durch Aufrufen der <xref:System.Net.WebResponse.Close%2A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="e94eb-125">After you are finished with a <xref:System.Net.WebResponse> object, you must close it by calling the <xref:System.Net.WebResponse.Close%2A> method.</span></span> <span data-ttu-id="e94eb-126">Wenn Sie den Antwortstream vom Antwortobjekt abgerufen haben, können Sie den Datenstrom alternativ dazu auch durch Aufrufen der <xref:System.IO.Stream.Close%2A?displayProperty=nameWithType>-Methode schließen.</span><span class="sxs-lookup"><span data-stu-id="e94eb-126">Alternatively, if you have gotten the response stream from the response object, you can close the stream by calling the <xref:System.IO.Stream.Close%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="e94eb-127">Wird die Antwort oder der Datenstrom nicht geschlossen, verfügt die Anwendung möglicherweise nicht mehr über genügend Verbindungen mit dem Server und kann somit weitere Anforderungen nicht mehr verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e94eb-127">If you do not close the response or the stream, your application can run out of connections to the server and become unable to process additional requests.</span></span>  
  
10. <span data-ttu-id="e94eb-128">Sie können die protokollspezifischen Eigenschaften lesen, indem Sie auf die Eigenschaften von **WebResponse** zugreifen oder **WebResponse** in eine protokollspezifische Instanz umwandeln.</span><span class="sxs-lookup"><span data-stu-id="e94eb-128">You can access the properties of the **WebResponse** or cast the **WebResponse** to a protocol-specific instance to read protocol-specific properties.</span></span> <span data-ttu-id="e94eb-129">Sie können z.B. auf die HTTP-spezifischen Eigenschaften von <xref:System.Net.HttpWebResponse> zugreifen, indem Sie **WebRequest** in einen **HttpWebRequest**-Verweis umwandeln.</span><span class="sxs-lookup"><span data-stu-id="e94eb-129">For example, to access the HTTP-specific properties of <xref:System.Net.HttpWebResponse>, cast the **WebResponse** to an **HttpWebResponse** reference.</span></span>  
  
    ```csharp  
    Console.WriteLine (((HttpWebResponse)response).StatusDescription);  
    ```  
  
    ```vb  
    Console.WriteLine(CType(response, HttpWebResponse).StatusDescription)  
    ```  
  
11. <span data-ttu-id="e94eb-130">Zum Abrufen des Datenstroms, der die vom Server gesendeten Antwortdaten enthält, rufen Sie die Methode <xref:System.Net.WebResponse.GetResponseStream%2A> der **WebResponse** auf.</span><span class="sxs-lookup"><span data-stu-id="e94eb-130">To get the stream containing response data sent by the server, call the <xref:System.Net.WebResponse.GetResponseStream%2A> method of the **WebResponse**.</span></span>  
  
    ```csharp  
    Stream data = response.GetResponseStream;  
    ```  
  
    ```vb  
    Dim data As Stream = response.GetResponseStream  
    ```  
  
12. <span data-ttu-id="e94eb-131">Nachdem Sie die Daten der Antwort gelesen haben, schließen Sie entweder den Antwortstream mithilfe der **Stream.Close**-Methode, oder schließen Sie die Antwort mithilfe der **WebResponse.Close**-Methode.</span><span class="sxs-lookup"><span data-stu-id="e94eb-131">After reading the data from the response, you must either close the response stream using the **Stream.Close** method or close the response using the **WebResponse.Close** method.</span></span> <span data-ttu-id="e94eb-132">Es ist zwar nicht notwendig, die **Close**-Methode für sowohl Antwortdatenstrom als auch **WebResponse** aufzurufen, doch es ist auch nicht schädlich.</span><span class="sxs-lookup"><span data-stu-id="e94eb-132">It is not necessary to call the **Close** method on both the response stream and the **WebResponse**, but doing so is not harmful.</span></span>  
  
    ```csharp  
    response.Close();  
    ```  
  
    ```vb  
    response.Close()  
    ```  
  
## <a name="example"></a><span data-ttu-id="e94eb-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e94eb-133">Example</span></span>  
  
```csharp  
using System;  
using System.IO;  
using System.Net;  
using System.Text;  
  
namespace Examples.System.Net  
{  
    public class WebRequestPostExample  
    {  
        public static void Main ()  
        {  
            // Create a request using a URL that can receive a post.   
            WebRequest request = WebRequest.Create ("http://www.contoso.com/PostAccepter.aspx ");  
            // Set the Method property of the request to POST.  
            request.Method = "POST";  
            // Create POST data and convert it to a byte array.  
            string postData = "This is a test that posts this string to a Web server.";  
            byte[] byteArray = Encoding.UTF8.GetBytes (postData);  
            // Set the ContentType property of the WebRequest.  
            request.ContentType = "application/x-www-form-urlencoded";  
            // Set the ContentLength property of the WebRequest.  
            request.ContentLength = byteArray.Length;  
            // Get the request stream.  
            Stream dataStream = request.GetRequestStream ();  
            // Write the data to the request stream.  
            dataStream.Write (byteArray, 0, byteArray.Length);  
            // Close the Stream object.  
            dataStream.Close ();  
            // Get the response.  
            WebResponse response = request.GetResponse ();  
            // Display the status.  
            Console.WriteLine (((HttpWebResponse)response).StatusDescription);  
            // Get the stream containing content returned by the server.  
            dataStream = response.GetResponseStream ();  
            // Open the stream using a StreamReader for easy access.  
            StreamReader reader = new StreamReader (dataStream);  
            // Read the content.  
            string responseFromServer = reader.ReadToEnd ();  
            // Display the content.  
            Console.WriteLine (responseFromServer);  
            // Clean up the streams.  
            reader.Close ();  
            dataStream.Close ();  
            response.Close ();  
        }  
    }  
}  
```  
  
```vb  
Imports System  
Imports System.IO  
Imports System.Net  
Imports System.Text  
Namespace Examples.System.Net  
    Public Class WebRequestPostExample  
  
        Public Shared Sub Main()  
            ' Create a request using a URL that can receive a post.   
            Dim request As WebRequest = WebRequest.Create("http://www.contoso.com/PostAccepter.aspx ")  
            ' Set the Method property of the request to POST.  
            request.Method = "POST"  
            ' Create POST data and convert it to a byte array.  
            Dim postData As String = "This is a test that posts this string to a Web server."  
            Dim byteArray As Byte() = Encoding.UTF8.GetBytes(postData)  
            ' Set the ContentType property of the WebRequest.  
            request.ContentType = "application/x-www-form-urlencoded"  
            ' Set the ContentLength property of the WebRequest.  
            request.ContentLength = byteArray.Length  
            ' Get the request stream.  
            Dim dataStream As Stream = request.GetRequestStream()  
            ' Write the data to the request stream.  
            dataStream.Write(byteArray, 0, byteArray.Length)  
            ' Close the Stream object.  
            dataStream.Close()  
            ' Get the response.  
            Dim response As WebResponse = request.GetResponse()  
            ' Display the status.  
            Console.WriteLine(CType(response, HttpWebResponse).StatusDescription)  
            ' Get the stream containing content returned by the server.  
            dataStream = response.GetResponseStream()  
            ' Open the stream using a StreamReader for easy access.  
            Dim reader As New StreamReader(dataStream)  
            ' Read the content.  
            Dim responseFromServer As String = reader.ReadToEnd()  
            ' Display the content.  
            Console.WriteLine(responseFromServer)  
            ' Clean up the streams.  
            reader.Close()  
            dataStream.Close()  
            response.Close()  
        End Sub  
    End Class  
End Namespace  
```  
  
## <a name="see-also"></a><span data-ttu-id="e94eb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e94eb-134">See also</span></span>
- [<span data-ttu-id="e94eb-135">Erstellen von Internetanforderungen</span><span class="sxs-lookup"><span data-stu-id="e94eb-135">Creating Internet Requests</span></span>](../../../docs/framework/network-programming/creating-internet-requests.md)
- [<span data-ttu-id="e94eb-136">Verwenden von Datenströmen im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e94eb-136">Using Streams on the Network</span></span>](../../../docs/framework/network-programming/using-streams-on-the-network.md)
- [<span data-ttu-id="e94eb-137">Zugreifen auf das Internet über einen Proxy</span><span class="sxs-lookup"><span data-stu-id="e94eb-137">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
- [<span data-ttu-id="e94eb-138">Requesting Data (Anfordern von Daten)</span><span class="sxs-lookup"><span data-stu-id="e94eb-138">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
- [<span data-ttu-id="e94eb-139">Vorgehensweise: Anfordern von Daten mithilfe der WebRequest-Klasse</span><span class="sxs-lookup"><span data-stu-id="e94eb-139">How to: Request Data Using the WebRequest Class</span></span>](../../../docs/framework/network-programming/how-to-request-data-using-the-webrequest-class.md)
