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
ms.openlocfilehash: 1c48ceefa84658b236b8dfa4e10df18c175d920e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595163"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="be321-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="be321-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="be321-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be321-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be321-105">Crea un objeto de soporte técnico del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="be321-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="be321-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="be321-106">Parameters</span></span>

 <span data-ttu-id="be321-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be321-107">_ulFlags_</span></span>
  
> <span data-ttu-id="be321-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="be321-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="be321-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="be321-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="be321-110">[out] Un puntero a un puntero al nuevo objeto de soporte técnico de servicio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="be321-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be321-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be321-111">Return value</span></span>

<span data-ttu-id="be321-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="be321-112">S_OK</span></span> 
  
> <span data-ttu-id="be321-113">Se ha creado correctamente el objeto de configuración de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="be321-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be321-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be321-114">Remarks</span></span>

<span data-ttu-id="be321-115">El método **IMAPISupport::GetSvcConfigSupportObj** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="be321-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="be321-116">Proveedores de servicios de llamar a **GetSvcConfigSupportObj** para crear un objeto de soporte técnico de configuración que se pase a una función de punto de entrada de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="be321-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="be321-117">Una función de punto de entrada de servicio de mensajes se basa en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) y se llama a los métodos de la interfaz [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="be321-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="be321-118">Una función de punto de entrada de servicio de mensajes permite servicios de mensajes configurar ellos mismos o realizar otras acciones cuando se cambia el perfil.</span><span class="sxs-lookup"><span data-stu-id="be321-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="be321-119">Punto de entrada de servicio de mensaje funciones pueden admitir los cambios de configuración mediante la presentación de una hoja de propiedades o a través de una matriz de valores de propiedad que se pasa al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="be321-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be321-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="be321-120">See also</span></span>



[<span data-ttu-id="be321-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be321-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="be321-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="be321-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="be321-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="be321-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="be321-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be321-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="be321-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="be321-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="be321-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="be321-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

