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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309985"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="700df-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="700df-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="700df-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="700df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="700df-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="700df-105">Deprecated.</span></span> <span data-ttu-id="700df-106">Asigna un nombre nuevo a un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="700df-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="700df-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="700df-107">Parameters</span></span>

 <span data-ttu-id="700df-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="700df-108">_lpUID_</span></span>
  
> <span data-ttu-id="700df-109">a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a cambiar de nombre.</span><span class="sxs-lookup"><span data-stu-id="700df-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="700df-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="700df-110">_ulFlags_</span></span>
  
> <span data-ttu-id="700df-111">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="700df-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="700df-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="700df-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="700df-113">a Un puntero al nuevo nombre del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="700df-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="700df-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="700df-114">Return value</span></span>

<span data-ttu-id="700df-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="700df-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="700df-116">MAPI no admite el cambio de nombre de este servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="700df-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="700df-117">**RenameMsgService** siempre devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="700df-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="700df-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="700df-118">Remarks</span></span>

<span data-ttu-id="700df-119">Para asignar un nuevo nombre a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="700df-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="700df-120">Los nombres de los proveedores de servicios de un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="700df-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="700df-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="700df-121">See also</span></span>



[<span data-ttu-id="700df-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="700df-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="700df-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="700df-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

