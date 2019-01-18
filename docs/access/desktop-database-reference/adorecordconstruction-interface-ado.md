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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712011"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="95592-102">Interfaz ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="95592-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="95592-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95592-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95592-104">La interfaz **ADORecordConstruction** se utiliza para construir un objeto **Record** de ADO a partir de un objeto **Row** de OLE DB en una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="95592-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="95592-105">Esta interfaz admite las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="95592-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="95592-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95592-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95592-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="95592-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="95592-108">Sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="95592-108">Write-only.</span></span><br />
<span data-ttu-id="95592-109">Establece el contenedor de un objeto <strong>Row</strong> de OLE DB en este objeto <strong>Record</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="95592-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95592-110"><a href="row-property-ado.md">Fila</a></span><span class="sxs-lookup"><span data-stu-id="95592-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="95592-111">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="95592-111">Read/Write.</span></span><br />
<span data-ttu-id="95592-112">Obtiene o establece un objeto <strong>Row</strong> de OLE DB desde o sobre este objeto <strong>Record</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="95592-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="95592-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="95592-113">Methods</span></span>

<span data-ttu-id="95592-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95592-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="95592-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="95592-115">Events</span></span>

<span data-ttu-id="95592-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95592-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="95592-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95592-117">Remarks</span></span>

<span data-ttu-id="95592-118">Dado un objeto **Row** de OLE DB (pRow), la construcción de un objeto **Record** de ADO (), la construcción de un objeto **Record** de ADO (adoR), la cantidad a las tres siguientes operaciones básicas:</span><span class="sxs-lookup"><span data-stu-id="95592-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="95592-119">Cree un objeto **Record** de ADO:</span><span class="sxs-lookup"><span data-stu-id="95592-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="95592-120">Consulte la interfaz **IADORecordConstruction** en el objeto **Record**:</span><span class="sxs-lookup"><span data-stu-id="95592-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="95592-121">Llamar a la **IADORecordConstruction::put\_fila** método de propiedad para establecer el objeto **Row** de OLE DB en el objeto **Record** de ADO:</span><span class="sxs-lookup"><span data-stu-id="95592-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="95592-122">El objeto **adoR** resultante representa ahora el objeto **Record** de ADO construido a partir del objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="95592-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="95592-123">Un objeto **Record** de ADO se puede crear también a partir del contenedor de un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="95592-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="95592-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95592-124">Requirements</span></span>

<span data-ttu-id="95592-125">**Versión:** ADO 2.0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="95592-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="95592-126">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="95592-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="95592-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="95592-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

