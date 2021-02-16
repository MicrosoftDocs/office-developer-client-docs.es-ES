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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405908"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="94a02-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="94a02-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="94a02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94a02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94a02-105">Devuelve un [puntero IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94a02-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="94a02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94a02-106">Parameters</span></span>

 <span data-ttu-id="94a02-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94a02-107">_ulFlags_</span></span>
  
> <span data-ttu-id="94a02-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="94a02-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="94a02-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="94a02-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="94a02-110">[salida] Puntero a un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94a02-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94a02-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94a02-111">Return value</span></span>

<span data-ttu-id="94a02-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="94a02-112">S_OK</span></span> 
  
> <span data-ttu-id="94a02-113">Se devolvió correctamente un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94a02-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="94a02-114">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="94a02-114">Notes to callers</span></span>

<span data-ttu-id="94a02-115">El **método IMAPISession::AdminServices** crea un objeto de administración del servicio de mensajes, un objeto que admite la interfaz **IMsgServiceAdmin** y devuelve un puntero.</span><span class="sxs-lookup"><span data-stu-id="94a02-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="94a02-116">Mediante este puntero, puede llamar a los métodos **IMsgServiceAdmin** para cambiar cualquiera de los servicios de mensajes en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="94a02-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="94a02-117">Tenga en cuenta que estos cambios no tienen efecto hasta la siguiente sesión; la sesión actual no se ha afectado.</span><span class="sxs-lookup"><span data-stu-id="94a02-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="94a02-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="94a02-118">MFCMAPI reference</span></span>

<span data-ttu-id="94a02-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="94a02-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="94a02-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="94a02-120">**File**</span></span>|<span data-ttu-id="94a02-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="94a02-121">**Function**</span></span>|<span data-ttu-id="94a02-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="94a02-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94a02-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="94a02-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="94a02-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="94a02-124">GetServerName</span></span>  <br/> |<span data-ttu-id="94a02-125">MFCMAPI usa el **método IMAPISession::AdminServices** para tener acceso al perfil y leer el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="94a02-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94a02-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94a02-126">See also</span></span>



[<span data-ttu-id="94a02-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94a02-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="94a02-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="94a02-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="94a02-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94a02-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="94a02-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="94a02-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

