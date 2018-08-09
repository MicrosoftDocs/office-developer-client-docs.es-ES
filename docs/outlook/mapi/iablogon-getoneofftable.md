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
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817099"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="6dcf7-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6dcf7-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="6dcf7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dcf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dcf7-105">Devuelve un objeto table de plantillas de uso único para la creación de los destinatarios que se agregará a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6dcf7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6dcf7-106">Parameters</span></span>

 <span data-ttu-id="6dcf7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dcf7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6dcf7-108">[entrada] Una máscara de bits de indicadores que controla el tipo de columnas de cadena que se incluyen en la tabla.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="6dcf7-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="6dcf7-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6dcf7-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6dcf7-111">Las columnas de cadena se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6dcf7-112">Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6dcf7-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6dcf7-113">_lppTable_</span></span>
  
> <span data-ttu-id="6dcf7-114">[out] Un puntero a un puntero a la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dcf7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dcf7-115">Return value</span></span>

<span data-ttu-id="6dcf7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dcf7-116">S_OK</span></span> 
  
> <span data-ttu-id="6dcf7-117">En la tabla de uso único se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="6dcf7-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6dcf7-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6dcf7-119">Se ha establecido el indicador MAPI_UNICODE y el proveedor de la libreta de direcciones no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de la libreta de direcciones admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="6dcf7-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6dcf7-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6dcf7-121">El proveedor de la libreta de direcciones no proporciona las plantillas de uso único.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dcf7-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dcf7-122">Remarks</span></span>

<span data-ttu-id="6dcf7-123">MAPI llama al método de **GetOneOffTable** para hacer que las plantillas de uso único disponibles para crear a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="6dcf7-124">Los destinatarios nuevos se agregan a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="6dcf7-125">Los proveedores de la libreta de direcciones deben admitir la notificación en su tabla de uso único para informar a MAPI de las modificaciones de plantilla.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="6dcf7-126">MAPI mantiene en la tabla de uso único abierta para habilitar la actualización dinámica.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="6dcf7-127">Los proveedores de la libreta de direcciones también pueden admitir una tabla de uso único para cada uno de sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="6dcf7-128">Los autores de llamadas recuperar esta tabla de uso único, llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y solicite la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6dcf7-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="6dcf7-129">Las plantillas disponibles en esta tabla se usan para agregar a destinatarios al contenedor.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="6dcf7-130">Para obtener una descripción de las diferencias entre los dos tipos de tablas de uso único, vea [Implementación de tablas de uso único](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6dcf7-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="6dcf7-131">Para obtener una lista de las columnas necesarias en la tabla de uso único de un proveedor libreta de direcciones, vea [Las tablas de uso único](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6dcf7-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6dcf7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dcf7-132">See also</span></span>



[<span data-ttu-id="6dcf7-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6dcf7-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="6dcf7-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="6dcf7-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="6dcf7-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6dcf7-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="6dcf7-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dcf7-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

