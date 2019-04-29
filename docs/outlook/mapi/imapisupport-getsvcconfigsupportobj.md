---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411312"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="80f54-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="80f54-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="80f54-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80f54-105">Crea un objeto de compatibilidad del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="80f54-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="80f54-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="80f54-106">Parameters</span></span>

 <span data-ttu-id="80f54-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80f54-107">_ulFlags_</span></span>
  
> <span data-ttu-id="80f54-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="80f54-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="80f54-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="80f54-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="80f54-110">contempla Un puntero a un puntero al nuevo objeto de compatibilidad con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="80f54-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80f54-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80f54-111">Return value</span></span>

<span data-ttu-id="80f54-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="80f54-112">S_OK</span></span> 
  
> <span data-ttu-id="80f54-113">El objeto de compatibilidad de configuración se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="80f54-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80f54-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80f54-114">Remarks</span></span>

<span data-ttu-id="80f54-115">El método **IMAPISupport:: GetSvcConfigSupportObj** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="80f54-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="80f54-116">Los proveedores de servicios llaman a **GetSvcConfigSupportObj** para crear un objeto de compatibilidad de configuración para pasar a una función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="80f54-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="80f54-117">Una función de punto de entrada del servicio de mensajes se basa en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) y es llamada por los métodos de la interfaz [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="80f54-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="80f54-118">Una función de punto de entrada del servicio de mensajes permite a los servicios de mensaje configurarse a sí mismos o realizar otras acciones cuando se cambia el perfil.</span><span class="sxs-lookup"><span data-stu-id="80f54-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="80f54-119">Las funciones del punto de entrada del servicio de mensajes pueden admitir los cambios de configuración mostrando una hoja de propiedades o a través de una matriz de valores de propiedad que se pasa al método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="80f54-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80f54-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="80f54-120">See also</span></span>



[<span data-ttu-id="80f54-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80f54-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="80f54-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="80f54-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="80f54-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="80f54-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="80f54-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80f54-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="80f54-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="80f54-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="80f54-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="80f54-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

