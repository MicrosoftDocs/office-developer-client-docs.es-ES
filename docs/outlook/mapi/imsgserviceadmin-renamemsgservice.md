---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422106"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="22ce6-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="22ce6-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="22ce6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22ce6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22ce6-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="22ce6-105">Deprecated.</span></span> <span data-ttu-id="22ce6-106">Asigna un nombre nuevo a un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22ce6-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="22ce6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="22ce6-107">Parameters</span></span>

 <span data-ttu-id="22ce6-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="22ce6-108">_lpUID_</span></span>
  
> <span data-ttu-id="22ce6-109">a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a cambiar de nombre.</span><span class="sxs-lookup"><span data-stu-id="22ce6-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="22ce6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22ce6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="22ce6-111">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="22ce6-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="22ce6-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="22ce6-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="22ce6-113">a Un puntero al nuevo nombre del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22ce6-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22ce6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22ce6-114">Return value</span></span>

<span data-ttu-id="22ce6-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="22ce6-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="22ce6-116">MAPI no admite el cambio de nombre de este servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22ce6-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="22ce6-117">**RenameMsgService** siempre devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="22ce6-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22ce6-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22ce6-118">Remarks</span></span>

<span data-ttu-id="22ce6-119">Para asignar un nuevo nombre a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22ce6-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="22ce6-120">Los nombres de los proveedores de servicios de un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22ce6-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22ce6-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="22ce6-121">See also</span></span>



[<span data-ttu-id="22ce6-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="22ce6-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="22ce6-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22ce6-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

