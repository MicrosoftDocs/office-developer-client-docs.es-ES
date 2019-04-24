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
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336522"
---
# <a name="srow"></a><span data-ttu-id="74537-103">SRow</span><span class="sxs-lookup"><span data-stu-id="74537-103">SRow</span></span>

<span data-ttu-id="74537-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74537-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74537-105">Describe una fila de una tabla que contiene las propiedades seleccionadas para un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="74537-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74537-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="74537-106">Header file:</span></span>  <br/> |<span data-ttu-id="74537-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="74537-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="74537-108">Members</span><span class="sxs-lookup"><span data-stu-id="74537-108">Members</span></span>

<span data-ttu-id="74537-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="74537-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="74537-110">Bytes de relleno para alinear correctamente los valores de propiedad a los que apunta el miembro **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="74537-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="74537-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="74537-111">**cValues**</span></span>
  
> <span data-ttu-id="74537-112">Número de valores de propiedad a los que apunta **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="74537-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="74537-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="74537-113">**lpProps**</span></span>
  
> <span data-ttu-id="74537-114">Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que describen los valores de propiedad de las columnas de la fila.</span><span class="sxs-lookup"><span data-stu-id="74537-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="74537-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74537-115">Remarks</span></span>

<span data-ttu-id="74537-116">Una estructura **SRow** describe una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="74537-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="74537-117">Se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) que acompaña a una notificación de tabla.</span><span class="sxs-lookup"><span data-stu-id="74537-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="74537-118">Las estructuras **SRow** se usan en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="74537-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="74537-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="74537-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="74537-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="74537-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="74537-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="74537-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="74537-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="74537-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="74537-123">[ITableData: IUnknown](itabledataiunknown.md) (muchos métodos)</span><span class="sxs-lookup"><span data-stu-id="74537-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="74537-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="74537-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="74537-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="74537-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="74537-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="74537-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="74537-127">Cuando se debe describir más de una fila, se usa una estructura [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="74537-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="74537-128">Una estructura **SRowSet** contiene una matriz de estructuras **SRow** y un recuento de estructuras en la matriz.</span><span class="sxs-lookup"><span data-stu-id="74537-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="74537-129">En la siguiente ilustración se muestra la relación entre una **SRow** y una estructura de datos de **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="74537-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="74537-130">**Relación entre SRow y SRowSet**</span><span class="sxs-lookup"><span data-stu-id="74537-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="74537-131">![Relación entre SRow y SRowSet] (media/amapi_17.gif "Relación entre SRow y SRowSet")</span><span class="sxs-lookup"><span data-stu-id="74537-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="74537-132">Las estructuras **SRow** se definen del mismo modo que las estructuras [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="74537-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="74537-133">Por lo tanto, una fila de una tabla de destinatarios y una entrada en una lista de direcciones se puede tratar del mismo modo.</span><span class="sxs-lookup"><span data-stu-id="74537-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="74537-134">Para obtener información sobre cómo se debe asignar la memoria para las estructuras de **SRow** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="74537-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74537-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="74537-135">See also</span></span>

- [<span data-ttu-id="74537-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="74537-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="74537-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="74537-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="74537-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="74537-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="74537-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74537-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="74537-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="74537-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="74537-141">Administración de la memoria para las estructuras ADRLIST y SRowSet</span><span class="sxs-lookup"><span data-stu-id="74537-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

