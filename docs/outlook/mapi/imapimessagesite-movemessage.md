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
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817351"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="c4144-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="c4144-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="c4144-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4144-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4144-105">Mueve el mensaje actual a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4144-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="c4144-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4144-106">Parameters</span></span>

 <span data-ttu-id="c4144-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="c4144-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="c4144-108">[entrada] Un puntero a la carpeta donde el mensaje se va a mover.</span><span class="sxs-lookup"><span data-stu-id="c4144-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="c4144-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="c4144-109">_pViewContext_</span></span>
  
> <span data-ttu-id="c4144-110">[entrada] Un puntero a un objeto de contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="c4144-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="c4144-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="c4144-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="c4144-112">[entrada] Un puntero a una estructura de [rectángulo](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contiene el tamaño de la ventana y la posición del formulario actual.</span><span class="sxs-lookup"><span data-stu-id="c4144-112">[in] A pointer to a [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="c4144-113">El siguiente formulario que muestra también usa este rectángulo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c4144-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c4144-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4144-114">Return value</span></span>

<span data-ttu-id="c4144-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4144-115">S_OK</span></span> 
  
> <span data-ttu-id="c4144-116">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c4144-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c4144-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c4144-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c4144-118">La operación no es compatible con este sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4144-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4144-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4144-119">Remarks</span></span>

<span data-ttu-id="c4144-120">Objetos de formulario llamar al método **IMAPIMessageSite::MoveMessage** para mover el mensaje actual a una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="c4144-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c4144-121">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="c4144-121">Notes to implementers</span></span>

<span data-ttu-id="c4144-122">Implementación del Visor de un formulario de **MoveMessage** debe llamar al método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , que se pasa el indicador VCDIR_MOVE, antes de mover realmente el mensaje a una carpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="c4144-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="c4144-123">Para obtener la estructura de **rectángulo** usada por la ventana de un formulario, llame a la función de Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="c4144-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="c4144-124">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c4144-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c4144-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c4144-125">Notes to callers</span></span>

<span data-ttu-id="c4144-126">Después de la devolución de **MoveMessage**, formularios deben comprobar si un mensaje actual y descartar a sí mismos si no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4144-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c4144-127">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c4144-127">MFCMAPI reference</span></span>

<span data-ttu-id="c4144-128">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c4144-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c4144-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c4144-129">**File**</span></span>|<span data-ttu-id="c4144-130">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="c4144-130">**Function**</span></span>|<span data-ttu-id="c4144-131">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c4144-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4144-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c4144-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c4144-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="c4144-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="c4144-134">No se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="c4144-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4144-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4144-135">See also</span></span>



[<span data-ttu-id="c4144-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c4144-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="c4144-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4144-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c4144-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c4144-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c4144-139">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="c4144-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)
