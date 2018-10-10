---
title: Ejemplo de la propiedad StayInSync (VC++)
TOCTitle: StayInSync Property Example (VC++)
ms:assetid: 42c389a8-e6d5-45f4-0442-1b2a2422dcbe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249197(v=office.15)
ms:contentKeyID: 48544485
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42203001135e65056ff5370637d4b5bea3f7a515
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484438"
---
# <a name="stayinsync-property-example-vc"></a><span data-ttu-id="b75dc-102">Ejemplo de la propiedad StayInSync (VC++)</span><span class="sxs-lookup"><span data-stu-id="b75dc-102">StayInSync Property Example (VC++)</span></span>


<span data-ttu-id="b75dc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b75dc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b75dc-104">En este ejemplo se muestra cómo facilita la propiedad [StayInSync](stayinsync-property-ado.md) el acceso a las filas de un objeto [Recordset](recordset-object-ado.md) jerárquico.</span><span class="sxs-lookup"><span data-stu-id="b75dc-104">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="b75dc-p101">El bucle externo muestra el nombre y apellido de cada autor, el país y la identificación. El objeto **Recordset** anexado de cada fila se recupera desde la colección [Fields](fields-collection-ado.md) y es asignado automáticamente a **rstTitleAuthor** por la propiedad **StayInSync** siempre que el objeto **Recordset** primario se mueve a una nueva fila. El bucle interno muestra cuatro campos de cada fila en el conjunto de registros anexado.</span><span class="sxs-lookup"><span data-stu-id="b75dc-p101">The outer loop displays each author's first and last name, state, and identification. The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row. The inner loop displays four fields from each row in the appended recordset.</span></span>

```cpp 
 
// BeginStayInSyncCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void StayInSyncX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 StayInSyncX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// StayInSyncX Function // 
// // 
////////////////////////////////////////////////////////// 
void StayInSyncX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='MSDataShape';" 
 "Data Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _RecordsetPtr pRst = NULL; 
 _RecordsetPtr pRstTitleAuthor = NULL; 
 
 try 
 { 
 TESTHR(pRstTitleAuthor.CreateInstance(__uuidof(Recordset))); 
 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRst.CreateInstance(__uuidof(Recordset))); 
 
 // Open connection. 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 pRst->PutStayInSync(true); 
 
 // Open recordset with names from Author & titleauthor table. 
 pRst->Open("SHAPE {select * from authors} " 
 "APPEND ({select * from titleauthor}" 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 _variant_t((IDispatch*)pConnection,true), 
 adOpenStatic, adLockReadOnly, adCmdText); 
 
 pRstTitleAuthor = pRst->GetFields()->GetItem("chapTitleAuthor")-> 
 Value; 
 int intLineCnt=0; 
 while(!(pRst->EndOfFile)) 
 { 
 printf("\n%s %s %s %s\n", (LPCSTR)(_bstr_t)pRst-> 
 Fields->GetItem("au_fname")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("au_lname")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("state")->Value, 
 (LPCSTR)(_bstr_t)pRst->Fields->GetItem("au_id")->Value); 
 intLineCnt++; 
 
 if (intLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 
 _variant_t vIndex; 
 while(!(pRstTitleAuthor->EndOfFile)) 
 { 
 vIndex = (short) 0; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 1; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 2; 
 printf("%s ",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 vIndex = (short) 3; 
 printf("%s\n",(LPCSTR)(_bstr_t)pRstTitleAuthor-> 
 Fields->Item[&vIndex]->Value); 
 intLineCnt++; 
 
 if (intLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 pRstTitleAuthor->MoveNext(); 
 } 
 pRst->MoveNext(); 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRst) 
 if (pRst->State == adStateOpen) 
 pRst->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
////////////////////////////////////////////////////////// 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
////////////////////////////////////////////////////////// 
void PrintComError(_com_error &e) 
{ 
 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print Com errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
 
} 
// EndStayInSyncCpp 
```

