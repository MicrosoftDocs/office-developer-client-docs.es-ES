---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583186"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="133c4-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="133c4-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="133c4-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="133c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="133c4-105">Administra el registro de un formulario para recibir las notificaciones sobre cambios en el Visor.</span><span class="sxs-lookup"><span data-stu-id="133c4-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="133c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="133c4-106">Parameters</span></span>

 <span data-ttu-id="133c4-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="133c4-107">_pmvns_</span></span>
  
> <span data-ttu-id="133c4-108">[entrada] Puntero a un formulario de aviso objeto receptor o NULL.</span><span class="sxs-lookup"><span data-stu-id="133c4-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="133c4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="133c4-109">Return value</span></span>

<span data-ttu-id="133c4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="133c4-110">S_OK</span></span> 
  
> <span data-ttu-id="133c4-111">El registro o la cancelación de la notificación de formulario que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="133c4-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="133c4-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="133c4-112">Remarks</span></span>

<span data-ttu-id="133c4-113">Objetos de formulario llame al método de **IMAPIViewContext::SetAdviseSink** a cualquier registro para obtener información acerca de los cambios en el Visor de formulario o cancelar un registro previo.</span><span class="sxs-lookup"><span data-stu-id="133c4-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="133c4-114">Cuando _pmvns_ se establece en NULL, el formulario desea cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="133c4-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="133c4-115">Cuando los puntos de _pmvns_ a un formulario válido de aviso receptor, el formulario desea registrar para las notificaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="133c4-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="133c4-116">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="133c4-116">Notes to implementers</span></span>

<span data-ttu-id="133c4-117">Cuando **SetAdviseSink** incluye un formulario de aviso puntero receptor, mantener una referencia a él hasta que se realiza otra llamada **SetAdviseSink** para cancelar la notificación.</span><span class="sxs-lookup"><span data-stu-id="133c4-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="133c4-118">Enviar una notificación cuando se produce un cambio en el Visor y cuando se carga un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="133c4-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="133c4-119">Para obtener más información, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="133c4-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="133c4-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="133c4-120">MFCMAPI reference</span></span>

<span data-ttu-id="133c4-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="133c4-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="133c4-122">**File**</span><span class="sxs-lookup"><span data-stu-id="133c4-122">**File**</span></span>|<span data-ttu-id="133c4-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="133c4-123">**Function**</span></span>|<span data-ttu-id="133c4-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="133c4-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="133c4-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="133c4-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="133c4-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="133c4-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="133c4-127">MFCMAPI implementa el método **IMAPIViewContext::SetAdviseSink** en esta función.</span><span class="sxs-lookup"><span data-stu-id="133c4-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="133c4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="133c4-128">See also</span></span>



[<span data-ttu-id="133c4-129">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="133c4-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

