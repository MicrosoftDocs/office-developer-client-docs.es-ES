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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316561"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="75903-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="75903-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="75903-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75903-105">Crea un objeto de compatibilidad del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="75903-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="75903-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="75903-106">Parameters</span></span>

 <span data-ttu-id="75903-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75903-107">_ulFlags_</span></span>
  
> <span data-ttu-id="75903-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="75903-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="75903-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="75903-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="75903-110">contempla Un puntero a un puntero al nuevo objeto de compatibilidad con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="75903-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75903-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75903-111">Return value</span></span>

<span data-ttu-id="75903-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="75903-112">S_OK</span></span> 
  
> <span data-ttu-id="75903-113">El objeto de compatibilidad de configuración se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="75903-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75903-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75903-114">Remarks</span></span>

<span data-ttu-id="75903-115">El método **IMAPISupport:: GetSvcConfigSupportObj** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="75903-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="75903-116">Los proveedores de servicios llaman a **GetSvcConfigSupportObj** para crear un objeto de compatibilidad de configuración para pasar a una función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="75903-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="75903-117">Una función de punto de entrada del servicio de mensajes se basa en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) y es llamada por los métodos de la interfaz [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="75903-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="75903-118">Una función de punto de entrada del servicio de mensajes permite a los servicios de mensaje configurarse a sí mismos o realizar otras acciones cuando se cambia el perfil.</span><span class="sxs-lookup"><span data-stu-id="75903-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="75903-119">Las funciones del punto de entrada del servicio de mensajes pueden admitir los cambios de configuración mostrando una hoja de propiedades o a través de una matriz de valores de propiedad que se pasa al método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="75903-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75903-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="75903-120">See also</span></span>



[<span data-ttu-id="75903-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75903-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="75903-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="75903-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="75903-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="75903-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="75903-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75903-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="75903-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="75903-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="75903-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="75903-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

