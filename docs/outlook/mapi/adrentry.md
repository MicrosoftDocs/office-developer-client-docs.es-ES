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
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421441"
---
# <a name="adrentry"></a><span data-ttu-id="ab0aa-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ab0aa-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="ab0aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab0aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab0aa-105">Describe cero o más propiedades que pertenecen a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab0aa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ab0aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab0aa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ab0aa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="ab0aa-108">Members</span><span class="sxs-lookup"><span data-stu-id="ab0aa-108">Members</span></span>

 <span data-ttu-id="ab0aa-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="ab0aa-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="ab0aa-110">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ab0aa-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ab0aa-111">**cValues**</span></span>
  
> <span data-ttu-id="ab0aa-112">Número de propiedades de la matriz de valores de propiedad a la que señala el miembro **rgPropVals** .</span><span class="sxs-lookup"><span data-stu-id="ab0aa-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="ab0aa-113">El miembro **cValues** puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="ab0aa-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="ab0aa-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="ab0aa-115">Puntero a una matriz de valores de propiedad que describe las propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="ab0aa-116">El miembro **rgPropVals** puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ab0aa-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab0aa-117">Remarks</span></span>

<span data-ttu-id="ab0aa-118">Una estructura **ADRENTRY** describe las propiedades que pertenecen a un único destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="ab0aa-119">Las propiedades que se suelen usar para describir a un destinatario son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab0aa-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="ab0aa-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ab0aa-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="ab0aa-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ab0aa-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="ab0aa-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ab0aa-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="ab0aa-123">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ab0aa-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="ab0aa-124">Cuando se muestra un identificador de \*\*\*\* entrada o una propiedad de la matriz de [SPropValue](spropvalue.md) para un destinatario, esto indica que se ha resuelto el destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="ab0aa-125">Los clientes llaman al método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para asegurarse de que se han resuelto todos los destinatarios de la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="ab0aa-126">Solo se pueden enviar con mensajes los destinatarios resueltos.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="ab0aa-127">Las estructuras **ADRENTRY** suelen combinarse para formar una matriz para el miembro **aEntries** de una estructura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="ab0aa-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="ab0aa-128">Las estructuras **ADRENTRY** y [SRow](srow.md) son idénticas porque contienen un miembro reservado, una matriz de valores de propiedad y un recuento de valores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="ab0aa-129">Mientras que las estructuras **ADRENTRY** se combinan para formar el miembro **aEntries** de una estructura **ADRLIST** , las estructuras **SRow** se combinan para formar el miembro **aRow** de una estructura [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="ab0aa-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="ab0aa-130">Ambos tipos de estructuras siguen las mismas reglas de asignación, lo que implica que una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de libretas de direcciones se puede convertir en una estructura **ADRLIST** y usar tal cual.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="ab0aa-131">Una estructura **ADRENTRY** puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="ab0aa-132">Por ejemplo, una estructura **ADRENTRY** que está incluida en la estructura **ADRLIST** a la que apunta el parámetro _LppAdrList_ en una llamada a **IAddrBook:: Address** puede estar vacía cuando se quita un destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0aa-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="ab0aa-133">Para obtener más información acerca de cómo asignar memoria para estructuras de **ADRENTRY** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ab0aa-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab0aa-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="ab0aa-134">See also</span></span>



[<span data-ttu-id="ab0aa-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ab0aa-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ab0aa-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ab0aa-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="ab0aa-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ab0aa-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ab0aa-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ab0aa-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ab0aa-139">SRow</span><span class="sxs-lookup"><span data-stu-id="ab0aa-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="ab0aa-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ab0aa-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="ab0aa-141">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ab0aa-141">MAPI Structures</span></span>](mapi-structures.md)

