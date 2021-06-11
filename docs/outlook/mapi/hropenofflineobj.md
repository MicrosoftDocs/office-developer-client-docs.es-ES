---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347750"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="aa84f-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="aa84f-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="aa84f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa84f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa84f-105">Abre un objeto sin conexión basado en un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="aa84f-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aa84f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="aa84f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa84f-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="aa84f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="aa84f-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="aa84f-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="aa84f-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="aa84f-109">Called by:</span></span>  <br/> |<span data-ttu-id="aa84f-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="aa84f-110">Client</span></span>  <br/> |
|<span data-ttu-id="aa84f-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="aa84f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa84f-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="aa84f-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="aa84f-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="aa84f-113">Parameters</span></span>

 <span data-ttu-id="aa84f-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="aa84f-114">_ulReserved_</span></span>
  
> <span data-ttu-id="aa84f-115">[in] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="aa84f-115">[in] This parameter is not used.</span></span> <span data-ttu-id="aa84f-116">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="aa84f-116">It must be 0.</span></span>
    
 <span data-ttu-id="aa84f-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="aa84f-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="aa84f-118">[in] Nombre del perfil para el que está el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="aa84f-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="aa84f-119">Debe expresarse en Unicode.</span><span class="sxs-lookup"><span data-stu-id="aa84f-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="aa84f-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="aa84f-120">_pGUID_</span></span>
  
> <span data-ttu-id="aa84f-121">[in] Puntero a un GUID que se puede usar para identificar de forma única este objeto desde otros objetos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="aa84f-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="aa84f-122">Debe ser **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="aa84f-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="aa84f-123">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="aa84f-123">_pReserved_</span></span>
  
> <span data-ttu-id="aa84f-124">[in] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="aa84f-124">[in] This parameter is not used.</span></span> <span data-ttu-id="aa84f-125">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="aa84f-125">It must be **null**.</span></span>
    
 <span data-ttu-id="aa84f-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="aa84f-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="aa84f-127">[salida] Puntero al objeto sin conexión solicitado.</span><span class="sxs-lookup"><span data-stu-id="aa84f-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="aa84f-128">El autor de la llamada puede usar este puntero para obtener acceso a la interfaz [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) para buscar las devoluciones de llamada que admite este objeto y configurar las devoluciones de llamada para él.</span><span class="sxs-lookup"><span data-stu-id="aa84f-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="aa84f-129">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="aa84f-129">Return values</span></span>

<span data-ttu-id="aa84f-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa84f-130">S_OK</span></span> 
  
- <span data-ttu-id="aa84f-131">La llamada a la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa84f-131">The function call is successful.</span></span>
    
<span data-ttu-id="aa84f-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aa84f-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="aa84f-133">Error en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="aa84f-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa84f-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa84f-134">Remarks</span></span>

<span data-ttu-id="aa84f-135">Esta es la primera llamada que realiza un cliente cuando el cliente desea recibir una notificación de cualquier cambio de estado de conexión para un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="aa84f-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="aa84f-136">Al llamar **a HrOpenOfflineObj**, el cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="aa84f-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="aa84f-137">El cliente puede comprobar los tipos de devoluciones de llamada compatibles con el objeto (mediante [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) y, a continuación, configurar devoluciones de llamada para él (mediante [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="aa84f-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="aa84f-138">Al usar [GetProcAddress para](https://msdn.microsoft.com/library/ms683212.aspx) buscar la dirección de esta función en msmapi32.dll, especifique **HrOpenOfflineObj@20** como el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="aa84f-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="aa84f-139">**HrOpenOfflineObj** solo funciona para clientes que son proveedores MAPI, complementos COM y extensiones de cliente Exchange que se ejecutan dentro del Outlook cliente.</span><span class="sxs-lookup"><span data-stu-id="aa84f-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="aa84f-140">De lo contrario, **HrOpenOfflineObj** **devuelve MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="aa84f-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa84f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa84f-141">See also</span></span>



[<span data-ttu-id="aa84f-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa84f-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="aa84f-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="aa84f-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="aa84f-144">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="aa84f-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="aa84f-145">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="aa84f-145">MAPI Constants</span></span>](mapi-constants.md)

