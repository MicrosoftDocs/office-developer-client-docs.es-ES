---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420097"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="59202-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="59202-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="59202-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59202-105">Establece el orden en que se llama a los proveedores de transporte para entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="59202-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="59202-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="59202-106">Parameters</span></span>

 <span data-ttu-id="59202-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="59202-107">_cUID_</span></span>
  
> <span data-ttu-id="59202-108">[in] Recuento de identificadores únicos en el _parámetro lpUIDList._</span><span class="sxs-lookup"><span data-stu-id="59202-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="59202-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="59202-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="59202-110">[in] Puntero a una matriz de identificadores únicos que representan proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="59202-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="59202-111">La matriz contiene un identificador para cada proveedor de transporte configurado en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="59202-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="59202-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59202-112">_ulFlags_</span></span>
  
> <span data-ttu-id="59202-113">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="59202-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59202-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59202-114">Return value</span></span>

<span data-ttu-id="59202-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="59202-115">S_OK</span></span> 
  
> <span data-ttu-id="59202-116">El orden de transporte se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="59202-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="59202-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="59202-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="59202-118">El valor del  _parámetro cUID_ difiere del número de proveedores de transporte en realidad en el perfil.</span><span class="sxs-lookup"><span data-stu-id="59202-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="59202-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="59202-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="59202-120">Una o varias de las estructuras [MAPIUID](mapiuid.md) pasadas en el parámetro  _lpUIDList_ no hacen referencia a un proveedor de transporte actualmente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="59202-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59202-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59202-121">Remarks</span></span>

<span data-ttu-id="59202-122">El **método IMsgServiceAdmin::MsgServiceTransportOrder** establece el orden de entrega de los proveedores de transporte en un perfil.</span><span class="sxs-lookup"><span data-stu-id="59202-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="59202-123">El parámetro _lpUIDList_ debe contener una lista ordenada de identificadores de entrada del proveedor de transporte obtenidos **de** la propiedad PR_PROVIDER_UID ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la tabla devuelta desde el método [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="59202-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="59202-124">Una aplicación cliente debe pasar la lista completa  _en lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="59202-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="59202-125">**SetTransportOrder** invalida las preferencias del proveedor de transporte, como la marca STATUS_XP_PREFER_LAST establecida en **la propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59202-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59202-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="59202-126">See also</span></span>



[<span data-ttu-id="59202-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="59202-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="59202-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59202-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

