---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432124"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="7136e-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="7136e-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="7136e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7136e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7136e-105">Copia un servicio de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7136e-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7136e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7136e-106">Parameters</span></span>

 <span data-ttu-id="7136e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="7136e-107">_lpUID_</span></span>
  
> <span data-ttu-id="7136e-108">[in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se debe copiar.</span><span class="sxs-lookup"><span data-stu-id="7136e-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="7136e-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="7136e-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="7136e-110">[in] Este parámetro ha quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="7136e-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="7136e-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="7136e-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="7136e-112">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil del servicio de mensajes que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="7136e-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="7136e-113">Si se pasa NULL, se usa la interfaz de sección de perfil [estándar, IProfSect.](iprofsectimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="7136e-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="7136e-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="7136e-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="7136e-115">[in] Puntero al IID que representa la interfaz que se usará para tener acceso al objeto al que apunta el _parámetro lpObjectDst._</span><span class="sxs-lookup"><span data-stu-id="7136e-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="7136e-116">Si se pasa NULL, se usa la interfaz de [sesión, IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="7136e-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="7136e-117">El  _parámetro lpInterfaceDst_ también se puede establecer en IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="7136e-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="7136e-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="7136e-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="7136e-119">[in] Puntero a un puntero a un objeto de administración de servicio de mensajes o de sesión.</span><span class="sxs-lookup"><span data-stu-id="7136e-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="7136e-120">El tipo de objeto debe corresponder al identificador de interfaz pasado  _en lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="7136e-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="7136e-121">Los punteros de objeto válidos son LPMAPISESSION y LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="7136e-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="7136e-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7136e-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="7136e-123">[in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método.</span><span class="sxs-lookup"><span data-stu-id="7136e-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="7136e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7136e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="7136e-125">[in] Máscara de bits de marcas que controla cómo se copia el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7136e-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="7136e-126">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="7136e-126">The following flags can be set:</span></span>
    
<span data-ttu-id="7136e-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7136e-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="7136e-128">Solicita que el servicio de mensajes muestre siempre una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="7136e-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7136e-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7136e-129">Return value</span></span>

<span data-ttu-id="7136e-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7136e-130">S_OK</span></span> 
  
> <span data-ttu-id="7136e-131">El servicio de mensajes se copió correctamente.</span><span class="sxs-lookup"><span data-stu-id="7136e-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="7136e-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7136e-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7136e-133">El servicio de mensajes ya está en el perfil y no permite varias instancias de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="7136e-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="7136e-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7136e-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7136e-135">El **MAPIUID al** que  _apunta lpUID_ no hace referencia a un servicio de mensajes existente.</span><span class="sxs-lookup"><span data-stu-id="7136e-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7136e-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7136e-136">Remarks</span></span>

<span data-ttu-id="7136e-137">El **método IMsgServiceAdmin::CopyMsgService** copia un servicio de mensajes en un perfil, ya sea el perfil activo u otro perfil.</span><span class="sxs-lookup"><span data-stu-id="7136e-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="7136e-138">El perfil que contiene el servicio de mensajes que se va a copiar y el destino no tiene que ser el mismo perfil, pero pueden serlo.</span><span class="sxs-lookup"><span data-stu-id="7136e-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="7136e-139">No se llama a la función de punto de entrada del servicio de mensajes para una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="7136e-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="7136e-140">El servicio de mensajes copiado tiene las mismas opciones de configuración que su original.</span><span class="sxs-lookup"><span data-stu-id="7136e-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="7136e-141">Para cambiar esta configuración, un cliente debe llamar al [método IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="7136e-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7136e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7136e-142">See also</span></span>



[<span data-ttu-id="7136e-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="7136e-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="7136e-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7136e-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7136e-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7136e-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

