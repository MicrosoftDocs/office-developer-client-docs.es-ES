---
title: Interfaz ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281629"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="ecf45-102">Interfaz ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="ecf45-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="ecf45-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecf45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ecf45-104">La interfaz **ADORecordConstruction** se utiliza para construir un objeto **Record** de ADO a partir de un objeto **Row** de OLE DB en una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="ecf45-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="ecf45-105">Esta interfaz admite las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="ecf45-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="ecf45-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ecf45-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecf45-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="ecf45-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="ecf45-108">Solo escritura.</span><span class="sxs-lookup"><span data-stu-id="ecf45-108">Write-only.</span></span><br />
<span data-ttu-id="ecf45-109"> Establece el contenedor de un objeto <strong>Row</strong> de OLE DB en este objeto <strong>Record</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="ecf45-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecf45-110"><a href="row-property-ado.md">Fila</a></span><span class="sxs-lookup"><span data-stu-id="ecf45-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="ecf45-111">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ecf45-111">Read/Write.</span></span><br />
<span data-ttu-id="ecf45-112"> Obtiene y establece un objeto <strong>Row</strong> de OLE DB de/en este objeto <strong>Record</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="ecf45-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="ecf45-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ecf45-113">Methods</span></span>

<span data-ttu-id="ecf45-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ecf45-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="ecf45-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="ecf45-115">Events</span></span>

<span data-ttu-id="ecf45-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ecf45-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf45-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ecf45-117">Remarks</span></span>

<span data-ttu-id="ecf45-118">Dado un objeto **Row** de OLE DB (pRow), la construcción de un objeto **Record** de ADO (), la construcción de un objeto **Record** de ADO (adoR), equivale a las tres operaciones básicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ecf45-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="ecf45-119">Cree un objeto **Record** de ADO:</span><span class="sxs-lookup"><span data-stu-id="ecf45-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="ecf45-120">Consulte la interfaz **IADORecordConstruction** en el objeto **Record**:</span><span class="sxs-lookup"><span data-stu-id="ecf45-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="ecf45-121">Llame al método de propiedad **IADORecordConstruction::p ut \_ Row** para establecer el objeto **Row** de OLE DB en el objeto **Record** de ADO:</span><span class="sxs-lookup"><span data-stu-id="ecf45-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="ecf45-122">El objeto **adoR** resultante representa ahora el objeto **Record** de ADO construido a partir del objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ecf45-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="ecf45-123">Un objeto **Record** de ADO se puede crear también a partir del contenedor de un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ecf45-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf45-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecf45-124">Requirements</span></span>

<span data-ttu-id="ecf45-125">**Versión:** ADO 2.0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="ecf45-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="ecf45-126">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="ecf45-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="ecf45-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="ecf45-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

