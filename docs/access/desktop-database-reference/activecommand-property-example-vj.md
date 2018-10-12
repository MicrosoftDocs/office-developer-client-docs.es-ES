---
title: Ejemplo de la Propiedad ActiveCommand (VJ++)
TOCTitle: ActiveCommand Property Example (VJ++)
ms:assetid: e7ec73de-1097-ea57-9bdd-27c56263c943
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250176(v=office.15)
ms:contentKeyID: 48548415
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 556bf57b1f6ebb27bf1119d0b4962d16aa38c2c6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486447"
---
# <a name="activecommand-property-example-vj"></a><span data-ttu-id="fabd1-102">Ejemplo de la Propiedad ActiveCommand (VJ++)</span><span class="sxs-lookup"><span data-stu-id="fabd1-102">ActiveCommand Property Example (VJ++)</span></span>


<span data-ttu-id="fabd1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fabd1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fabd1-104">En este ejemplo se muestra la propiedad [ActiveCommand](activecommand-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fabd1-104">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property.</span></span>

<span data-ttu-id="fabd1-105">A una subrutina se le asigna un objeto [Recordset](recordset-object-ado.md) cuya propiedad **ActiveCommand** se utiliza para mostrar el texto y los parámetros del comando que ha creado el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fabd1-105">A subroutine is given a [Recordset](recordset-object-ado.md) object whose **ActiveCommand** property is used to display the command text and parameter that created the **Recordset**.</span></span>

```java 
 
// BeginActiveCommandJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class ActiveCommandX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 ActiveCommandX(); 
 System.exit(0); 
 } 
 
 // ActiveCommandX function 
 
 static void ActiveCommandX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Command cmd = null; 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 String strName; 
 
 try 
 { 
 System.out.println("Enter an author's name (e.g., Ringer): "); 
 strName = in.readLine().trim(); 
 cmd = new Command(); 
 cmd.setCommandText("SELECT * FROM authors WHERE au_lname = ?"); 
 cmd.getParameters().append(cmd.createParameter("LastName", 
 AdoEnums.DataType.CHAR, 
 AdoEnums.ParameterDirection.INPUT, 20, strName)); 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 cmd.setActiveConnection(cnConn1); 
 rstAuthors = cmd.execute(null,AdoEnums.CommandType.TEXT); 
 ActiveCommandXprint(rstAuthors); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 // Cleanup objects before exit. 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 } 
 
 // ActiveCommandXprint function 
 static void ActiveCommandXprint(Recordset rstp) 
 { 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strName; 
 
 try 
 { 
 strName = rstp.getActiveCommand().getParameters(). 
 getItem("LastName").getValue().toString(); 
 System.out.println("\nCommand text = '" + 
 rstp.getActiveCommand().getCommandText() + "'"); 
 System.out.println("Parameter = '" + strName + "'"); 
 if(rstp.getBOF()) 
 { 
 System.out.println("Name = '" + strName + "', not found."); 
 } 
 else 
 { 
 System.out.println("Name = '" + 
 rstp.getField("au_fname").getString() + " " + 
 rstp.getField("au_lname").getString() + 
 "', author ID = '" + 
 rstp.getField("au_id").getString() + "'"); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstp != null) 
 { 
 PrintProviderError(rstp.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 //.PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndActiveCommandJ 
```
