---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817303"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="09d51-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="09d51-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="09d51-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09d51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09d51-105">Inicia un formulario para abrir un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="09d51-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="09d51-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09d51-106">Parameters</span></span>

 <span data-ttu-id="09d51-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="09d51-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="09d51-108">[entrada] Identificador de la ventana principal del indicador de progreso que se muestra mientras se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="09d51-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="09d51-109">El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="09d51-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="09d51-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09d51-110">_ulFlags_</span></span>
  
> <span data-ttu-id="09d51-111">[entrada] Una máscara de bits de indicadores que controla cómo se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="09d51-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="09d51-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="09d51-112">The following flags can be set:</span></span>
    
<span data-ttu-id="09d51-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="09d51-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="09d51-114">Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="09d51-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="09d51-115">Si no se establece este marcador, no se muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="09d51-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="09d51-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="09d51-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="09d51-117">Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="09d51-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="09d51-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="09d51-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="09d51-119">[entrada] Un puntero a una cadena que da nombre a la clase de mensaje del mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="09d51-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="09d51-120">Si se pasa NULL en el parámetro _lpszMessageClass_ , se determina la clase de mensaje del mensaje indicada por el parámetro _pmsg_ .</span><span class="sxs-lookup"><span data-stu-id="09d51-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="09d51-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="09d51-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="09d51-122">[entrada] Una máscara de bits de definidas por el cliente o definidas por el proveedor de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje que proporciona información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="09d51-123">El parámetro _ulMessageStatus_ debe establecerse si _lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageStatus_ .</span><span class="sxs-lookup"><span data-stu-id="09d51-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="09d51-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="09d51-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="09d51-125">[entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="09d51-126">El parámetro _ulMessageFlags_ debe establecerse si _lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageFlags_ .</span><span class="sxs-lookup"><span data-stu-id="09d51-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="09d51-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="09d51-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="09d51-128">[entrada] Un puntero a la carpeta que contiene directamente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="09d51-129">El parámetro _pFolderFocus_ puede ser NULL si no existe como una carpeta (por ejemplo, si el mensaje está incrustado en otro mensaje).</span><span class="sxs-lookup"><span data-stu-id="09d51-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="09d51-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="09d51-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="09d51-131">[entrada] Un puntero al sitio de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="09d51-132">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="09d51-132">_pmsg_</span></span>
  
> <span data-ttu-id="09d51-133">[entrada] Un puntero al mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="09d51-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="09d51-134">_pViewContext_</span></span>
  
> <span data-ttu-id="09d51-135">[entrada] Un puntero al contexto de vista para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="09d51-136">El parámetro _pViewContext_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="09d51-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="09d51-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="09d51-137">_riid_</span></span>
  
> <span data-ttu-id="09d51-138">[entrada] El identificador de interfaz (IID) de la interfaz que se usará para el objeto de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="09d51-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="09d51-139">El parámetro _riid_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="09d51-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="09d51-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="09d51-140">_ppvObj_</span></span>
  
> <span data-ttu-id="09d51-141">[out] Un puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="09d51-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09d51-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09d51-142">Return value</span></span>

<span data-ttu-id="09d51-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="09d51-143">S_OK</span></span> 
  
> <span data-ttu-id="09d51-144">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="09d51-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="09d51-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="09d51-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="09d51-146">El formulario no es compatible con la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="09d51-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="09d51-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="09d51-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="09d51-148">La clase de mensaje que se pasó _lpszMessageClass_ no coincide con la clase de mensaje para cualquier formulario en la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="09d51-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09d51-149">Notas</span><span class="sxs-lookup"><span data-stu-id="09d51-149">Remarks</span></span>

<span data-ttu-id="09d51-150">Visores de formulario llamar al método **IMAPIFormMgr::LoadForm** para abrir un formulario para un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="09d51-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="09d51-151">**LoadForm** abre el objeto de formulario, se carga el mensaje en el objeto de formulario, se configura el contexto de vista apropiada, si es necesario y se devuelve la interfaz solicitada para el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="09d51-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="09d51-152">El parámetro _pFolderFocus_ apunta a la carpeta que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d51-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="09d51-153">Si el mensaje está incrustado en otro mensaje, _pFolderFocus_ debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="09d51-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="09d51-154">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="09d51-154">Notes to implementers</span></span>

<span data-ttu-id="09d51-155">Si se pasa NULL en _lpszMessageClass_, la implementación obtiene la clase de mensaje del mensaje, estado y los indicadores desde el mensaje **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** y **PR_MESSAGE_FLAGS **propiedades.</span><span class="sxs-lookup"><span data-stu-id="09d51-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="09d51-156">Si se proporciona una cadena de la clase de mensaje en _lpszMessageClass_, la implementación debe usar los valores de _ulMessageStatus_ y _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="09d51-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09d51-157">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09d51-157">MFCMAPI reference</span></span>

<span data-ttu-id="09d51-158">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="09d51-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09d51-159">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="09d51-159">**File**</span></span>|<span data-ttu-id="09d51-160">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="09d51-160">**Function**</span></span>|<span data-ttu-id="09d51-161">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="09d51-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09d51-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="09d51-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="09d51-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="09d51-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="09d51-164">MFCMAPI usa el método **IMAPIFormMgr::LoadForm** para cargar un formulario antes de mostrarla.</span><span class="sxs-lookup"><span data-stu-id="09d51-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09d51-165">Ver también</span><span class="sxs-lookup"><span data-stu-id="09d51-165">See also</span></span>



[<span data-ttu-id="09d51-166">Propiedad canónico PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="09d51-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="09d51-167">Propiedad canónico PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="09d51-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="09d51-168">Propiedad canónico PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="09d51-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="09d51-169">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="09d51-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="09d51-170">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="09d51-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

