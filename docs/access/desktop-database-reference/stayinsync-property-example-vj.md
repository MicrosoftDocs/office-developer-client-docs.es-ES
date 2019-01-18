---
title: Ejemplo de la propiedad StayInSync (VJ++)
TOCTitle: StayInSync property example (VJ++)
ms:assetid: e9e0fcc7-07b6-c433-7c4c-478fc69eacaf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250184(v=office.15)
ms:contentKeyID: 48548448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0002f571a2022a7975271c40e9204864824bdb92
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716365"
---
# <a name="stayinsync-property-example-vj"></a><span data-ttu-id="ad674-102">Ejemplo de la propiedad StayInSync (VJ++)</span><span class="sxs-lookup"><span data-stu-id="ad674-102">StayInSync property example (VJ++)</span></span>


<span data-ttu-id="ad674-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad674-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad674-104">En este ejemplo se muestra cómo facilita la propiedad [StayInSync](stayinsync-property-ado.md) el acceso a las filas de un objeto [Recordset](recordset-object-ado.md) jerárquico.</span><span class="sxs-lookup"><span data-stu-id="ad674-104">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="ad674-p101">El bucle externo muestra el nombre y apellido de cada autor, el país y la identificación. El objeto **Recordset** anexado de cada fila se recupera desde la colección [Fields](fields-collection-ado.md) y es asignado automáticamente a **rstTitleAuthor** por la propiedad **StayInSync** siempre que el objeto **Recordset** primario se mueve a una nueva fila. El bucle interno muestra cuatro campos de cada fila en el conjunto de registros anexado.</span><span class="sxs-lookup"><span data-stu-id="ad674-p101">The outer loop displays each author's first and last name, state, and identification. The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row. The inner loop displays four fields from each row in the appended recordset.</span></span>

```java 
 
// BeginStayInSyncJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class StayInSyncX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 StayInSyncX(); 
 System.exit(0); 
 } 
 
 // StayInSyncX function 
 
 static void StayInSyncX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 Recordset rstTitleAuthor = null; 
 
 // Declarations. 
 BufferedReader in = new 
 BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider=MSDataShape;" + 
 "Data Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.setStayInSync(true); 
 rstAuthors.open("SHAPE {select * from Authors} " + 
 "APPEND ({select * from titleauthor}" + 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 Variant varRstTitleAuthor = rstAuthors.getFields(). 
 getItem("chapTitleAuthor").getValue(); 
 rstTitleAuthor =new Recordset(varRstTitleAuthor.toObject()); 
 int intCount =0; 
 while(!rstAuthors.getEOF()) 
 { 
 System.out.println("\n" + 
 rstAuthors.getField("au_fname").getString() + " " + 
 rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("state").getString() + " " + 
 rstAuthors.getField("au_id").getString()); 
 while(!rstTitleAuthor.getEOF()) 
 { 
 System.out.println(rstTitleAuthor.getField(0). 
 getString() + " " + 
 rstTitleAuthor.getField(1).getString() + " " + 
 rstTitleAuthor.getField(2).getString() + " " + 
 rstTitleAuthor.getField(3).getString()); 
 rstTitleAuthor.moveNext(); 
 } 
 if(++intCount % 5 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 rstAuthors.moveNext(); 
 } 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
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
 if (rstTitleAuthor != null) 
 if (rstTitleAuthor.getState() == 1) 
 rstTitleAuthor.close(); 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndStayInSyncJ 
```

