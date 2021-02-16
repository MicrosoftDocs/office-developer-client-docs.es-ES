---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411879"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="6935f-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6935f-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="6935f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6935f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6935f-105">Devuelve una tabla de plantillas de uso único para crear destinatarios que se agregarán a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="6935f-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6935f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6935f-106">Parameters</span></span>

 <span data-ttu-id="6935f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6935f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6935f-108">[entrada] Máscara de bits de marcas que controla el tipo de columnas de cadena incluidas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="6935f-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="6935f-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="6935f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6935f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6935f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6935f-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6935f-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6935f-112">Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6935f-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6935f-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6935f-113">_lppTable_</span></span>
  
> <span data-ttu-id="6935f-114">[salida] Puntero a un puntero a la tabla de un solo acceso.</span><span class="sxs-lookup"><span data-stu-id="6935f-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6935f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6935f-115">Return value</span></span>

<span data-ttu-id="6935f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6935f-116">S_OK</span></span> 
  
> <span data-ttu-id="6935f-117">La tabla de un solo juego se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6935f-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="6935f-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6935f-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6935f-119">Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="6935f-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="6935f-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6935f-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6935f-121">El proveedor de libreta de direcciones no proporciona ninguna plantilla de pago único.</span><span class="sxs-lookup"><span data-stu-id="6935f-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6935f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6935f-122">Remarks</span></span>

<span data-ttu-id="6935f-123">MAPI llama al **método GetOneOffTable** para que las plantillas de uso único estén disponibles para crear destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6935f-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="6935f-124">Los nuevos destinatarios se agregan a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="6935f-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="6935f-125">Los proveedores de libretas de direcciones deben admitir notificaciones en su tabla de uso único para informar a MAPI de las modificaciones de plantilla.</span><span class="sxs-lookup"><span data-stu-id="6935f-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="6935f-126">MAPI mantiene abierta la tabla de uso único para habilitar la actualización dinámica.</span><span class="sxs-lookup"><span data-stu-id="6935f-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="6935f-127">Los proveedores de libretas de direcciones también pueden admitir una tabla de uso único para cada uno de sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="6935f-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="6935f-128">Los autores de llamadas recuperan esta tabla de uso único llamando al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y solicitando la **propiedad PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6935f-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="6935f-129">Las plantillas disponibles a través de esta tabla se usan para agregar destinatarios al contenedor.</span><span class="sxs-lookup"><span data-stu-id="6935f-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="6935f-130">Para obtener una explicación de las diferencias entre los dos tipos de tablas de uso único, vea Implementar One-Off [tablas.](implementing-one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6935f-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="6935f-131">Para obtener una lista de las columnas necesarias en la tabla de uso único de un proveedor de libreta de direcciones, vea [Tablas de uso único.](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6935f-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6935f-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6935f-132">See also</span></span>



[<span data-ttu-id="6935f-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6935f-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="6935f-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="6935f-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="6935f-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6935f-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="6935f-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6935f-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

