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
ms.openlocfilehash: 2a09731dbd0ba2c5d6c1055a7c5ed11097c5ef27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817616"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="ad7cc-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="ad7cc-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="ad7cc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad7cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad7cc-105">Se notifica al Visor de formulario que se está cerrando un formulario.</span><span class="sxs-lookup"><span data-stu-id="ad7cc-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="ad7cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad7cc-106">Parameters</span></span>

<span data-ttu-id="ad7cc-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ad7cc-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ad7cc-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad7cc-108">Return value</span></span>

<span data-ttu-id="ad7cc-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad7cc-109">S_OK</span></span> 
  
> <span data-ttu-id="ad7cc-110">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad7cc-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad7cc-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad7cc-111">Remarks</span></span>

<span data-ttu-id="ad7cc-112">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ad7cc-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad7cc-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad7cc-113">See also</span></span>



[<span data-ttu-id="ad7cc-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad7cc-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

