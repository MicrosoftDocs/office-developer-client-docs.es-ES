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
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820771"
---
# <a name="srowset"></a><span data-ttu-id="8e311-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="8e311-103">SRowSet</span></span>

  
  
<span data-ttu-id="8e311-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e311-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e311-105">Contiene una matriz de estructuras [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="8e311-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="8e311-106">Cada estructura **SRow** describe una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8e311-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e311-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8e311-107">Header file:</span></span>  <br/> |<span data-ttu-id="8e311-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e311-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8e311-109">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="8e311-109">Related macros:</span></span>  <br/> |<span data-ttu-id="8e311-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="8e311-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="8e311-111">Members</span><span class="sxs-lookup"><span data-stu-id="8e311-111">Members</span></span>

 <span data-ttu-id="8e311-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="8e311-112">**cRows**</span></span>
  
> <span data-ttu-id="8e311-113">Recuento de las estructuras de **SRow** en el miembro **aRow** .</span><span class="sxs-lookup"><span data-stu-id="8e311-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="8e311-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="8e311-114">**aRow**</span></span>
  
> <span data-ttu-id="8e311-115">Matriz de estructuras **SRow** .</span><span class="sxs-lookup"><span data-stu-id="8e311-115">Array of **SRow** structures.</span></span> <span data-ttu-id="8e311-116">Hay una estructura para cada fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8e311-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e311-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e311-117">Remarks</span></span>

<span data-ttu-id="8e311-118">Una estructura de **SRowSet** se usa para describir varias filas de datos de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8e311-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="8e311-119">Estructuras de **SRowSet** se usan en los métodos de interfaz [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)y [IMAPITable](imapitableiunknown.md) , además de las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e311-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="8e311-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="8e311-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="8e311-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="8e311-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="8e311-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="8e311-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="8e311-123">Se definen las estructuras de **SRowSet** igual que las estructuras [ADRLIST](adrlist.md) para permitir que las filas de una tabla de destinatarios y las entradas de una lista de direcciones tratan de la misma.</span><span class="sxs-lookup"><span data-stu-id="8e311-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="8e311-124">Estructuras de **SRowSet** y estructuras **ADRLIST** se pueden pasar a métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) y [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="8e311-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="8e311-125">Además, las reglas de asignación de memoria para las estructuras de **SRowSet** son los mismos que para las estructuras **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="8e311-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="8e311-126">En resumen, se debe asignar cada estructura [SPropValue](spropvalue.md) en la matriz apuntada por el miembro **lpProps** de cada fila de la fila establecer por separado mediante [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8e311-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="8e311-127">También se debe desasignar cada estructura de valor de propiedad mediante [MAPIFreeBuffer](mapifreebuffer.md) antes de la cancelación de asignación de su estructura de **SRowSet** para que no se pierden punteros a las estructuras **SPropValue** asignados.</span><span class="sxs-lookup"><span data-stu-id="8e311-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="8e311-128">Una fila del asigna memoria puede, a continuación, se conserva y volver a usar fuera del contexto de la estructura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="8e311-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="8e311-129">Para obtener más información acerca de cómo se debe asignar la memoria para las estructuras de **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="8e311-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e311-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e311-130">See also</span></span>



[<span data-ttu-id="8e311-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="8e311-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="8e311-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e311-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8e311-133">SRow</span><span class="sxs-lookup"><span data-stu-id="8e311-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8e311-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8e311-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8e311-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e311-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="8e311-136">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8e311-136">MAPI Structures</span></span>](mapi-structures.md)

