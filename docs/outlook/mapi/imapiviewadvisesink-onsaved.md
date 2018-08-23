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
ms.openlocfilehash: 1ae94b40d984adee0f3c888f69dfdbffb1e352e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584439"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="2bd84-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="2bd84-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="2bd84-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bd84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bd84-105">Se notifica el Visor de formulario que se ha guardado el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="2bd84-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="2bd84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bd84-106">Parameters</span></span>

<span data-ttu-id="2bd84-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2bd84-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2bd84-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bd84-108">Return value</span></span>

<span data-ttu-id="2bd84-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="2bd84-109">S_OK</span></span> 
  
> <span data-ttu-id="2bd84-110">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="2bd84-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2bd84-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bd84-111">Remarks</span></span>

<span data-ttu-id="2bd84-112">Un objeto de formulario llama al método de **IMAPIViewAdviseSink::OnSaved** después de que se ha guardado correctamente el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="2bd84-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="2bd84-113">Al hacerlo, permite que los visores puedan actualizar sus windows para reflejar los cambios realizados en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="2bd84-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="2bd84-114">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="2bd84-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2bd84-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2bd84-115">See also</span></span>



[<span data-ttu-id="2bd84-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2bd84-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

