---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587848"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="1bbde-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="1bbde-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="1bbde-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bbde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bbde-105">Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="1bbde-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1bbde-106">Parameters</span></span>

 <span data-ttu-id="1bbde-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1bbde-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1bbde-108">[entrada] Una máscara de bits de indicadores que controla la configuración del almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="1bbde-109">Estas marcas son mutuamente excluyentes; se puede establecer solo uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1bbde-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="1bbde-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="1bbde-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="1bbde-111">Establece el almacén de mensajes como el valor predeterminado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="1bbde-112">Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1bbde-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="1bbde-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1bbde-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="1bbde-114">Establece el almacén de mensajes como el almacén que se usará en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="1bbde-115">Si el almacén de mensajes no es el almacén de forma predeterminada, los clientes hacen que el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="1bbde-116">Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_PRIMARY_STORE en la columna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="1bbde-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="1bbde-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1bbde-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="1bbde-118">Establece el almacén de mensajes como el almacén que se usará en el inicio de sesión si el almacén de mensajes principal no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1bbde-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="1bbde-119">Si un cliente no puede abrir el almacén principal, debe abrir el almacén de secundario y establecer como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="1bbde-120">Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_SECONDARY_STORE en la columna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="1bbde-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="1bbde-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="1bbde-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="1bbde-122">Establece la marca STATUS_SIMPLE_STORE en propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en su fila de tabla de estado, fila de la tabla de almacenamiento de mensajes y en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="1bbde-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="1bbde-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="1bbde-124">Establece la marca STATUS_SIMPLE_STORE en propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en su fila de la tabla de estado y la fila de tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1bbde-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="1bbde-125">No se modificó el perfil.</span><span class="sxs-lookup"><span data-stu-id="1bbde-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="1bbde-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1bbde-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="1bbde-127">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1bbde-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1bbde-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1bbde-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="1bbde-129">[entrada] Un puntero al identificador de entrada del almacén de mensajes que se ha diseñado como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="1bbde-130">Si un cliente pasa NULL en _lpEntryID_, no se selecciona ningún almacén de mensajes como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1bbde-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bbde-131">Return value</span></span>

<span data-ttu-id="1bbde-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bbde-132">S_OK</span></span> 
  
> <span data-ttu-id="1bbde-133">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1bbde-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bbde-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1bbde-134">Remarks</span></span>

<span data-ttu-id="1bbde-135">El método **IMAPISession::SetDefaultStore** establece un almacén de mensajes como una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="1bbde-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="1bbde-136">El almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="1bbde-137">El almacén de mensajes principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="1bbde-138">El almacén de mensajes secundario para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="1bbde-139">Para establecer un almacén de mensajes como el valor predeterminado, el almacén de mensajes debe tener las siguientes marcas establecer en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="1bbde-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="1bbde-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="1bbde-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="1bbde-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="1bbde-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="1bbde-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="1bbde-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1bbde-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1bbde-143">Notes to callers</span></span>

<span data-ttu-id="1bbde-144">Puede determinar el almacén de mensajes predeterminado para la sesión al recuperar la tabla de estado y busca el valor de la marca STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="1bbde-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="1bbde-145">La fila que tiene esta opción representa el almacén de mensajes que se designa como el valor predeterminado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1bbde-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="1bbde-146">Cuando se establece la MAPI_DEFAULT_STORE o la marca MAPI_SIMPLE_STORE_PERMANENT, MAPI actualiza el perfil, tabla de almacén de mensajes y tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="1bbde-147">Cada vez que se realiza un cambio a la configuración predeterminada de almacén de mensajes, se generan las notificaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1bbde-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="1bbde-148">Se emite una notificación de evento **fnevTableModified** para cada fila afectada en ambas en la tabla de almacenamiento y el estado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1bbde-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="1bbde-149">Se emite una notificación interna a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1bbde-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="1bbde-150">Operaciones en curso se completan sin cambio; nuevas operaciones relacionadas con el almacén de mensajes de forma predeterminada, como una descarga el mensaje, se procesan para el nuevo almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1bbde-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1bbde-151">MFCMAPI reference</span></span>

<span data-ttu-id="1bbde-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1bbde-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1bbde-153">**File**</span><span class="sxs-lookup"><span data-stu-id="1bbde-153">**File**</span></span>|<span data-ttu-id="1bbde-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="1bbde-154">**Function**</span></span>|<span data-ttu-id="1bbde-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1bbde-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1bbde-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1bbde-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1bbde-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="1bbde-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="1bbde-158">MFCMAPI usa el método **IMAPISession::SetDefaultStore** para establecer el almacén seleccionado como el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1bbde-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bbde-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bbde-159">See also</span></span>



[<span data-ttu-id="1bbde-160">Propiedad canónico PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="1bbde-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="1bbde-161">Propiedad canónico PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="1bbde-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="1bbde-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1bbde-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1bbde-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1bbde-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1bbde-164">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1bbde-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

