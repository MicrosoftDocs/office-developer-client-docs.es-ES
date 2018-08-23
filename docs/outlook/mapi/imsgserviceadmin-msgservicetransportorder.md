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
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570796"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="095cb-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="095cb-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="095cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="095cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="095cb-105">Establece el orden en que transporte se denominan proveedores para entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="095cb-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="095cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="095cb-106">Parameters</span></span>

 <span data-ttu-id="095cb-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="095cb-107">_cUID_</span></span>
  
> <span data-ttu-id="095cb-108">[entrada] El recuento de identificadores únicos en el parámetro _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="095cb-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="095cb-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="095cb-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="095cb-110">[entrada] Un puntero a una matriz de identificadores únicos que representan los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="095cb-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="095cb-111">La matriz contiene un identificador para cada proveedor de transporte configurado en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="095cb-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="095cb-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="095cb-112">_ulFlags_</span></span>
  
> <span data-ttu-id="095cb-113">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="095cb-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="095cb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="095cb-114">Return value</span></span>

<span data-ttu-id="095cb-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="095cb-115">S_OK</span></span> 
  
> <span data-ttu-id="095cb-116">Se estableció correctamente en el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="095cb-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="095cb-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="095cb-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="095cb-118">El valor en el parámetro _cUID_ difiere del número de proveedores de transporte realmente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="095cb-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="095cb-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="095cb-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="095cb-120">Una o varias de las estructuras [MAPIUID](mapiuid.md) que se pasa en el parámetro _lpUIDList_ no hacen referencia a un proveedor de transporte que están actualmente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="095cb-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="095cb-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="095cb-121">Remarks</span></span>

<span data-ttu-id="095cb-122">El método **IMsgServiceAdmin::MsgServiceTransportOrder** establece el orden de entrega de los proveedores de transporte en un perfil.</span><span class="sxs-lookup"><span data-stu-id="095cb-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="095cb-123">El parámetro _lpUIDList_ debe contener una lista ordenada de los identificadores de entrada de proveedor de transporte obtenido de la propiedad **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la tabla devuelta desde el [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) (método).</span><span class="sxs-lookup"><span data-stu-id="095cb-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="095cb-124">Una aplicación de cliente debe pasar la lista completa de _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="095cb-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="095cb-125">**SetTransportOrder** invalidaciones de transporte preferencias de proveedor como la marca STATUS_XP_PREFER_LAST establecida en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="095cb-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="095cb-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="095cb-126">See also</span></span>



[<span data-ttu-id="095cb-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="095cb-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="095cb-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="095cb-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

