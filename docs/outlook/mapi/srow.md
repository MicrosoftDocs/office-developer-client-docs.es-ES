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
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579126"
---
# <a name="srow"></a><span data-ttu-id="aa104-103">SRow</span><span class="sxs-lookup"><span data-stu-id="aa104-103">SRow</span></span>

<span data-ttu-id="aa104-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa104-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa104-105">Describe una fila de una tabla que contiene las propiedades seleccionadas de un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="aa104-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa104-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="aa104-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa104-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa104-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="aa104-108">Members</span><span class="sxs-lookup"><span data-stu-id="aa104-108">Members</span></span>

<span data-ttu-id="aa104-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="aa104-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="aa104-110">Espaciado interno bytes para alinear correctamente los valores de propiedad que señala el miembro **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="aa104-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="aa104-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="aa104-111">**cValues**</span></span>
  
> <span data-ttu-id="aa104-112">Recuento de valores de propiedad que señala **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="aa104-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="aa104-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="aa104-113">**lpProps**</span></span>
  
> <span data-ttu-id="aa104-114">Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que describen los valores de propiedad para las columnas de la fila.</span><span class="sxs-lookup"><span data-stu-id="aa104-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa104-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa104-115">Remarks</span></span>

<span data-ttu-id="aa104-116">Una estructura **SRow** describe una fila en una tabla.</span><span class="sxs-lookup"><span data-stu-id="aa104-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="aa104-117">Se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) que acompaña a una notificación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="aa104-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="aa104-118">Estructuras de **SRow** se usan en los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="aa104-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="aa104-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="aa104-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="aa104-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="aa104-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="aa104-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="aa104-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="aa104-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="aa104-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="aa104-123">[ITableData: IUnknown](itabledataiunknown.md) (muchos métodos de)</span><span class="sxs-lookup"><span data-stu-id="aa104-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="aa104-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="aa104-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="aa104-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="aa104-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="aa104-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="aa104-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="aa104-127">Cuando más de una fila necesita ser descrito, se usa una estructura de [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="aa104-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="aa104-128">Una estructura **SRowSet** contiene una matriz de estructuras **SRow** y un recuento de las estructuras de la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa104-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="aa104-129">En la siguiente ilustración se muestra la relación entre un **SRow** y una estructura de datos **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="aa104-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="aa104-130">**Relación entre SRow y SRowSet**</span><span class="sxs-lookup"><span data-stu-id="aa104-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="aa104-131">![Relación entre SRow y SRowSet] (media/amapi_17.gif "Relación entre SRow y SRowSet")</span><span class="sxs-lookup"><span data-stu-id="aa104-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="aa104-132">Se definen las estructuras **SRow** el mismo como estructuras [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="aa104-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="aa104-133">Por lo tanto, puede ser una fila de una tabla de destinatarios y una entrada en una lista de direcciones tratan de la misma.</span><span class="sxs-lookup"><span data-stu-id="aa104-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="aa104-134">Para obtener información acerca de cómo se debe asignar la memoria para las estructuras de **SRow** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="aa104-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa104-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="aa104-135">See also</span></span>

- [<span data-ttu-id="aa104-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="aa104-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="aa104-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="aa104-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="aa104-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="aa104-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="aa104-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="aa104-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="aa104-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="aa104-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="aa104-141">Administrar memoria para ADRLIST y estructuras SRowSet</span><span class="sxs-lookup"><span data-stu-id="aa104-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

