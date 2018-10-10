---
title: Ejemplo de los métodos Save y Open (VJ++)
TOCTitle: Save and Open Methods Example (VJ++)
ms:assetid: 15ad340a-2d32-3656-25d1-5c3927b9fed2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248920(v=office.15)
ms:contentKeyID: 48543414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69d2ea8f40946ea3edcacf52c97a7464d47cd653
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483364"
---
# <a name="save-and-open-methods-example-vj"></a><span data-ttu-id="f7cb7-102">Ejemplo de los métodos Save y Open (VJ++)</span><span class="sxs-lookup"><span data-stu-id="f7cb7-102">Save and Open Methods Example (VJ++)</span></span>


<span data-ttu-id="f7cb7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7cb7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7cb7-104">En estos tres ejemplos se muestra cómo se pueden utilizar conjuntamente los métodos [Save](save-method-ado.md) y **Open**.</span><span class="sxs-lookup"><span data-stu-id="f7cb7-104">These three examples demonstrate how the [Save](save-method-ado.md) and **Open** methods can be used together.</span></span>

<span data-ttu-id="f7cb7-p101">Supongamos que se va de viaje de negocios y que desea llevarse una tabla de una base de datos. Antes de marcharse, obtiene acceso a los datos como un [conjunto de registros](recordset-object-ado.md) y lo guarda en un formato transportable. Cuando llega a su destino, obtiene acceso al **conjunto de registros** como un **conjunto de registros** local desconectado. Realiza cambios en el **conjunto de registros** y, a continuación, lo vuelve a guardar con los cambios. Finalmente, al volver a casa, se conecta de nuevo a la base de datos y la actualiza con los cambios realizados mientras estaba de viaje.</span><span class="sxs-lookup"><span data-stu-id="f7cb7-p101">Assume you are going on a business trip and want to take along a table from a database. Before you go, you access the data as a [Recordset](recordset-object-ado.md) and save it in a transportable form. When you arrive at your destination, you access the **Recordset** as a local, disconnected **Recordset**. You make changes to the **Recordset**, then save it again, along with your changes. Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</span></span>

```java 
 
// BeginSaveJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class SaveX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 SaveX1(); 
 SaveX2(); 
 SaveX3(); 
 System.exit(0); 
 } 
 
 // First, access and save the Authors table. 
 
 // SaveX1 function 
 
 static void SaveX1() 
 { 
 // Define ADO Objects. 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 File file; 
 
 try 
 { 
 rstAuthors = new Recordset(); 
 rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 rstAuthors.open("SELECT * FROM Authors", 
 strCnn, 
 AdoEnums.CursorType.DYNAMIC, 
 AdoEnums.LockType.OPTIMISTIC, 
 AdoEnums.CommandType.TEXT); 
 
 // For the sake of illustration, save the recordset to a 
 //diskette in XML format. 
 file = new File("c:\\Pubs.xml"); 
 if(!file.exists()) 
 rstAuthors.save("c:\\Pubs.xml",AdoEnums.PersistFormat.XML); 
 else 
 { 
 System.out.println("\nFile already exists."); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 System.exit(0); 
 } 
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
 } 
 } 
 
 // At this point, you have arrived at your destination. You will 
 // access the Authors table as a local, disconnected Recordset. 
 // Don't forget you must have the MSPersist provider on the machine 
 // you are using in order to access the saved file, a:\Pubs.xml. 
 
 // SaveX2 function 
 
 static void SaveX2() 
 { 
 // Define ADO Objects. 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 
 try 
 { 
 rstAuthors = new Recordset(); 
 
 // For sake of illustration, we specify all parameters. 
 rstAuthors.open("c:\\Pubs.xml", 
 "Provider=MSPersist;", 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.FILE); 
 
 // Now you have a local, disconnected recordset. 
 // Edit it as you desire. 
 // (In this example, the change makes no difference). 
 rstAuthors.find("au_lname = 'Carson'"); 
 if(rstAuthors.getEOF()) 
 { 
 System.out.println("Name not found."); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 return; 
 } 
 rstAuthors.getField("city").setString("Berkeley"); 
 rstAuthors.update(); 
 
 // Save changes in ADTG format this time, for illustration. 
 // Note that previous version on the diskette, as a:\Pubs.xml. 
 rstAuthors.save("c:\\Pubs.adtg",AdoEnums.PersistFormat.ADTG); 
 
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
 } 
 } 
 
 // Finally, update the database with your changes. 
 
 // SaveX3 function 
 
 static void SaveX3() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 // If there is no ActiveConnection, you can open with defaults. 
 rstAuthors = new Recordset(); 
 rstAuthors.open("c:\\Pubs.adtg"); 
 
 // Connect to the database, associate the Recordset with 
 // connection, then update the database table with the changed 
 // Recordset. 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors.setActiveConnection(cnConn1); 
 rstAuthors.updateBatch(); 
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
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
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
// EndSaveJ 
```
