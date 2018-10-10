---
title: Ejemplo de las propiedades IsolationLevel y Mode (VJ++)
TOCTitle: IsolationLevel and Mode Properties Example (VJ++)
ms:assetid: cb2e177c-c60c-b3ca-7de2-cbe2519d1e63
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249989(v=office.15)
ms:contentKeyID: 48547711
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b8ff091d17a8e46ad6439ef7964ab4a8ff87e00
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483523"
---
# <a name="isolationlevel-and-mode-properties-example-vj"></a><span data-ttu-id="92219-102">Ejemplo de las propiedades IsolationLevel y Mode (VJ++)</span><span class="sxs-lookup"><span data-stu-id="92219-102">IsolationLevel and Mode Properties Example (VJ++)</span></span>


<span data-ttu-id="92219-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92219-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92219-104">En este ejemplo se utiliza la propiedad [Mode](mode-property-ado.md) para abrir una conexión exclusiva y la propiedad [IsolationLevel](isolationlevel-property-ado.md) para abrir una transacción realizada de forma aislada con respecto a otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="92219-104">This example uses the [Mode](mode-property-ado.md) property to open an exclusive connection, and the [IsolationLevel](isolationlevel-property-ado.md) property to open a transaction that is conducted in isolation of other transactions.</span></span>

```java 
 
// BeginIsolationLevelJ 
import com.ms.wfc.data.*; 
import java.io.*; 
 
public class IsolationLevelX 
{ 
 // The main entry point for the application. 
 public static void main (String[] args) 
 { 
 IsolationLevelX(); 
 System.exit(0); 
 } 
 
 // IsolationLevelX Function 
 
 static void IsolationLevelX() 
 { 
 // Define ADO Objects 
 Connection cnn1 = null; 
 Recordset rstTitles = null; 
 
 // Assign connection string to variable 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 // Declarations 
 BufferedReader in = 
 new BufferedReader ( new InputStreamReader(System.in)); 
 String line = null; 
 
 try 
 { 
 // Open connection and Titles table 
 cnn1 = new Connection(); 
 
 cnn1.setMode(AdoEnums.ConnectMode.SHAREEXCLUSIVE); 
 cnn1.setIsolationLevel(AdoEnums.IsolationLevel.ISOLATED); 
 cnn1.open(strCnn); 
 
 rstTitles = new Recordset(); 
 rstTitles.setCursorType(AdoEnums.CursorType.DYNAMIC); 
 rstTitles.setLockType(AdoEnums.LockType.PESSIMISTIC); 
 rstTitles.open("Titles", cnn1, AdoEnums.CursorType.DYNAMIC, 
 AdoEnums.LockType.PESSIMISTIC); 
 
 cnn1.beginTrans(); 
 
 // Display the connection mode 
 if (cnn1.getMode() == AdoEnums.ConnectMode.SHAREEXCLUSIVE) 
 System.out.println("\n\tConnection mode is exclusive"); 
 else 
 System.out.println("\n\tConnection mode is not exclusive"); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Display the Isolation level 
 if ( cnn1.getIsolationLevel() == AdoEnums.IsolationLevel.ISOLATED) 
 System.out.println("\tTransaction is Isolated\n"); 
 else 
 System.out.println("\tTransaction is not Isolated\n"); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Change the type of psychology titles 
 while(!rstTitles.getEOF()) 
 { 
 
 if(rstTitles.getField("Type").getString().trim(). 
 equals(new String("psychology"))) 
 { 
 rstTitles.getField("Type").setString("self_help"); 
 rstTitles.update(); 
 } 
 rstTitles.moveNext(); 
 
 } 
 
 // Print current data in recordset 
 rstTitles.requery(); 
 while(!rstTitles.getEOF()) 
 { 
 System.out.println(rstTitles.getField("Title").getString() + 
 " - " + rstTitles.getField("Type").getString() ); 
 rstTitles.moveNext(); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Restore original data 
 cnn1.rollbackTrans(); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO 
 
 // As passing a connection, check for null pointer first 
 if(cnn1 !=null) 
 { 
 PrintProviderError(cnn1); 
 } 
 else 
 { 
 System.out.println("Exception:" + ae.getLocalizedMessage()); 
 } 
 } 
 
 // System Read requires this catch 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitles != null) 
 if (rstTitles.getState() == 1) 
 rstTitles.close(); 
 if (cnn1 != null) 
 if (cnn1.getState() == 1) 
 cnn1.close(); 
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
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndIsolationLevelJ 
```
