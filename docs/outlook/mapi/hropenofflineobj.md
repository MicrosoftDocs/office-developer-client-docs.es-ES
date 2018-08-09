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
ms.openlocfilehash: ac6584819b5dfa96a5f7816f1d77b89323e3eaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817086"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="168cd-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="168cd-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="168cd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="168cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="168cd-105">Se abre un objeto sin conexión basada en un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="168cd-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="168cd-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="168cd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="168cd-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="168cd-107">Exported by:</span></span>  <br/> |<span data-ttu-id="168cd-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="168cd-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="168cd-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="168cd-109">Called by:</span></span>  <br/> |<span data-ttu-id="168cd-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="168cd-110">Client</span></span>  <br/> |
|<span data-ttu-id="168cd-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="168cd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="168cd-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="168cd-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="168cd-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="168cd-113">Parameters</span></span>

 <span data-ttu-id="168cd-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="168cd-114">_ulReserved_</span></span>
  
> <span data-ttu-id="168cd-115">[entrada] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="168cd-115">[in] This parameter is not used.</span></span> <span data-ttu-id="168cd-116">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="168cd-116">It must be 0.</span></span>
    
 <span data-ttu-id="168cd-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="168cd-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="168cd-118">[entrada] El nombre del perfil que es el objeto sin conexión para.</span><span class="sxs-lookup"><span data-stu-id="168cd-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="168cd-119">Se expresará en Unicode.</span><span class="sxs-lookup"><span data-stu-id="168cd-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="168cd-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="168cd-120">_pGUID_</span></span>
  
> <span data-ttu-id="168cd-121">[entrada] Puntero a un GUID que se puede usar para identificar de forma única este objeto desde otros objetos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="168cd-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="168cd-122">Debe ser **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="168cd-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="168cd-123">_Conserva_</span><span class="sxs-lookup"><span data-stu-id="168cd-123">_pReserved_</span></span>
  
> <span data-ttu-id="168cd-124">[entrada] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="168cd-124">[in] This parameter is not used.</span></span> <span data-ttu-id="168cd-125">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="168cd-125">It must be **null**.</span></span>
    
 <span data-ttu-id="168cd-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="168cd-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="168cd-127">[out] Un puntero al objeto solicitado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="168cd-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="168cd-128">El autor de la llamada puede usar este puntero para obtener acceso a la [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) interfaz para buscar las devoluciones de llamada que admite este objeto y para configurar las devoluciones de llamada para él.</span><span class="sxs-lookup"><span data-stu-id="168cd-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="168cd-129">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="168cd-129">Return values</span></span>

<span data-ttu-id="168cd-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="168cd-130">S_OK</span></span> 
  
- <span data-ttu-id="168cd-131">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="168cd-131">The function call is successful.</span></span>
    
<span data-ttu-id="168cd-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="168cd-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="168cd-133">Error en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="168cd-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="168cd-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="168cd-134">Remarks</span></span>

<span data-ttu-id="168cd-135">Se trata de la primera llamada realizada por un cliente cuando el cliente desea recibir una notificación de los cambios de estado de conexión para un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="168cd-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="168cd-136">Tras llamar a **HrOpenOfflineObj**, el cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="168cd-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="168cd-137">El cliente puede comprobar para los tipos de devoluciones de llamada admitidos por el objeto (mediante el uso de [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) y, a continuación, configurar las devoluciones de llamada para él (mediante [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="168cd-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="168cd-138">Cuando se usa [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) para buscar la dirección de esta función en msmapi32.dll, especifique **HrOpenOfflineObj@20** como el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="168cd-138">When using [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="168cd-139">**HrOpenOfflineObj** sólo funciona para los clientes que son proveedores MAPI, complementos COM y las extensiones de cliente de Exchange que se ejecuta dentro del proceso de Outlook.</span><span class="sxs-lookup"><span data-stu-id="168cd-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="168cd-140">De lo contrario, **HrOpenOfflineObj** devuelve **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="168cd-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="168cd-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="168cd-141">See also</span></span>



[<span data-ttu-id="168cd-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="168cd-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="168cd-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="168cd-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="168cd-144">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="168cd-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="168cd-145">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="168cd-145">MAPI Constants</span></span>](mapi-constants.md)

