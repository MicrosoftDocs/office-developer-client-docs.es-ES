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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817736"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="86751-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="86751-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="86751-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86751-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86751-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="86751-105">Deprecated.</span></span> <span data-ttu-id="86751-106">Asigna un nombre nuevo a un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="86751-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="86751-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86751-107">Parameters</span></span>

 <span data-ttu-id="86751-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="86751-108">_lpUID_</span></span>
  
> <span data-ttu-id="86751-109">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="86751-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="86751-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="86751-110">_ulFlags_</span></span>
  
> <span data-ttu-id="86751-111">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="86751-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="86751-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="86751-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="86751-113">[entrada] Un puntero al nuevo nombre para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="86751-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86751-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86751-114">Return value</span></span>

<span data-ttu-id="86751-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="86751-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="86751-116">MAPI no es compatible con el cambio de nombre de este servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="86751-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="86751-117">**RenameMsgService** siempre devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="86751-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86751-118">Notas</span><span class="sxs-lookup"><span data-stu-id="86751-118">Remarks</span></span>

<span data-ttu-id="86751-119">Para asignar un nombre nuevo a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="86751-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="86751-120">Los nombres de los proveedores de servicios en un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="86751-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86751-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="86751-121">See also</span></span>



[<span data-ttu-id="86751-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="86751-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="86751-123">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="86751-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

