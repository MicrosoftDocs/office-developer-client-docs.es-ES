---
title: Ejemplo de la propiedad Type (Field) (VC++)
TOCTitle: Type property example (Field) (VC++)
ms:assetid: d157407d-e7c9-897e-a0d1-e6396fb78690
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250045(v=office.15)
ms:contentKeyID: 48547858
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4646326469b4db688277885c31b5629aba8d408
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314096"
---
# <a name="type-property-example-field-vc"></a>Ejemplo de la propiedad Type (Field) (VC++)


**Se aplica a:** Access 2013, Office 2013

En este ejemplo se muestra la propiedad [Type](type-property-ado.md) al mostrar el nombre de la constante que corresponde al valor de la propiedad **Type** de todos los objetos [Field](field-object-ado.md) de la tabla ***Employees***. Para que este procedimiento se ejecute se necesita la función FieldType.

```cpp 
 
// BeginTypeFieldCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void TypeX(void); 
_bstr_t FieldType(int intType); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 TypeX(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////// 
// // 
// TypeX Function // 
// // 
/////////////////////////////////////////////// 
void TypeX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstEmployees = NULL; 
 FieldsPtr pFldLoop = NULL; 
 
 try 
 { 
 // Open recordset with data from Employee table. 
 TESTHR(pRstEmployees.CreateInstance(__uuidof(Recordset))); 
 pRstEmployees->Open ("employee",strCnn, 
 adOpenForwardOnly, adLockReadOnly, adCmdTable); 
 
 printf("Fields in Employee Table:\n\n"); 
 
 // Enumerate the Fields collection of the Employees table. 
 pFldLoop = pRstEmployees->GetFields(); 
 int intLine = 0; 
 for (int intFields = 0; intFields < (int)pFldLoop-> 
 GetCount(); intFields++) 
 { 
 _variant_t Index; 
 Index.vt = VT_I2; 
 Index.iVal = intFields; 
 printf(" Name: %s\n" , 
 (LPCSTR) pFldLoop->GetItem(Index)->GetName()); 
 printf(" Type: %s\n\n", 
 (LPCTSTR)FieldType(pFldLoop->GetItem(Index)->Type)); 
 intLine++; 
 if(intLine % 5 == 0) 
 { 
 printf("Press any key to continue..."); 
 getch(); 
 system("cls"); 
 } 
 } 
 } 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstEmployees->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 // Clean up objects before exit. 
 if (pRstEmployees) 
 if (pRstEmployees->State == adStateOpen) 
 pRstEmployees->Close(); 
} 
 
/////////////////////////////////////////////// 
// // 
// FieldType Function // 
// // 
/////////////////////////////////////////////// 
_bstr_t FieldType(int intType) 
{ 
 _bstr_t strType; 
 switch(intType) 
 { 
 case adChar: 
 strType = "adChar"; 
 break; 
 case adVarChar: 
 strType = "adVarChar"; 
 break; 
 case adSmallInt: 
 strType = "adSmallInt"; 
 break; 
 case adUnsignedTinyInt: 
 strType = "adUnsignedTinyInt"; 
 break; 
 case adDBTimeStamp: 
 strType = "adDBTimeStamp"; 
 break; 
 default: 
 break; 
 } 
 return strType; 
} 
 
/////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////// 
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
 
/////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////// 
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
// EndTypeFieldCpp 
```

