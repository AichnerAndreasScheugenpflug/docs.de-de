---
title: Entschlüsseln von Daten
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [.NET Framework], decryption
- symmetric decryption
- asymmetric decryption
- decryption
ms.assetid: 9b266b6c-a9b2-4d20-afd8-b3a0d8fd48a0
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7f41a61fe929bb3eaf691deb75749777c0880aea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54530687"
---
# <a name="decrypting-data"></a><span data-ttu-id="6c9b7-102">Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="6c9b7-102">Decrypting Data</span></span>
<span data-ttu-id="6c9b7-103">Entschlüsselung ist die Umkehrung einer Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-103">Decryption is the reverse operation of encryption.</span></span> <span data-ttu-id="6c9b7-104">Bei einer Entschlüsselung mit geheimem Schlüssel müssen sowohl der Schlüssel als auch der Initialisierungsvektor (IV) bekannt sein, die zum Verschlüsseln der Daten verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-104">For secret-key encryption, you must know both the key and IV that were used to encrypt the data.</span></span> <span data-ttu-id="6c9b7-105">Bei einer Entschlüsselung mit öffentlichem Schlüssel muss entweder der öffentliche Schlüssel (wenn die Daten mit dem privaten Schlüssel verschlüsselt wurden) oder der private Schlüssel (wenn die Daten mit dem öffentlichen Schlüssel verschlüsselt wurden) bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-105">For public-key encryption, you must know either the public key (if the data was encrypted using the private key) or the private key (if the data was encrypted using the public key).</span></span>  
  
## <a name="symmetric-decryption"></a><span data-ttu-id="6c9b7-106">Symmetrische Entschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6c9b7-106">Symmetric Decryption</span></span>  
 <span data-ttu-id="6c9b7-107">Die Entschlüsselung von Daten, die mit einem symmetrischen Algorithmus verschlüsselt wurden, ist mit der Vorgehensweise zum Verschlüsseln der Daten mit einem symmetrischen Algorithmus vergelichbar.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-107">The decryption of data encrypted with symmetric algorithms is similar to the process used to encrypt data with symmetric algorithms.</span></span> <span data-ttu-id="6c9b7-108">Um Daten zu entschlüsseln, die aus einem beliebigen verwalteten Streamobjekt gelesen wurden, wird die <xref:System.Security.Cryptography.CryptoStream> -Klasse zusammen mit den von .NET Framework bereitgestellten symmetrischen Kryptografieklassen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-108">The <xref:System.Security.Cryptography.CryptoStream> class is used with symmetric cryptography classes provided by the .NET Framework to decrypt data read from any managed stream object.</span></span>  
  
 <span data-ttu-id="6c9b7-109">Im folgenden Beispiel wird veranschaulicht, wie eine neue Instanz der <xref:System.Security.Cryptography.RijndaelManaged> -Klasse erstellt und dann dazu verwendet wird, ein <xref:System.Security.Cryptography.CryptoStream> -Objekt zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-109">The following example illustrates how to create a new instance of the <xref:System.Security.Cryptography.RijndaelManaged> class and use it to perform decryption on a <xref:System.Security.Cryptography.CryptoStream> object.</span></span> <span data-ttu-id="6c9b7-110">In diesem Beispiel wird zunächst eine neue Instanz der **RijndaelManaged** -Klasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-110">This example first creates a new instance of the **RijndaelManaged** class.</span></span> <span data-ttu-id="6c9b7-111">Danach wird ein **CryptoStream** -Objekt erstellt und mit dem Wert eines verwalteten Streams namens `MyStream`initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-111">Next it creates a **CryptoStream** object and initializes it to the value of a managed stream called `MyStream`.</span></span> <span data-ttu-id="6c9b7-112">Anschließend werden der **CreateDecryptor** -Methode aus der **RijndaelManaged** -Klasse der Schlüssel und der IV übergeben, die für die Verschlüsselung verwendet wurden, und die Methode wird danach an den **CryptoStream** -Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-112">Next, the **CreateDecryptor** method from the **RijndaelManaged** class is passed the same key and IV that was used for encryption and is then passed to the **CryptoStream** constructor.</span></span> <span data-ttu-id="6c9b7-113">Zum Schluss wird die **CryptoStreamMode.Read** -Enumeration an den **CryptoStream** -Konstruktor übergeben, um Lesezugriff auf den Stream anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-113">Finally, the **CryptoStreamMode.Read** enumeration is passed to the **CryptoStream** constructor to specify read access to the stream.</span></span>  
  
