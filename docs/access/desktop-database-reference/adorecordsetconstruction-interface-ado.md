---
title: Interfaz ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701282"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="69cf1-102">Interfaz ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="69cf1-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="69cf1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69cf1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69cf1-104">La interfaz **ADORecordsetConstruction** se usa para construir un objeto **Recordset** de ADO a partir de un objeto **Rowset** de OLE DB en una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="69cf1-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="69cf1-105">Esta interfaz admite las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="69cf1-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="69cf1-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69cf1-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69cf1-107"><a href="chapter-property-ado.md">Capítulo</a></span><span class="sxs-lookup"><span data-stu-id="69cf1-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="69cf1-108">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="69cf1-108">Read/Write.</span></span><br />
<span data-ttu-id="69cf1-109">Obtiene o establece un objeto <strong>Chapter</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="69cf1-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cf1-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="69cf1-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="69cf1-111">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="69cf1-111">Read/Write.</span></span><br />
<span data-ttu-id="69cf1-112">Obtiene o establece un objeto <strong>RowPosition</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="69cf1-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cf1-113"><a href="rowset-property-ado.md">Conjunto de filas</a></span><span class="sxs-lookup"><span data-stu-id="69cf1-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="69cf1-114">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="69cf1-114">Read/Write.</span></span><br />
<span data-ttu-id="69cf1-115">Obtiene o establece un objeto <strong>Rowset</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</span><span class="sxs-lookup"><span data-stu-id="69cf1-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="69cf1-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="69cf1-116">Methods</span></span>

<span data-ttu-id="69cf1-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="69cf1-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="69cf1-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="69cf1-118">Events</span></span>

<span data-ttu-id="69cf1-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="69cf1-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="69cf1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69cf1-120">Remarks</span></span>

<span data-ttu-id="69cf1-121">Dado un objeto **Rowset** de OLE DB (pRowset), la construcción de un objeto **Recordset** de ADO (), la construcción de un importe de (adoRs) del objeto **Recordset** de ADO a las tres siguientes operaciones básicas:</span><span class="sxs-lookup"><span data-stu-id="69cf1-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="69cf1-122">Cree un objeto **Recordset** de ADO:</span><span class="sxs-lookup"><span data-stu-id="69cf1-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="69cf1-123">Consulte la interfaz **IADORecordsetConstruction** en el objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="69cf1-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="69cf1-124">Llamar a la IADORecordsetConstruction::put\_método de propiedad de conjunto de filas para establecer el objeto Rowset de OLE DB en el objeto Recordset de ADO:</span><span class="sxs-lookup"><span data-stu-id="69cf1-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="69cf1-125">El objeto resultante representa ahora el objeto **Recordset** de ADO construido a partir del objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="69cf1-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="69cf1-126">También se puede crear un objeto **Recordset** de ADO a partir de un objeto **Chapter** o **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="69cf1-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cf1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69cf1-127">Requirements</span></span>

- <span data-ttu-id="69cf1-128">**Versión:** ADO 2.0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="69cf1-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="69cf1-129">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="69cf1-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="69cf1-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="69cf1-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

