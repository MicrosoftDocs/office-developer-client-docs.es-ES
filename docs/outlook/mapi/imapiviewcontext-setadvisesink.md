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
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351194"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="b57a9-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b57a9-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="b57a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b57a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b57a9-105">Administra el registro de un formulario para recibir notificaciones sobre cambios en el visor.</span><span class="sxs-lookup"><span data-stu-id="b57a9-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="b57a9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b57a9-106">Parameters</span></span>

 <span data-ttu-id="b57a9-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="b57a9-107">_pmvns_</span></span>
  
> <span data-ttu-id="b57a9-108">a Puntero a un objeto receptor de notificaciones de formulario o NULL.</span><span class="sxs-lookup"><span data-stu-id="b57a9-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b57a9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b57a9-109">Return value</span></span>

<span data-ttu-id="b57a9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b57a9-110">S_OK</span></span> 
  
> <span data-ttu-id="b57a9-111">El registro o la cancelación de la notificación del formulario se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b57a9-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b57a9-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b57a9-112">Remarks</span></span>

<span data-ttu-id="b57a9-113">Los objetos de formulario llaman al método **IMAPIViewContext:: SetAdviseSink** para registrarse para obtener información sobre los cambios en el visor de formularios o cancelar un registro anterior.</span><span class="sxs-lookup"><span data-stu-id="b57a9-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="b57a9-114">Cuando _pmvns_ se establece en null, el formulario desea cancelar un registro.</span><span class="sxs-lookup"><span data-stu-id="b57a9-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="b57a9-115">Cuando _pmvns_ apunta a un receptor de formulario válido, el formulario desea registrarse para notificaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="b57a9-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b57a9-116">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="b57a9-116">Notes to implementers</span></span>

<span data-ttu-id="b57a9-117">Cuando **SetAdviseSink** incluye un puntero para notificar al receptor, mantenga una referencia al mismo hasta que se realice otra llamada a **SetAdviseSink** para cancelar la notificación.</span><span class="sxs-lookup"><span data-stu-id="b57a9-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="b57a9-118">Envíe una notificación cuando se produzca un cambio en el visor y cuando cargue un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="b57a9-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="b57a9-119">Para obtener más información, consulte [enviar y recibir notificaCiones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b57a9-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b57a9-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b57a9-120">MFCMAPI reference</span></span>

<span data-ttu-id="b57a9-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b57a9-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b57a9-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b57a9-122">**File**</span></span>|<span data-ttu-id="b57a9-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="b57a9-123">**Function**</span></span>|<span data-ttu-id="b57a9-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b57a9-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b57a9-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="b57a9-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b57a9-126">CMyMAPIFormViewer:: SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b57a9-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="b57a9-127">MFCMAPI implementa el método **IMAPIViewContext:: SetAdviseSink** en esta función.</span><span class="sxs-lookup"><span data-stu-id="b57a9-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b57a9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b57a9-128">See also</span></span>



[<span data-ttu-id="b57a9-129">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b57a9-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

