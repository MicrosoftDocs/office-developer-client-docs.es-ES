---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407259"
---
# <a name="srowset"></a><span data-ttu-id="ee36d-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ee36d-103">SRowSet</span></span>

  
  
<span data-ttu-id="ee36d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee36d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee36d-105">Contiene una matriz de [estructuras SRow.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="ee36d-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="ee36d-106">Cada **estructura de SRow** describe una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ee36d-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee36d-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ee36d-107">Header file:</span></span>  <br/> |<span data-ttu-id="ee36d-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee36d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ee36d-109">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="ee36d-109">Related macros:</span></span>  <br/> |<span data-ttu-id="ee36d-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="ee36d-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="ee36d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee36d-111">Members</span></span>

 <span data-ttu-id="ee36d-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="ee36d-112">**cRows**</span></span>
  
> <span data-ttu-id="ee36d-113">Recuento de **estructuras de SRow** en el **miembro aRow.**</span><span class="sxs-lookup"><span data-stu-id="ee36d-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="ee36d-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="ee36d-114">**aRow**</span></span>
  
> <span data-ttu-id="ee36d-115">Matriz de **estructuras SRow.**</span><span class="sxs-lookup"><span data-stu-id="ee36d-115">Array of **SRow** structures.</span></span> <span data-ttu-id="ee36d-116">Hay una estructura para cada fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ee36d-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee36d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee36d-117">Remarks</span></span>

<span data-ttu-id="ee36d-118">Una **estructura SRowSet** se usa para describir varias filas de datos de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ee36d-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="ee36d-119">**Las estructuras SRowSet** se usan en los métodos de interfaz [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e [IMAPITable,](imapitableiunknown.md) además de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="ee36d-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="ee36d-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="ee36d-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="ee36d-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="ee36d-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="ee36d-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="ee36d-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="ee36d-123">**Las estructuras SRowSet** se definen igual que las estructuras [ADRLIST](adrlist.md) para permitir que las filas de una tabla de destinatarios y las entradas de una lista de direcciones se traten igual.</span><span class="sxs-lookup"><span data-stu-id="ee36d-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="ee36d-124">Tanto **las estructuras SRowSet** como las estructuras **ADRLIST** se pueden pasar a métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="ee36d-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="ee36d-125">Además, las reglas para la asignación de memoria para **las estructuras SRowSet** son las mismas que para las **estructuras ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="ee36d-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="ee36d-126">En resumen, cada estructura [SPropValue](spropvalue.md) de la matriz a la que apunta el miembro **lpProps** de cada fila del conjunto de filas debe asignarse por separado mediante [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee36d-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="ee36d-127">También se debe desasignar cada estructura de valores de propiedad mediante [MAPIFreeBuffer](mapifreebuffer.md) antes de la desasignación de su estructura **SRowSet** para que no se pierdan los punteros a las estructuras **SPropValue** asignadas.</span><span class="sxs-lookup"><span data-stu-id="ee36d-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="ee36d-128">A continuación, se puede conservar y reutilizar la memoria asignada de una fila fuera del contexto de la **estructura SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="ee36d-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="ee36d-129">Para obtener más información acerca de cómo se debe asignar la memoria para las estructuras **SRowSet,** vea Managing [Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ee36d-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee36d-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee36d-130">See also</span></span>



[<span data-ttu-id="ee36d-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ee36d-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ee36d-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ee36d-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ee36d-133">SRow</span><span class="sxs-lookup"><span data-stu-id="ee36d-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="ee36d-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ee36d-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ee36d-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ee36d-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="ee36d-136">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ee36d-136">MAPI Structures</span></span>](mapi-structures.md)

