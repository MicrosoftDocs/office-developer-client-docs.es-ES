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
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407609"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="be7fe-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="be7fe-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="be7fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be7fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be7fe-105">Notifica al visor de formularios que se ha guardado el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="be7fe-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="be7fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be7fe-106">Parameters</span></span>

<span data-ttu-id="be7fe-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="be7fe-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="be7fe-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be7fe-108">Return value</span></span>

<span data-ttu-id="be7fe-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="be7fe-109">S_OK</span></span> 
  
> <span data-ttu-id="be7fe-110">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="be7fe-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be7fe-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be7fe-111">Remarks</span></span>

<span data-ttu-id="be7fe-112">Un objeto Form llama al método **IMAPIViewAdviseSink:: onSave** después de que se haya guardado correctamente el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="be7fe-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="be7fe-113">Esto permite a los visores actualizar sus ventanas para reflejar los cambios realizados en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="be7fe-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="be7fe-114">Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="be7fe-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be7fe-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="be7fe-115">See also</span></span>



[<span data-ttu-id="be7fe-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be7fe-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

