---
title: Ejemplo de colección Parameters, propiedad Comando (VC++)
TOCTitle: Parameters Collection, Command Property Example (VC++)
ms:assetid: 625a83d5-5b73-f945-7e01-bf412fed0827
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249369(v=office.15)
ms:contentKeyID: 48545237
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6fd25d09338e15086fc520c1d4b3a83b859d9a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483667"
---
# <a name="parameters-collection-command-property-example-vc"></a><span data-ttu-id="c1d2a-102">Ejemplo de colección Parameters, propiedad Comando (VC++)</span><span class="sxs-lookup"><span data-stu-id="c1d2a-102">Parameters Collection, Command Property Example (VC++)</span></span>


<span data-ttu-id="c1d2a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1d2a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c1d2a-104">El código siguiente muestra cómo utilizar la propiedad [Comando](command-property-adox.md) con el objeto [Command](command-object-ado.md) para recuperar información de parámetros para el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c1d2a-104">The following code demonstrates how to use the [Command](command-property-adox.md) property with the [Command](command-object-ado.md) object to retrieve parameter information for the procedure.</span></span>

```cpp 
 
// This sample runs correctly only if procedure 'CustomerById' 
// exists. If the procedure doesn't exist, please use 
// 'ADOXProceduresAppend.cpp' to creat it. 
 
// BeginProcedureParametersCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProcedureParametersX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProcedureParametersX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ProcedureParametersX Function // 
// // 
////////////////////////////////////////////////////////// 
void ProcedureParametersX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 
 //Define ADODB object pointers. 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_CommandPtr m_pCommand = NULL; 
 ADODB::_ParameterPtr m_pParameter = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 //Open the Connection 
 m_pCnn->Open("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';","","",NULL); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 //Open the catalog 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 //Get the command object 
 m_pCommand = m_pCatalog->Procedures->GetItem("CustomerById")-> 
 GetCommand(); 
 
 _variant_t vIndex; 
 
 //Retrieve Parameter information 
 m_pCommand->Parameters->Refresh(); 
 for (long lIndex = 0; lIndex < m_pCommand->Parameters->Count; 
 lIndex ++) 
 { 
 vIndex = lIndex; 
 m_pParameter = m_pCommand->Parameters->GetItem(vIndex); 
 cout << m_pParameter->Name << ":" << m_pParameter->Type << 
 "\n" << endl; 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 
 catch(...) 
 { 
 cout << "Error occured in ProcedureParametersX...."<< endl; 
 } 
} 
// EndProcedureParametersCpp 
```
