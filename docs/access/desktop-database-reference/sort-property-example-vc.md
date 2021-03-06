---
title: Ejemplo de la propiedad Sort (VC++)
TOCTitle: Sort property example (VC++)
ms:assetid: 0f32b7ac-1902-1753-0c03-b38ba8c10c9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248862(v=office.15)
ms:contentKeyID: 48543259
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e23cf573d51e52c74f4bbf24801f4bd6f47ea22a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306926"
---
# <a name="sort-property-example-vc"></a>Ejemplo de la propiedad Sort (VC++)


**Se aplica a:** Access 2013, Office 2013

En este ejemplo se usa la propiedad [Sort](sort-property-ado.md) del objeto [Recordset](recordset-object-ado.md) para volver a ordenar las filas de un objeto **Recordset** derivado de la tabla ***Authors*** de la base de datos **Pubs**. Una rutina de la utilidad secundaria imprime cada fila.

```cpp 
 
// BeginSortCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void SortX(void); 
void SortXprint(_bstr_t title, _RecordsetPtr rstp); 
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
 
 SortX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SortX Function // 
// // 
////////////////////////////////////////////////////////// 
void SortX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _RecordsetPtr pRstAuthors = NULL; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 pRstAuthors->CursorLocation = adUseClient; 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 pRstAuthors->Open("SELECT * FROM authors", 
 _variant_t((IDispatch *) pConnection), 
 adOpenStatic, adLockReadOnly, adCmdText); 
 
 SortXprint(" Initial Order ", pRstAuthors); 
 
 //Clear the screen for the next display. 
 printf("\nPress any key to continue..."); 
 getch(); 
 system("cls"); 
 
 pRstAuthors->Sort = "au_lname ASC, au_fname ASC"; 
 SortXprint("Last Name Ascending", pRstAuthors); 
 
 //Clear the screen for the next display. 
 printf("\nPress any key to continue..."); 
 getch(); 
 system("cls"); 
 
 pRstAuthors->Sort = "au_lname DESC, au_fname ASC"; 
 SortXprint("Last Name Descending", pRstAuthors); 
 } 
 catch(_com_error &e) 
 { 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SortXprint Function // 
// // 
////////////////////////////////////////////////////////// 
//This is the secondary utility routine that prints 
//the given title, and the contents of the specified Recordset. 
void SortXprint(_bstr_t title, _RecordsetPtr rstp) 
{ 
 printf("---------------%s---------------\n", (LPCSTR)title); 
 printf("First Name Last Name\n" 
 "---------------------------------------------------\n"); 
 rstp->MoveFirst(); 
 int intLineCnt = 4; 
 while (!(rstp->EndOfFile)) 
 { 
 _bstr_t aufname; 
 _bstr_t aulname; 
 aufname = rstp->GetFields()->GetItem("au_fname")->Value; 
 aulname = rstp->GetFields()->GetItem("au_lname")->Value, 
 printf("%s %s\n",(LPCSTR) aufname, (LPCSTR) aulname); 
 rstp->MoveNext(); 
 intLineCnt++; 
 if (intLineCnt % 20 ==0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 } 
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
 
// EndSortCpp 
```

