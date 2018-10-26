---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586168"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="90516-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="90516-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="90516-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90516-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90516-105">Se abre un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="90516-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90516-106">Parameters</span></span>

 <span data-ttu-id="90516-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="90516-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="90516-108">[entrada] Identificador de la ventana principal para el indicador de progreso que se muestra mientras se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="90516-109">El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="90516-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="90516-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="90516-110">_ulFlags_</span></span>
  
> <span data-ttu-id="90516-111">[entrada] Una máscara de bits de indicadores que controla cómo se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="90516-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="90516-112">The following flag can be set:</span></span>
    
<span data-ttu-id="90516-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="90516-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="90516-114">Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="90516-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="90516-115">Si no se establece este marcador, no se muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="90516-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="90516-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="90516-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="90516-117">[entrada] Un puntero al objeto de información de formulario que se usa para abrir el formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="90516-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="90516-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="90516-119">[entrada] Un puntero para el identificador de interfaz (IID) para la interfaz que se devolverá para el objeto de formulario que se creó.</span><span class="sxs-lookup"><span data-stu-id="90516-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="90516-120">El parámetro _refiidToAsk_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="90516-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="90516-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="90516-121">_ppvObj_</span></span>
  
> <span data-ttu-id="90516-122">[out] Un puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="90516-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90516-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90516-123">Return value</span></span>

<span data-ttu-id="90516-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="90516-124">S_OK</span></span> 
  
> <span data-ttu-id="90516-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="90516-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="90516-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="90516-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="90516-127">No se admite la interfaz solicitada por el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90516-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90516-128">Remarks</span></span>

<span data-ttu-id="90516-129">Visores de formulario llamar al método **IMAPIFormMgr::CreateForm** para abrir un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="90516-130">**CreateForm** abre el formulario mediante la creación de una instancia del servidor de formulario para ese formulario tal como se describe en el objeto de información de formulario determinado.</span><span class="sxs-lookup"><span data-stu-id="90516-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="90516-131">Si es necesario, **CreateForm** llama al método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) para descargar el código de servidor del formulario en el disco del usuario.</span><span class="sxs-lookup"><span data-stu-id="90516-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="90516-132">El parámetro _pfrminfoToActivate_ debe apuntar a un objeto de información de formulario que se ha resuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="90516-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="90516-133">Después de que se ha abierto el formulario, el Visor de formulario llamada debe configurar un mensaje mediante la interfaz de [IPersistMessage](ipersistmessageiunknown.md) y, opcionalmente, puede configurar un contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="90516-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="90516-134">Para obtener más información, vea [iniciar un servidor de formulario](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="90516-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="90516-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="90516-135">MFCMAPI reference</span></span>

<span data-ttu-id="90516-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="90516-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="90516-137">**File**</span><span class="sxs-lookup"><span data-stu-id="90516-137">**File**</span></span>|<span data-ttu-id="90516-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="90516-138">**Function**</span></span>|<span data-ttu-id="90516-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="90516-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90516-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="90516-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="90516-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="90516-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="90516-142">MFCMAPI usa el método **IMAPIFormMgr::CreateForm** para crear un formulario antes de mostrarla.</span><span class="sxs-lookup"><span data-stu-id="90516-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90516-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="90516-143">See also</span></span>



[<span data-ttu-id="90516-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="90516-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="90516-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90516-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="90516-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90516-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="90516-147">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="90516-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="90516-148">Iniciar un servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="90516-148">Launching a Form Server</span></span>](launching-a-form-server.md)

