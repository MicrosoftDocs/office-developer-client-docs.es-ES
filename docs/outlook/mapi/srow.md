---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820758"
---
# <a name="srow"></a><span data-ttu-id="44379-103">SRow</span><span class="sxs-lookup"><span data-stu-id="44379-103">SRow</span></span>

<span data-ttu-id="44379-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44379-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44379-105">Describe una fila de una tabla que contiene las propiedades seleccionadas de un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="44379-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44379-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="44379-106">Header file:</span></span>  <br/> |<span data-ttu-id="44379-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44379-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="44379-108">Members</span><span class="sxs-lookup"><span data-stu-id="44379-108">Members</span></span>

<span data-ttu-id="44379-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="44379-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="44379-110">Espaciado interno bytes para alinear correctamente los valores de propiedad que señala el miembro **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="44379-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="44379-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="44379-111">**cValues**</span></span>
  
> <span data-ttu-id="44379-112">Recuento de valores de propiedad que señala **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="44379-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="44379-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="44379-113">**lpProps**</span></span>
  
> <span data-ttu-id="44379-114">Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que describen los valores de propiedad para las columnas de la fila.</span><span class="sxs-lookup"><span data-stu-id="44379-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="44379-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44379-115">Remarks</span></span>

<span data-ttu-id="44379-116">Una estructura **SRow** describe una fila en una tabla.</span><span class="sxs-lookup"><span data-stu-id="44379-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="44379-117">Se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) que acompaña a una notificación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="44379-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="44379-118">Estructuras de **SRow** se usan en los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="44379-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="44379-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="44379-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="44379-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="44379-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="44379-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="44379-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="44379-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="44379-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="44379-123">[ITableData: IUnknown](itabledataiunknown.md) (muchos métodos de)</span><span class="sxs-lookup"><span data-stu-id="44379-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="44379-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="44379-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="44379-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="44379-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="44379-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="44379-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="44379-127">Cuando más de una fila necesita ser descrito, se usa una estructura de [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="44379-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="44379-128">Una estructura **SRowSet** contiene una matriz de estructuras **SRow** y un recuento de las estructuras de la matriz.</span><span class="sxs-lookup"><span data-stu-id="44379-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="44379-129">En la siguiente ilustración se muestra la relación entre un **SRow** y una estructura de datos **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="44379-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="44379-130">**Relación entre SRow y SRowSet**</span><span class="sxs-lookup"><span data-stu-id="44379-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="44379-131">![Relación entre SRow y SRowSet] (media/amapi_17.gif "Relación entre SRow y SRowSet")</span><span class="sxs-lookup"><span data-stu-id="44379-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="44379-132">Se definen las estructuras **SRow** el mismo como estructuras [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="44379-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="44379-133">Por lo tanto, puede ser una fila de una tabla de destinatarios y una entrada en una lista de direcciones tratan de la misma.</span><span class="sxs-lookup"><span data-stu-id="44379-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="44379-134">Para obtener información acerca de cómo se debe asignar la memoria para las estructuras de **SRow** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="44379-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44379-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="44379-135">See also</span></span>

- [<span data-ttu-id="44379-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="44379-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="44379-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="44379-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="44379-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="44379-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="44379-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="44379-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="44379-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="44379-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="44379-141">Administrar memoria para ADRLIST y estructuras SRowSet</span><span class="sxs-lookup"><span data-stu-id="44379-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)
