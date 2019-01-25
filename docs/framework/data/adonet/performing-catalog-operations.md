---
title: Ausführen von Katalogoperationen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e60f542f-6271-495b-a9e4-48553481c2a3
ms.openlocfilehash: 1b13d1e3e210964331a710512876bd1f8503069e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648075"
---
# <a name="performing-catalog-operations"></a><span data-ttu-id="b0f08-102">Ausführen von Katalogoperationen</span><span class="sxs-lookup"><span data-stu-id="b0f08-102">Performing Catalog Operations</span></span>
<span data-ttu-id="b0f08-103">Erstellen Sie zum Ausführen eines Befehls zum Ändern einer Datenbank oder der Katalog, z. B. der CREATE TABLE- oder CREATE PROCEDURE-Anweisung, eine **Befehl** -Objekt unter Verwendung der entsprechenden SQL-Anweisungen und ein **Verbindung** Objekt.</span><span class="sxs-lookup"><span data-stu-id="b0f08-103">To execute a command to modify a database or catalog, such as the CREATE TABLE or CREATE PROCEDURE statement, create a **Command** object using the appropriate SQL statements and a **Connection** object.</span></span> <span data-ttu-id="b0f08-104">Führen Sie den Befehl mit der **ExecuteNonQuery** Methode der **Befehl** Objekt.</span><span class="sxs-lookup"><span data-stu-id="b0f08-104">Execute the command with the **ExecuteNonQuery** method of the **Command** object.</span></span>  
  
 <span data-ttu-id="b0f08-105">Im folgenden Codebeispiel wird eine gespeicherte Prozedur in einer Microsoft SQL Server-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0f08-105">The following code example creates a stored procedure in a Microsoft SQL Server database.</span></span>  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim queryString As String = "CREATE PROCEDURE InsertCategory " & _  
    "@CategoryName nchar(15), " & _  
    "@Identity int OUT " & _  
    "AS " & _  
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " & _  
    "SET @Identity = @@Identity " & _  
    "RETURN @@ROWCOUNT"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
string queryString = "CREATE PROCEDURE InsertCategory  " +   
    "@CategoryName nchar(15), " +  
    "@Identity int OUT " +  
    "AS " +   
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " +   
    "SET @Identity = @@Identity " +  
    "RETURN @@ROWCOUNT";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
command.ExecuteNonQuery();  
```  
  
## <a name="see-also"></a><span data-ttu-id="b0f08-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0f08-106">See also</span></span>
- [<span data-ttu-id="b0f08-107">Verwenden von Befehlen zum Ändern von Daten</span><span class="sxs-lookup"><span data-stu-id="b0f08-107">Using Commands to Modify Data</span></span>](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)
- [<span data-ttu-id="b0f08-108">Befehle und Parameter</span><span class="sxs-lookup"><span data-stu-id="b0f08-108">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [<span data-ttu-id="b0f08-109">ADO.NET Managed Provider und DataSet Developer Center</span><span class="sxs-lookup"><span data-stu-id="b0f08-109">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