```vb  
Dim RMCrypto As New RijndaelManaged()  
Dim CryptStream As New CryptoStream(MyStream, RMCrypto.CreateDecryptor(RMCrypto.Key, RMCrypto.IV), CryptoStreamMode.Read)  
```  
  
```csharp  
RijndaelManaged RMCrypto = new RijndaelManaged();  
CryptoStream CryptStream = new CryptoStream(MyStream, RMCrypto.CreateDecryptor(Key, IV), CryptoStreamMode.Read);  
```  
  
 <span data-ttu-id="6c9b7-114">Das folgende Beispiel veranschaulicht den gesamten Prozess: das Erzeugen des Streams, das Verschlüsseln des Streams, das Lesen aus dem Stream und das Schließen des Streams.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-114">The following example shows the entire process of creating a stream, decrypting the stream, reading from the stream, and closing the streams.</span></span> <span data-ttu-id="6c9b7-115">Es wird ein <xref:System.Net.Sockets.TcpListener> -Objekt erstellt, durch das ein Netzwerkstream initialisiert wird, wenn eine Verbindung zum lauschenden Objekt hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-115">A <xref:System.Net.Sockets.TcpListener> object is created that initializes a network stream when a connection to the listening object is made.</span></span> <span data-ttu-id="6c9b7-116">Der Netzwerkstream wird anschließend mit der **CryptoStream** -Klasse und der **RijndaelManaged** -Klasse entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-116">The network stream is then decrypted using the **CryptoStream** class and the **RijndaelManaged** class.</span></span> <span data-ttu-id="6c9b7-117">Für dieses Beispiel wird angenommen, dass die Wert des Schlüssels und der Wert des IVs entweder erfolgreich übertragen oder zuvor vereinbart wurden.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-117">This example assumes that the key and IV values have been either successfully transferred or previously agreed upon.</span></span> <span data-ttu-id="6c9b7-118">Das Beispiel enthält nicht den Code, der zum Verschlüsseln und Übertragen dieser Werte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-118">It does not show the code needed to encrypt and transfer these values.</span></span>  
  
```vb  
Imports System  
Imports System.Net.Sockets  
Imports System.Threading  
Imports System.IO  
Imports System.Net  
Imports System.Security.Cryptography  
  
Module Module1  
    Sub Main()  
            'The key and IV must be the same values that were used  
            'to encrypt the stream.    
            Dim Key As Byte() = {&H1, &H2, &H3, &H4, &H5, &H6, &H7, &H8, &H9, &H10, &H11, &H12, &H13, &H14, &H15, &H16}  
            Dim IV As Byte() = {&H1, &H2, &H3, &H4, &H5, &H6, &H7, &H8, &H9, &H10, &H11, &H12, &H13, &H14, &H15, &H16}  
        Try  
            'Initialize a TCPListener on port 11000  
            'using the current IP address.  
            Dim TCPListen As New TcpListener(IPAddress.Any, 11000)  
  
            'Start the listener.  
            TCPListen.Start()  
  
            'Check for a connection every five seconds.  
            While Not TCPListen.Pending()  
                Console.WriteLine("Still listening. Will try in 5 seconds.")  
  
                Thread.Sleep(5000)  
            End While  
  
            'Accept the client if one is found.  
            Dim TCP As TcpClient = TCPListen.AcceptTcpClient()  
  
            'Create a network stream from the connection.  
            Dim NetStream As NetworkStream = TCP.GetStream()  
  
            'Create a new instance of the RijndaelManaged class  
            'and decrypt the stream.  
            Dim RMCrypto As New RijndaelManaged()  
  
            'Create an instance of the CryptoStream class, pass it the NetworkStream, and decrypt   
            'it with the Rijndael class using the key and IV.  
            Dim CryptStream As New CryptoStream(NetStream, RMCrypto.CreateDecryptor(Key, IV), CryptoStreamMode.Read)  
  
            'Read the stream.  
            Dim SReader As New StreamReader(CryptStream)  
  
            'Display the message.  
            Console.WriteLine("The decrypted original message: {0}", SReader.ReadToEnd())  
  
            'Close the streams.  
            SReader.Close()  
            NetStream.Close()  
            TCP.Close()  
            'Catch any exceptions.   
        Catch  
            Console.WriteLine("The Listener Failed.")  
        End Try  
    End Sub  
End Module  
```  
  
