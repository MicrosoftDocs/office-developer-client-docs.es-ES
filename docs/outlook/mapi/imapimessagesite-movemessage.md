---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321369"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="19a33-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="19a33-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="19a33-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19a33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19a33-105">Mueve el mensaje actual a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="19a33-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="19a33-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="19a33-106">Parameters</span></span>

 <span data-ttu-id="19a33-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="19a33-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="19a33-108">a Un puntero a la carpeta a la que se moverá el mensaje.</span><span class="sxs-lookup"><span data-stu-id="19a33-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="19a33-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="19a33-109">_pViewContext_</span></span>
  
> <span data-ttu-id="19a33-110">a Un puntero a un objeto de contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="19a33-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="19a33-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="19a33-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="19a33-112">a Un puntero a una estructura [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contiene el tamaño y la posición de la ventana del formulario actual.</span><span class="sxs-lookup"><span data-stu-id="19a33-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="19a33-113">El siguiente formulario que se muestra también usa este rectángulo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="19a33-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19a33-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19a33-114">Return value</span></span>

<span data-ttu-id="19a33-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="19a33-115">S_OK</span></span> 
  
> <span data-ttu-id="19a33-116">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="19a33-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="19a33-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="19a33-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="19a33-118">La operación no es compatible con este sitio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="19a33-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19a33-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19a33-119">Remarks</span></span>

<span data-ttu-id="19a33-120">Los objetos de formulario llaman al método **IMAPIMessageSite:: MoveMessage** para mover el mensaje actual a una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="19a33-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="19a33-121">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="19a33-121">Notes to implementers</span></span>

<span data-ttu-id="19a33-122">La implementación de **MoveMessage** del visor de formularios debe llamar al método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) , pasando la marca VCDIR_MOVE, antes de mover el mensaje a una carpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="19a33-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="19a33-123">Para obtener la estructura **Rect** que utiliza la ventana de un formulario, llame a la función [GetWindowRect](https://msdn.microsoft.com/library/ms633519) de Windows.</span><span class="sxs-lookup"><span data-stu-id="19a33-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="19a33-124">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="19a33-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="19a33-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="19a33-125">Notes to callers</span></span>

<span data-ttu-id="19a33-126">Tras la devolución de **MoveMessage**, los formularios deben comprobar si hay un mensaje actual y, a continuación, descartarse si no hay ninguno.</span><span class="sxs-lookup"><span data-stu-id="19a33-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="19a33-127">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="19a33-127">MFCMAPI reference</span></span>

<span data-ttu-id="19a33-128">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="19a33-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="19a33-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="19a33-129">**File**</span></span>|<span data-ttu-id="19a33-130">**Función**</span><span class="sxs-lookup"><span data-stu-id="19a33-130">**Function**</span></span>|<span data-ttu-id="19a33-131">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="19a33-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19a33-132">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="19a33-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="19a33-133">CMyMAPIFormViewer:: MoveMessage</span><span class="sxs-lookup"><span data-stu-id="19a33-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="19a33-134">No implementado.</span><span class="sxs-lookup"><span data-stu-id="19a33-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19a33-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="19a33-135">See also</span></span>



[<span data-ttu-id="19a33-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="19a33-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="19a33-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19a33-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="19a33-138">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="19a33-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="19a33-139">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="19a33-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

