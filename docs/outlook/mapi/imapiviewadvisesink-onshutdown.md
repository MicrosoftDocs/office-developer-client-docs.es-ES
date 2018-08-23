---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592972"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="e7341-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="e7341-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="e7341-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7341-105">Se notifica al Visor de formulario que se está cerrando un formulario.</span><span class="sxs-lookup"><span data-stu-id="e7341-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="e7341-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7341-106">Parameters</span></span>

<span data-ttu-id="e7341-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e7341-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e7341-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7341-108">Return value</span></span>

<span data-ttu-id="e7341-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7341-109">S_OK</span></span> 
  
> <span data-ttu-id="e7341-110">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e7341-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7341-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7341-111">Remarks</span></span>

<span data-ttu-id="e7341-112">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e7341-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7341-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e7341-113">See also</span></span>



[<span data-ttu-id="e7341-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7341-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

