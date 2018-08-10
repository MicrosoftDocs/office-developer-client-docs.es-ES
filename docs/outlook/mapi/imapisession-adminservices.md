---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817456"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="1405f-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1405f-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="1405f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1405f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1405f-105">Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1405f-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="1405f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1405f-106">Parameters</span></span>

 <span data-ttu-id="1405f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1405f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1405f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1405f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1405f-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="1405f-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="1405f-110">[out] Un puntero a un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1405f-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1405f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1405f-111">Return value</span></span>

<span data-ttu-id="1405f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1405f-112">S_OK</span></span> 
  
> <span data-ttu-id="1405f-113">Un puntero a un objeto de administración del servicio de mensajes se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="1405f-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1405f-114">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1405f-114">Notes to callers</span></span>

<span data-ttu-id="1405f-115">El método **IMAPISession::AdminServices** crea un objeto de administración de servicio de mensaje, un objeto que admite la interfaz **IMsgServiceAdmin** y devuelve un puntero.</span><span class="sxs-lookup"><span data-stu-id="1405f-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="1405f-116">Mediante el uso de este puntero, puede llamar a métodos **IMsgServiceAdmin** para cambiar cualquiera de los servicios de mensaje en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="1405f-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="1405f-117">Tenga en cuenta que estos cambios no tendrán efecto hasta la siguiente sesión; la sesión actual no se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="1405f-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1405f-118">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1405f-118">MFCMAPI reference</span></span>

<span data-ttu-id="1405f-119">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1405f-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1405f-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1405f-120">**File**</span></span>|<span data-ttu-id="1405f-121">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1405f-121">**Function**</span></span>|<span data-ttu-id="1405f-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1405f-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1405f-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1405f-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1405f-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="1405f-124">GetServerName</span></span>  <br/> |<span data-ttu-id="1405f-125">MFCMAPI usa el método **IMAPISession::AdminServices** para tener acceso a los perfiles para leer el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="1405f-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1405f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1405f-126">See also</span></span>



[<span data-ttu-id="1405f-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1405f-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="1405f-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1405f-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="1405f-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1405f-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1405f-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1405f-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
