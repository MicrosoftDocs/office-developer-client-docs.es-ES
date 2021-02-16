---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422764"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="575fe-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="575fe-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="575fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="575fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="575fe-105">Devuelve un puntero que proporciona acceso a un objeto de administración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="575fe-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="575fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="575fe-106">Parameters</span></span>

 <span data-ttu-id="575fe-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="575fe-107">_lpUID_</span></span>
  
> <span data-ttu-id="575fe-108">[entrada] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a administrar.</span><span class="sxs-lookup"><span data-stu-id="575fe-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="575fe-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="575fe-109">_ulFlags_</span></span>
  
> <span data-ttu-id="575fe-110">[entrada] Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="575fe-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="575fe-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="575fe-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="575fe-112">[salida] Puntero a un puntero a un objeto de administración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="575fe-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="575fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="575fe-113">Return value</span></span>

<span data-ttu-id="575fe-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="575fe-114">S_OK</span></span> 
  
> <span data-ttu-id="575fe-115">El objeto de administración del proveedor se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="575fe-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="575fe-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="575fe-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="575fe-117">El **MAPIUID** al que apunta  _lpUID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="575fe-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="575fe-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="575fe-118">Remarks</span></span>

<span data-ttu-id="575fe-119">El **método IMsgServiceAdmin::AdminProviders** proporciona acceso a un objeto de administración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="575fe-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="575fe-120">Una administración de proveedores es un objeto que admite la [interfaz IProviderAdmin](iprovideradminiunknown.md) y permite a los clientes hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="575fe-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="575fe-121">Agregar proveedores de servicios a un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="575fe-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="575fe-122">Eliminar proveedores de servicios de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="575fe-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="575fe-123">Abra las secciones de perfil.</span><span class="sxs-lookup"><span data-stu-id="575fe-123">Open profile sections.</span></span>
    
- <span data-ttu-id="575fe-124">Obtener acceso a la tabla del proveedor de servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="575fe-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="575fe-125">Los tipos de cambios que se pueden realizar realmente en un servicio de mensajes mientras el perfil está en uso dependen del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="575fe-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="575fe-126">Sin embargo, la mayoría de los servicios de mensajes no admiten cambios como agregar y eliminar proveedores mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="575fe-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="575fe-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="575fe-127">Notes to callers</span></span>

<span data-ttu-id="575fe-128">Para recuperar la estructura **MAPIUID** para el servicio de mensajes que se va a administrar, recupere la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="575fe-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="575fe-129">Para obtener más información, vea el procedimiento descrito en el [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="575fe-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="575fe-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="575fe-130">MFCMAPI reference</span></span>

<span data-ttu-id="575fe-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="575fe-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="575fe-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="575fe-132">**File**</span></span>|<span data-ttu-id="575fe-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="575fe-133">**Function**</span></span>|<span data-ttu-id="575fe-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="575fe-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="575fe-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="575fe-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="575fe-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="575fe-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="575fe-137">MFCMAPI usa el **método IMsgServiceAdmin::AdminProviders** para abrir un objeto de administración de proveedor para un servicio.</span><span class="sxs-lookup"><span data-stu-id="575fe-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="575fe-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="575fe-138">See also</span></span>



[<span data-ttu-id="575fe-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="575fe-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="575fe-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="575fe-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="575fe-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="575fe-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="575fe-142">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="575fe-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

