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
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351166"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="9ada6-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="9ada6-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="9ada6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ada6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ada6-105">Notifica al visor de formularios que se va a cerrar un formulario.</span><span class="sxs-lookup"><span data-stu-id="9ada6-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="9ada6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ada6-106">Parameters</span></span>

<span data-ttu-id="9ada6-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9ada6-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9ada6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ada6-108">Return value</span></span>

<span data-ttu-id="9ada6-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ada6-109">S_OK</span></span> 
  
> <span data-ttu-id="9ada6-110">La notificación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ada6-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ada6-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ada6-111">Remarks</span></span>

<span data-ttu-id="9ada6-112">Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="9ada6-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ada6-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ada6-113">See also</span></span>



[<span data-ttu-id="9ada6-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ada6-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

