---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817896"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="c0ad0-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="c0ad0-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="c0ad0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0ad0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0ad0-105">Elimina un proveedor de servicios desde el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="c0ad0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0ad0-106">Parameters</span></span>

 <span data-ttu-id="c0ad0-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c0ad0-107">_lpUID_</span></span>
  
> <span data-ttu-id="c0ad0-108">[entrada, salida] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0ad0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0ad0-109">Return value</span></span>

<span data-ttu-id="c0ad0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0ad0-110">S_OK</span></span> 
  
> <span data-ttu-id="c0ad0-111">El proveedor se eliminó correctamente desde el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="c0ad0-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c0ad0-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c0ad0-113">No se reconoció la **MAPIUID** indicada por el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="c0ad0-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0ad0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0ad0-114">Remarks</span></span>

<span data-ttu-id="c0ad0-115">El método **IProviderAdmin::DeleteProvider** elimina un proveedor de servicios desde el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="c0ad0-116">**DeleteProvider** determina el proveedor de servicios para eliminar de forma que coincidan con la estructura **MAPIUID** que señala _lpUID_ con el conjunto de identificadores registrados por los proveedores de servicio de active.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="c0ad0-117">La mayoría de los servicios de mensaje no permiten que los proveedores se elimina mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="c0ad0-118">Si el proveedor que se va a eliminar está en uso, **DeleteProvider** se marca para su eliminación en lugar de quitarlo inmediatamente y devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="c0ad0-119">Cuando ya no se usa el proveedor, se elimina.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="c0ad0-120">**DeleteProvider** llama a la función de punto de entrada del servicio de mensajes antes de que se ha quitado el proveedor del servicio.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="c0ad0-121">El parámetro _ulContext_ se establece en MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="c0ad0-122">La función de punto de entrada de servicio de mensaje lleva a cabo las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="c0ad0-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="c0ad0-123">Elimina el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="c0ad0-124">Elimina la sección de perfil de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="c0ad0-125">La función de punto de entrada de servicio de mensajes no se llama de nuevo después de que se ha eliminado el proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0ad0-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0ad0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0ad0-126">See also</span></span>



[<span data-ttu-id="c0ad0-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c0ad0-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c0ad0-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c0ad0-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c0ad0-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0ad0-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

