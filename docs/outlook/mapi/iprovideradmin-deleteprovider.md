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
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279552"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="d9c73-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="d9c73-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="d9c73-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9c73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9c73-105">Elimina un proveedor de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d9c73-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="d9c73-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9c73-106">Parameters</span></span>

 <span data-ttu-id="d9c73-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d9c73-107">_lpUID_</span></span>
  
> <span data-ttu-id="d9c73-108">[in, out] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa al proveedor que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="d9c73-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d9c73-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9c73-109">Return value</span></span>

<span data-ttu-id="d9c73-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9c73-110">S_OK</span></span> 
  
> <span data-ttu-id="d9c73-111">El proveedor se eliminó correctamente del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d9c73-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="d9c73-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d9c73-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d9c73-113">No se reconoció el **MAPIUID** al que señala el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="d9c73-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9c73-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9c73-114">Remarks</span></span>

<span data-ttu-id="d9c73-115">El método **IProviderAdmin::D eleteprovider** elimina un proveedor de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d9c73-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="d9c73-116">**DeleteProvider** determina el proveedor de servicios que se va a eliminar al hacer coincidir la estructura **MAPIUID** a la que apunta _lpUID_ con el conjunto de identificadores registrados por los proveedores de servicios activos.</span><span class="sxs-lookup"><span data-stu-id="d9c73-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="d9c73-117">La mayoría de los servicios de mensajes no permiten que se eliminen los proveedores mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="d9c73-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="d9c73-118">Si el proveedor que se va a eliminar está en uso, **DeleteProvider** lo marca para su eliminación en lugar de quitarlo inmediatamente y Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="d9c73-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="d9c73-119">Cuando el proveedor ya no se usa, se elimina.</span><span class="sxs-lookup"><span data-stu-id="d9c73-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="d9c73-120">**DeleteProvider** llama a la función de punto de entrada del servicio de mensajería antes de que se quite el proveedor del servicio.</span><span class="sxs-lookup"><span data-stu-id="d9c73-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="d9c73-121">El parámetro _ulContext_ está establecido en MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="d9c73-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="d9c73-122">La función de punto de entrada del servicio de mensajes realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d9c73-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="d9c73-123">Elimina el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d9c73-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="d9c73-124">Elimina la sección de perfil del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d9c73-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="d9c73-125">No se llama de nuevo a la función de punto de entrada del servicio de mensajes después de que se haya eliminado el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d9c73-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9c73-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9c73-126">See also</span></span>



[<span data-ttu-id="d9c73-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d9c73-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d9c73-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="d9c73-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="d9c73-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9c73-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

