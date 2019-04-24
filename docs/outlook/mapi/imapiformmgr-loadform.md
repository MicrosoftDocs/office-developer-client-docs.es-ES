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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321701"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="4dba5-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="4dba5-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="4dba5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dba5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dba5-105">Inicia un formulario para abrir un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="4dba5-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4dba5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4dba5-106">Parameters</span></span>

 <span data-ttu-id="4dba5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4dba5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4dba5-108">a Identificador de la ventana primaria del indicador de progreso que se muestra mientras se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="4dba5-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="4dba5-109">El parámetro _ulUIParam_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4dba5-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4dba5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4dba5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4dba5-111">a Máscara de máscara de marcadores que controla cómo se abre el formulario.</span><span class="sxs-lookup"><span data-stu-id="4dba5-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="4dba5-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4dba5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="4dba5-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4dba5-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4dba5-114">Muestra una interfaz de usuario para proporcionar el estado o solicitar información al usuario.</span><span class="sxs-lookup"><span data-stu-id="4dba5-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="4dba5-115">Si no se establece esta marca, no se muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4dba5-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="4dba5-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="4dba5-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="4dba5-117">Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="4dba5-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="4dba5-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4dba5-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="4dba5-119">a Un puntero a una cadena que da nombre a la clase de mensaje del mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="4dba5-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="4dba5-120">Si se pasa NULL en el parámetro _lpszMessageClass_ , la clase de mensaje se determina a partir del mensaje al que señala el parámetro _PMSG_ .</span><span class="sxs-lookup"><span data-stu-id="4dba5-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="4dba5-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4dba5-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4dba5-122">a Una máscara de bits de marcas definidas por el cliente o por el proveedor que se copian de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje que proporciona información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="4dba5-123">El parámetro _ulMessageStatus_ debe establecerse si _LPSZMESSAGECLASS_ no es null; de lo contrario, se omite _ulMessageStatus_ .</span><span class="sxs-lookup"><span data-stu-id="4dba5-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="4dba5-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4dba5-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4dba5-125">a Un puntero a una máscara de máscara de marcas copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="4dba5-126">El parámetro _ulMessageFlags_ debe establecerse si _LPSZMESSAGECLASS_ no es null; de lo contrario, se omite _ulMessageFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4dba5-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="4dba5-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="4dba5-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="4dba5-128">a Un puntero a la carpeta que contiene directamente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="4dba5-129">El parámetro _pFolderFocus_ puede ser null si no existe una carpeta de este tipo (por ejemplo, si el mensaje está incrustado en otro mensaje).</span><span class="sxs-lookup"><span data-stu-id="4dba5-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="4dba5-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4dba5-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="4dba5-131">a Un puntero al sitio del mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="4dba5-132">_PMSG_</span><span class="sxs-lookup"><span data-stu-id="4dba5-132">_pmsg_</span></span>
  
> <span data-ttu-id="4dba5-133">a Un puntero al mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="4dba5-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="4dba5-134">_pViewContext_</span></span>
  
> <span data-ttu-id="4dba5-135">a Un puntero al contexto de la vista para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="4dba5-136">El parámetro _pViewContext_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="4dba5-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="4dba5-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="4dba5-137">_riid_</span></span>
  
> <span data-ttu-id="4dba5-138">a Identificador de interfaz (IID) de la interfaz que se va a usar para el objeto de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="4dba5-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="4dba5-139">El parámetro _riid_ no debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="4dba5-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="4dba5-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="4dba5-140">_ppvObj_</span></span>
  
> <span data-ttu-id="4dba5-141">contempla Un puntero a un puntero a la interfaz devuelta.</span><span class="sxs-lookup"><span data-stu-id="4dba5-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4dba5-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dba5-142">Return value</span></span>

<span data-ttu-id="4dba5-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="4dba5-143">S_OK</span></span> 
  
> <span data-ttu-id="4dba5-144">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4dba5-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4dba5-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="4dba5-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="4dba5-146">El formulario no es compatible con la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="4dba5-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="4dba5-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4dba5-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4dba5-148">La clase de mensaje pasada en _lpszMessageClass_ no coincide con la clase de mensaje de ningún formulario de la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="4dba5-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4dba5-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4dba5-149">Remarks</span></span>

<span data-ttu-id="4dba5-150">Los visores de formularios llaman al método **IMAPIFormMgr:: LoadForm** para abrir un formulario de un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="4dba5-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="4dba5-151">**LoadForm** abre el objeto Form, carga el mensaje en el objeto de formulario, configura el contexto de vista apropiado, si es necesario, y devuelve la interfaz solicitada para el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="4dba5-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="4dba5-152">El parámetro _pFolderFocus_ apunta a la carpeta que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dba5-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="4dba5-153">Si el mensaje está incrustado en otro mensaje, _pFolderFocus_ debe ser null.</span><span class="sxs-lookup"><span data-stu-id="4dba5-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4dba5-154">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4dba5-154">Notes to implementers</span></span>

<span data-ttu-id="4dba5-155">Si se pasa NULL en _lpszMessageClass_, la implementación obtiene la clase de mensaje, el estado y las marcas del mensaje del **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** y \*\*PR_MESSAGE_FLAGS \*\*propiedades.</span><span class="sxs-lookup"><span data-stu-id="4dba5-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="4dba5-156">Si se proporciona una cadena de clase de mensaje en _lpszMessageClass_, la implementación debe usar los valores de _ulMessageStatus_ y _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="4dba5-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4dba5-157">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4dba5-157">MFCMAPI reference</span></span>

<span data-ttu-id="4dba5-158">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4dba5-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4dba5-159">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4dba5-159">**File**</span></span>|<span data-ttu-id="4dba5-160">**Función**</span><span class="sxs-lookup"><span data-stu-id="4dba5-160">**Function**</span></span>|<span data-ttu-id="4dba5-161">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4dba5-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4dba5-162">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="4dba5-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4dba5-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="4dba5-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="4dba5-164">MFCMAPI usa el método **IMAPIFormMgr:: LoadForm** para cargar un formulario antes de mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="4dba5-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4dba5-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dba5-165">See also</span></span>



[<span data-ttu-id="4dba5-166">Propiedad canónica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="4dba5-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="4dba5-167">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="4dba5-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="4dba5-168">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4dba5-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="4dba5-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4dba5-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="4dba5-170">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4dba5-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