```csharp  
using System;  
using System.Net.Sockets;  
using System.Threading;  
using System.IO;  
using System.Net;  
using System.Security.Cryptography;  
  
class Class1  
{  
   static void Main(string[] args)  
   {  
      //The key and IV must be the same values that were used  
      //to encrypt the stream.    
      byte[] Key = {0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08, 0x09, 0x10, 0x11, 0x12, 0x13, 0x14, 0x15, 0x16};  
      byte[] IV = {0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08, 0x09, 0x10, 0x11, 0x12, 0x13, 0x14, 0x15, 0x16};  
      try  
      {  
         //Initialize a TCPListener on port 11000  
         //using the current IP address.  
         TcpListener TCPListen = new TcpListener(IPAdress.Any, 11000);  
  
         //Start the listener.  
         TCPListen.Start();  
  
         //Check for a connection every five seconds.  
         while(!TCPListen.Pending())  
         {  
            Console.WriteLine("Still listening. Will try in 5 seconds.");  
            Thread.Sleep(5000);  
         }  
  
         //Accept the client if one is found.  
         TcpClient TCP = TCPListen.AcceptTcpClient();  
  
         //Create a network stream from the connection.  
         NetworkStream NetStream = TCP.GetStream();  
  
         //Create a new instance of the RijndaelManaged class  
         // and decrypt the stream.  
         RijndaelManaged RMCrypto = new RijndaelManaged();  
  
         //Create a CryptoStream, pass it the NetworkStream, and decrypt   
         //it with the Rijndael class using the key and IV.  
         CryptoStream CryptStream = new CryptoStream(NetStream,   
            RMCrypto.CreateDecryptor(Key, IV),   
            CryptoStreamMode.Read);  
  
         //Read the stream.  
         StreamReader SReader = new StreamReader(CryptStream);  
  
         //Display the message.  
         Console.WriteLine("The decrypted original message: {0}", SReader.ReadToEnd());  
  
         //Close the streams.  
         SReader.Close();  
         NetStream.Close();  
         TCP.Close();  
      }  
      //Catch any exceptions.   
      catch  
      {  
         Console.WriteLine("The Listener Failed.");  
      }  
   }  
}  
```  
  
 <span data-ttu-id="6c9b7-119">Damit das obige Beispiel funktioniert, muss eine verschlüsselte Verbindung zum Listener hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-119">For the previous sample to work, an encrypted connection must be made to the listener.</span></span> <span data-ttu-id="6c9b7-120">Für die Verbindung müssen derselbe Schlüssel, IV und Algorithmus wie im Listener verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-120">The connection must use the same key, IV, and algorithm used in the listener.</span></span> <span data-ttu-id="6c9b7-121">Wenn eine solche Verbindung hergestellt ist, wird die Nachricht entschlüsselt und in der Konsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-121">If such a connection is made, the message is decrypted and displayed to the console.</span></span>  
  
