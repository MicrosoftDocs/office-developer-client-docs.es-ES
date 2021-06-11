---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415918"
---
# <a name="adrlist"></a><span data-ttu-id="e8838-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e8838-103">ADRLIST</span></span>

<span data-ttu-id="e8838-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8838-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8838-105">Describe cero o más propiedades que pertenecen a uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e8838-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8838-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e8838-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8838-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8838-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e8838-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="e8838-108">Related macros:</span></span>  <br/> |<span data-ttu-id="e8838-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="e8838-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="e8838-110">Members</span><span class="sxs-lookup"><span data-stu-id="e8838-110">Members</span></span>

<span data-ttu-id="e8838-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="e8838-111">**cEntries**</span></span>
  
> <span data-ttu-id="e8838-112">Recuento de entradas en la matriz especificada por el **miembro aEntries.**</span><span class="sxs-lookup"><span data-stu-id="e8838-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="e8838-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="e8838-113">**aEntries**</span></span>
  
> <span data-ttu-id="e8838-114">Matriz de [estructuras ADRENTRY,](adrentry.md) una estructura para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="e8838-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8838-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8838-115">Remarks</span></span>

<span data-ttu-id="e8838-116">Una **estructura ADRLIST** contiene una o más estructuras **ADRENTRY,** cada una de las que describe las propiedades de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="e8838-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="e8838-117">Un destinatario puede no resolverse.</span><span class="sxs-lookup"><span data-stu-id="e8838-117">A recipient can be unresolved.</span></span> <span data-ttu-id="e8838-118">Esto significa que carece de un identificador de entrada en su matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e8838-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="e8838-119">Un destinatario resuelto significa que se incluye la propiedad **\_ PR ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8838-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="e8838-120">Normalmente, los destinatarios resueltos también tienen una dirección de correo **electrónico PR_EMAIL_ADDRESS** propiedad ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8838-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="e8838-121">Sin embargo, la dirección de correo electrónico no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="e8838-121">However, the email address is not required.</span></span> <span data-ttu-id="e8838-122">**Las estructuras ADRLIST** se usan, por ejemplo, para describir la lista de destinatarios de un mensaje saliente y mapi para mostrar las entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e8838-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="e8838-123">**Las estructuras ADRLIST** se asemejan a [las estructuras SRowSet](srowset.md) que se usan para representar filas en tablas.</span><span class="sxs-lookup"><span data-stu-id="e8838-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="e8838-124">De hecho, estas dos estructuras están diseñadas para que se puedan usar indistintamente.</span><span class="sxs-lookup"><span data-stu-id="e8838-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="e8838-125">Ambos contienen una matriz de estructuras que describen un grupo de propiedades y un recuento de los valores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e8838-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="e8838-126">Mientras que en la **estructura ADRLIST,** la matriz contiene estructuras [ADRENTRY,](adrentry.md) en la **estructura SRowSet** la matriz contiene [estructuras SRow.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="e8838-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="e8838-127">**Las estructuras ADRENTRY** y **SRow** son idénticas en diseño.</span><span class="sxs-lookup"><span data-stu-id="e8838-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="e8838-128">Dado que las estructuras **ADRLIST** y **SRowSet** siguen las mismas reglas de asignación, una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de libreta de direcciones se puede convertir en una estructura **ADRLIST** y usarse tal como está.</span><span class="sxs-lookup"><span data-stu-id="e8838-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="e8838-129">En la siguiente ilustración se muestra el diseño de una **estructura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="e8838-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="e8838-130">**Componentes de ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="e8838-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="e8838-131">![Componentes ADRLIST componentes](media/amapi_18.gif "ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="e8838-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="e8838-132">Las **partes ADRENTRY** y [SPropValue](spropvalue.md) de una estructura **ADRLIST** deben asignarse y liberarse independientemente de las demás partes.</span><span class="sxs-lookup"><span data-stu-id="e8838-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="e8838-133">Es decir, cada estructura **SPropValue** debe asignarse individualmente después de asignar y liberar la memoria de la estructura **ADRENTRY** antes de liberar la estructura **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="e8838-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="e8838-134">Esta independencia en el control de la memoria permite a los destinatarios y a las propiedades de destinatarios individuales agregarse o eliminarse libremente de la lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e8838-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="e8838-135">Las [funciones MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) deben usarse para asignar y liberar la estructura **ADRLIST** y todas sus partes.</span><span class="sxs-lookup"><span data-stu-id="e8838-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="e8838-136">Si una lista de destinatarios es demasiado grande para caber en la memoria, los clientes pueden llamar al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabajar con un subconjunto de la lista.</span><span class="sxs-lookup"><span data-stu-id="e8838-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="e8838-137">Los clientes no deben usar los cuadros de diálogo comunes de la libreta de direcciones en esta situación.</span><span class="sxs-lookup"><span data-stu-id="e8838-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="e8838-138">Para obtener más información acerca de cómo asignar memoria para estructuras **ADRENTRY,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e8838-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8838-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8838-139">See also</span></span>

- [<span data-ttu-id="e8838-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e8838-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="e8838-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="e8838-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="e8838-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e8838-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="e8838-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e8838-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="e8838-144">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e8838-144">MAPI Structures</span></span>](mapi-structures.md)

