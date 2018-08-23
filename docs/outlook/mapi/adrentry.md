---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f3a62f6783e3b1a0a0423a08c7f5e866b42b81f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569179"
---
# <a name="adrentry"></a><span data-ttu-id="7efb3-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7efb3-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="7efb3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7efb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7efb3-105">Se describen cero o más propiedades que pertenecen a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="7efb3-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7efb3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7efb3-106">Header file:</span></span>  <br/> |<span data-ttu-id="7efb3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7efb3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="7efb3-108">Members</span><span class="sxs-lookup"><span data-stu-id="7efb3-108">Members</span></span>

 <span data-ttu-id="7efb3-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="7efb3-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="7efb3-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7efb3-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7efb3-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7efb3-111">**cValues**</span></span>
  
> <span data-ttu-id="7efb3-112">Recuento de propiedades de la matriz de valores de propiedad que señala el miembro **rgPropVals** .</span><span class="sxs-lookup"><span data-stu-id="7efb3-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="7efb3-113">El miembro **cValues** puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="7efb3-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="7efb3-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="7efb3-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="7efb3-115">Puntero a una matriz de valores de propiedad que describe las propiedades para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="7efb3-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="7efb3-116">El miembro **rgPropVals** puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="7efb3-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7efb3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7efb3-117">Remarks</span></span>

<span data-ttu-id="7efb3-118">Una estructura de **ADRENTRY** describe las propiedades que pertenecen a un solo destinatario.</span><span class="sxs-lookup"><span data-stu-id="7efb3-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="7efb3-119">Las propiedades que se usan normalmente para describir a un destinatario incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7efb3-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="7efb3-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7efb3-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="7efb3-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7efb3-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="7efb3-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7efb3-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="7efb3-123">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7efb3-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="7efb3-124">Cuando una propiedad de **entrada del objeto** o el identificador de entrada aparece en la matriz [SPropValue](spropvalue.md) para un destinatario, esto indica que el destinatario se ha resuelto.</span><span class="sxs-lookup"><span data-stu-id="7efb3-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="7efb3-125">Los clientes de llaman al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que se han resueltos todos los destinatarios en la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="7efb3-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="7efb3-126">Destinatarios resueltos sólo se pueden enviar con los mensajes.</span><span class="sxs-lookup"><span data-stu-id="7efb3-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="7efb3-127">Estructuras **ADRENTRY** normalmente se combinan para formar una matriz para el miembro **aEntries** de una estructura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7efb3-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="7efb3-128">Estructuras **ADRENTRY** y estructuras [SRow](srow.md) son idénticas porque ambos contienen un miembro reservado, una matriz de valores de propiedad y un recuento de valores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7efb3-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="7efb3-129">Mientras que las estructuras **ADRENTRY** se combinan para formar al miembro **aEntries** de una estructura **ADRLIST** , **SRow** estructuras se combinan para formar al miembro **aRow** de una estructura de [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="7efb3-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="7efb3-130">Ambos tipos de estructuras siguen las mismas reglas de asignación, lo que implica que se puede convertir en una estructura de **ADRLIST** y utilizada como es una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7efb3-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="7efb3-131">Una estructura de **ADRENTRY** puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="7efb3-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="7efb3-132">Por ejemplo, una estructura **ADRENTRY** que se encuentra en la estructura **ADRLIST** indicada por el parámetro _lppAdrList_ en una llamada a **IAddrBook::Address** puede estar vacía cuando se está eliminando un destinatario.</span><span class="sxs-lookup"><span data-stu-id="7efb3-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="7efb3-133">Para obtener más información acerca de cómo asignar memoria para las estructuras **ADRENTRY** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="7efb3-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7efb3-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7efb3-134">See also</span></span>



[<span data-ttu-id="7efb3-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="7efb3-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="7efb3-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="7efb3-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="7efb3-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7efb3-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7efb3-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="7efb3-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="7efb3-139">SRow</span><span class="sxs-lookup"><span data-stu-id="7efb3-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="7efb3-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7efb3-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="7efb3-141">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7efb3-141">MAPI Structures</span></span>](mapi-structures.md)

