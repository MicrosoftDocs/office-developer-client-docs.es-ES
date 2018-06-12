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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817745"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="7c5ed-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="7c5ed-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="7c5ed-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c5ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c5ed-105">Copia un servicio de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="7c5ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c5ed-106">Parameters</span></span>

 <span data-ttu-id="7c5ed-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-107">_lpUID_</span></span>
  
> <span data-ttu-id="7c5ed-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes para copiar.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="7c5ed-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="7c5ed-110">[entrada] Este parámetro ha quedado obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="7c5ed-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="7c5ed-112">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil de servicio de mensajes para copiar.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="7c5ed-113">Si se pasa NULL da como resultado la interfaz de sección del perfil estándar, [IProfSect](iprofsectimapiprop.md), que se usa.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="7c5ed-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="7c5ed-115">[entrada] Un puntero a la IID que representa la interfaz que se usará para tener acceso al objeto al que apunta el parámetro _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="7c5ed-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="7c5ed-116">Si se pasa NULL da como resultado la interfaz de sesión [IMAPISession](imapisessioniunknown.md), que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="7c5ed-117">También se puede establecer el parámetro _lpInterfaceDst_ en IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="7c5ed-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="7c5ed-119">[entrada] Un puntero a un puntero a un objeto de administración de servicio de sesión o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="7c5ed-120">El tipo de objeto debe coincidir con el identificador de interfaz que se pasó _lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="7c5ed-121">Punteros a objetos válidos son LPMAPISESSION y LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="7c5ed-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="7c5ed-123">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="7c5ed-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c5ed-124">_ulFlags_</span></span>
  
> <span data-ttu-id="7c5ed-125">[entrada] Una máscara de bits de indicadores que controla cómo se copia el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="7c5ed-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="7c5ed-126">The following flags can be set:</span></span>
    
<span data-ttu-id="7c5ed-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7c5ed-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="7c5ed-128">Solicitudes que el servicio de mensajes siempre mostrar una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c5ed-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c5ed-129">Return value</span></span>

<span data-ttu-id="7c5ed-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c5ed-130">S_OK</span></span> 
  
> <span data-ttu-id="7c5ed-131">El servicio de mensajes se ha copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="7c5ed-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7c5ed-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7c5ed-133">El servicio de mensajes ya está en el perfil y no admite varias instancias de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="7c5ed-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7c5ed-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7c5ed-135">El **MAPIUID** que señala _lpUID_ no hace referencia a un servicio de mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7c5ed-136">Notas</span><span class="sxs-lookup"><span data-stu-id="7c5ed-136">Remarks</span></span>

<span data-ttu-id="7c5ed-137">El método **IMsgServiceAdmin::CopyMsgService** copia un servicio de mensajes en un perfil, el perfil activo u otro perfil.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="7c5ed-138">El perfil que contiene el servicio de mensajes que se va a copiar y el destino no tienen que ser el mismo perfil, pero pueden ser.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="7c5ed-139">Función de punto de entrada del servicio de mensajes no se llama para una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="7c5ed-140">El servicio de mensajes copiados tiene la misma configuración que su original.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="7c5ed-141">Para cambiar esta configuración, un cliente debe llamar al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5ed-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c5ed-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c5ed-142">See also</span></span>



[<span data-ttu-id="7c5ed-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="7c5ed-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="7c5ed-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7c5ed-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7c5ed-145">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c5ed-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

