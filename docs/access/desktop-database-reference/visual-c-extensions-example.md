---
title: Ejemplo de Extensiones de Visual C++
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f848e5adb9e8aca3a53732633b8b40cd75550cf9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484445"
---
# <a name="visual-c-extensions-example"></a><span data-ttu-id="faf30-102">Ejemplo de Extensiones de Visual C++</span><span class="sxs-lookup"><span data-stu-id="faf30-102">Visual C++ Extensions Example</span></span>


<span data-ttu-id="faf30-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="faf30-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="faf30-104">Este programa muestra cómo se recuperan los valores de los campos y se convierten en variables de C/C++.</span><span class="sxs-lookup"><span data-stu-id="faf30-104">This program shows how values are retrieved from fields and converted to C/C++ variables.</span></span>

<span data-ttu-id="faf30-105">En este ejemplo se también aprovecha las ventajas de los "punteros inteligentes", que controlan automáticamente los detalles específicos de COM de llamadas y el recuento de referencias para la interfaz **IADORecordBinding** .</span><span class="sxs-lookup"><span data-stu-id="faf30-105">This example also takes advantage of "smart pointers," which automatically handle the COM-specific details of calling and reference counting for the **IADORecordBinding** interface.</span></span>

<span data-ttu-id="faf30-106">Sin punteros inteligentes, el código será:</span><span class="sxs-lookup"><span data-stu-id="faf30-106">Without smart pointers, you would code:</span></span>

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

<span data-ttu-id="faf30-107">Con punteros inteligentes, se deriva el tipo de IADORecordBindingPtr el tipo de la interfaz IADORecordBinding con esta instrucción:</span><span class="sxs-lookup"><span data-stu-id="faf30-107">With smart pointers, you derive the IADORecordBindingPtr type from the type from the IADORecordBinding interface with this statement:</span></span>

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

<span data-ttu-id="faf30-108">Y se crea una instancia del puntero de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="faf30-108">And instantiate the pointer like this:</span></span>

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

<span data-ttu-id="faf30-109">Debido a que las extensiones de Visual C++ se implementa mediante el objeto **Recordset** , el constructor del puntero inteligente, picRs, toma el \_RecordsetPtr puntero, pRs.</span><span class="sxs-lookup"><span data-stu-id="faf30-109">Because the Visual C++ Extensions are implemented by the **Recordset** object, the constructor for the smart pointer, picRs , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="faf30-110">El constructor llama a QueryInterface mediante pRs para buscar la, lleve a cabo la \_RecordsetPtr puntero, pRs.</span><span class="sxs-lookup"><span data-stu-id="faf30-110">The constructor calls QueryInterface using pRs to find the , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="faf30-111">El constructor llama a QueryInterface mediante pRs para buscar la interfaz IADORecordBinding.</span><span class="sxs-lookup"><span data-stu-id="faf30-111">The constructor calls QueryInterface using pRs to find the IADORecordBinding interface.</span></span>

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