## <a name="asymmetric-decryption"></a><span data-ttu-id="6c9b7-122">Asymmetrische Entschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6c9b7-122">Asymmetric Decryption</span></span>  
 <span data-ttu-id="6c9b7-123">In der Regel generiert ein Teilnehmer (Teilnehmer A) sowohl einen öffentlichen als auch einen privaten Schlüssel und speichert diese entweder im Arbeitsspeicher oder in einem kryptografischen Schlüsselcontainer.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-123">Typically, a party (party A) generates both a public and private key and stores the key either in memory or in a cryptographic key container.</span></span>  <span data-ttu-id="6c9b7-124">Teilnehmer A sendet dann den öffentlichen Schlüssel an einen anderen Teilnehmer (Teilnehmer B).</span><span class="sxs-lookup"><span data-stu-id="6c9b7-124">Party A then sends the public key to another party (party B).</span></span>  <span data-ttu-id="6c9b7-125">Mit dem öffentlichen Schlüssel verschlüsselt Teilnehmer B Daten und sendet diese Daten an Teilnehmer A. Nachdem Teilnehmer A die Daten empfangen hat, entschlüsselt er diese mit dem entsprechenden privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-125">Using the public key, party B encrypts data and sends the data back to party A.  After receiving the data, party A decrypts it using the private key that corresponds.</span></span>  <span data-ttu-id="6c9b7-126">Die Entschlüsselung kann nur dann erfolgreich sein, wenn Teilnehmer A den privaten Schlüssel verwendet, der dem öffentlichen Schlüssel entspricht, den Teilnehmer B zum Verschlüsseln der Daten verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-126">Decryption will be successful only if party A uses the private key that corresponds to the public key Party B used to encrypt the data.</span></span>  
  
 <span data-ttu-id="6c9b7-127">Informationen zum Speichern ein asymmetrisches Schlüssels in sicheren Container für kryptografische Schlüssel und später diesen asymmetrischen Schlüssel abrufen finden Sie unter [Vorgehensweise: Asymmetrische Schlüssel in einem Schlüsselcontainer Store](../../../docs/standard/security/how-to-store-asymmetric-keys-in-a-key-container.md).</span><span class="sxs-lookup"><span data-stu-id="6c9b7-127">For information on how to store an asymmetric key in secure cryptographic key container and how to later retrieve the asymmetric key, see [How to: Store Asymmetric Keys in a Key Container](../../../docs/standard/security/how-to-store-asymmetric-keys-in-a-key-container.md).</span></span>  
  
 <span data-ttu-id="6c9b7-128">Das folgende Beispiel veranschaulicht die Entschlüsselung von zwei Bytearrays, die einen symmetrischen Schlüssel und einen IV darstellen.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-128">The following example illustrates the decryption of two arrays of bytes that represent a symmetric key and IV.</span></span>  <span data-ttu-id="6c9b7-129">Informationen dazu, wie der asymmetrische öffentliche Schlüssel aus dem <xref:System.Security.Cryptography.RSACryptoServiceProvider> -Objekt in ein Format extrahiert wird, das auf einfache Weise an andere Beteiligte gesendet werden kann, finden Sie unter [Encrypting Data](../../../docs/standard/security/encrypting-data.md)initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6c9b7-129">For information on how to extract the asymmetric public key from the <xref:System.Security.Cryptography.RSACryptoServiceProvider> object in a format that you can easily send to a third party, see [Encrypting Data](../../../docs/standard/security/encrypting-data.md).</span></span>  
  
```vb  
'Create a new instance of the RSACryptoServiceProvider class.  
Dim RSA As New RSACryptoServiceProvider()  
  
' Export the public key information and send it to a third party.  
' Wait for the third party to encrypt some data and send it back.  
  
'Decrypt the symmetric key and IV.  
SymmetricKey = RSA.Decrypt(EncryptedSymmetricKey, False)  
SymmetricIV = RSA.Decrypt(EncryptedSymmetricIV, False)  
```  
  
```csharp  
//Create a new instance of the RSACryptoServiceProvider class.  
RSACryptoServiceProvider RSA = new RSACryptoServiceProvider();  
  
// Export the public key information and send it to a third party.  
// Wait for the third party to encrypt some data and send it back.  
  
//Decrypt the symmetric key and IV.  
SymmetricKey = RSA.Decrypt( EncryptedSymmetricKey, false);  
SymmetricIV = RSA.Decrypt( EncryptedSymmetricIV , false);  
```  
  
## <a name="see-also"></a><span data-ttu-id="6c9b7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c9b7-130">See also</span></span>

- [<span data-ttu-id="6c9b7-131">Erzeugen von Schlüsseln für die Ver- und Entschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6c9b7-131">Generating Keys for Encryption and Decryption</span></span>](../../../docs/standard/security/generating-keys-for-encryption-and-decryption.md)
- [<span data-ttu-id="6c9b7-132">Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="6c9b7-132">Encrypting Data</span></span>](../../../docs/standard/security/encrypting-data.md)
- [<span data-ttu-id="6c9b7-133">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="6c9b7-133">Cryptographic Services</span></span>](../../../docs/standard/security/cryptographic-services.md)
