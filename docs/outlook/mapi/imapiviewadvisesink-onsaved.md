---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817626"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="cb995-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="cb995-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="cb995-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb995-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb995-105">Se notifica el Visor de formulario que se ha guardado el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="cb995-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="cb995-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb995-106">Parameters</span></span>

<span data-ttu-id="cb995-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cb995-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="cb995-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb995-108">Return value</span></span>

<span data-ttu-id="cb995-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb995-109">S_OK</span></span> 
  
> <span data-ttu-id="cb995-110">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="cb995-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb995-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb995-111">Remarks</span></span>

<span data-ttu-id="cb995-112">Un objeto de formulario llama al método de **IMAPIViewAdviseSink::OnSaved** después de que se ha guardado correctamente el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="cb995-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="cb995-113">Al hacerlo, permite que los visores puedan actualizar sus windows para reflejar los cambios realizados en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cb995-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="cb995-114">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="cb995-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb995-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb995-115">See also</span></span>



[<span data-ttu-id="cb995-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb995-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

