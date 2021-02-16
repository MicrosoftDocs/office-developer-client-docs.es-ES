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
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426110"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="1847b-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="1847b-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="1847b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1847b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1847b-105">Establece un almacén de mensajes como almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="1847b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1847b-106">Parameters</span></span>

 <span data-ttu-id="1847b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1847b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1847b-108">[entrada] Máscara de bits de marcas que controla la configuración del almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="1847b-109">Estas marcas son mutuamente excluyentes; solo se puede establecer una de las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1847b-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="1847b-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="1847b-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="1847b-111">Establece el almacén de mensajes como valor predeterminado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="1847b-112">Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo la marca STATUS_DEFAULT_STORE en la **columna PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1847b-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="1847b-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1847b-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="1847b-114">Establece el almacén de mensajes como almacén que se usará durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="1847b-115">Si el almacén de mensajes no es el almacén predeterminado, los clientes deben hacerlo el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="1847b-116">Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo la STATUS_PRIMARY_STORE en la **PR_RESOURCE_FLAGS** mensaje.</span><span class="sxs-lookup"><span data-stu-id="1847b-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="1847b-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1847b-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="1847b-118">Establece el almacén de mensajes como almacén que se usará durante el inicio de sesión si el almacén de mensajes principal no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1847b-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="1847b-119">Si un cliente no puede abrir el almacén principal, debe abrir el almacén secundario y establecerlo como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="1847b-120">Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo el indicador STATUS_SECONDARY_STORE en la **PR_RESOURCE_FLAGS** mensaje.</span><span class="sxs-lookup"><span data-stu-id="1847b-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="1847b-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="1847b-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="1847b-122">Establece el STATUS_SIMPLE_STORE en la propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en su fila de tabla de estado, fila de tabla del almacén de mensajes y en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="1847b-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="1847b-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="1847b-124">Establece la marca STATUS_SIMPLE_STORE en la  propiedad PR_RESOURCE_FLAGS del almacén de mensajes en su fila de tabla de estado y en la fila de la tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1847b-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="1847b-125">El perfil no se modifica.</span><span class="sxs-lookup"><span data-stu-id="1847b-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="1847b-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1847b-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="1847b-127">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="1847b-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1847b-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1847b-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="1847b-129">[entrada] Puntero al identificador de entrada del almacén de mensajes que está previsto como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="1847b-130">Si un cliente pasa NULL en  _lpEntryID,_ no se selecciona ningún almacén de mensajes como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1847b-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1847b-131">Return value</span></span>

<span data-ttu-id="1847b-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1847b-132">S_OK</span></span> 
  
> <span data-ttu-id="1847b-133">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1847b-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1847b-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1847b-134">Remarks</span></span>

<span data-ttu-id="1847b-135">El **método IMAPISession::SetDefaultStore** establece un almacén de mensajes como uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1847b-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="1847b-136">Almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="1847b-137">El almacén de mensajes principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="1847b-138">Almacén de mensajes secundario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="1847b-139">Para establecer un almacén de mensajes como predeterminado, el almacén de mensajes debe tener las siguientes marcas establecidas en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="1847b-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="1847b-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="1847b-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="1847b-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="1847b-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="1847b-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="1847b-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1847b-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1847b-143">Notes to callers</span></span>

<span data-ttu-id="1847b-144">Puede determinar el almacén de mensajes predeterminado para la sesión recuperando la tabla de estado y buscando la configuración de la marca STATUS_DEFAULT_STORE en la **PR_RESOURCE_FLAGS** columna.</span><span class="sxs-lookup"><span data-stu-id="1847b-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="1847b-145">La fila que tiene esta configuración representa el almacén de mensajes designado como predeterminado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1847b-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="1847b-146">Cuando se establece MAPI_DEFAULT_STORE o la marca MAPI_SIMPLE_STORE_PERMANENT, MAPI actualiza el perfil, la tabla del almacén de mensajes y la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="1847b-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="1847b-147">Cada vez que se realiza un cambio en la configuración predeterminada del almacén de mensajes, se generan las siguientes notificaciones:</span><span class="sxs-lookup"><span data-stu-id="1847b-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="1847b-148">Se **emite una notificación de evento fnevTableModified** para cada fila afectada tanto en el almacén de mensajes como en la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="1847b-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="1847b-149">Se emite una notificación interna a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1847b-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="1847b-150">Las operaciones que ya están en curso se completan sin cambios; Las nuevas operaciones que implican el almacén de mensajes predeterminado, como la descarga de mensajes, se procesan para el nuevo almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1847b-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1847b-151">MFCMAPI reference</span></span>

<span data-ttu-id="1847b-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1847b-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1847b-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1847b-153">**File**</span></span>|<span data-ttu-id="1847b-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="1847b-154">**Function**</span></span>|<span data-ttu-id="1847b-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1847b-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1847b-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1847b-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1847b-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="1847b-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="1847b-158">MFCMAPI usa el **método IMAPISession::SetDefaultStore** para establecer el almacén seleccionado como almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1847b-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1847b-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1847b-159">See also</span></span>



[<span data-ttu-id="1847b-160">Propiedad canónica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="1847b-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="1847b-161">Propiedad canónica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="1847b-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="1847b-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1847b-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1847b-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1847b-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1847b-164">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1847b-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

