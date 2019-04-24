---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335696"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="a0487-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="a0487-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="a0487-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0487-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0487-105">Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a0487-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0487-106">Parameters</span></span>

 <span data-ttu-id="a0487-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a0487-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="a0487-108">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a0487-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a0487-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="a0487-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="a0487-110">contempla Un puntero a un puntero al identificador de entrada del objeto que proporciona la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="a0487-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0487-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0487-111">Return value</span></span>

<span data-ttu-id="a0487-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0487-112">S_OK</span></span> 
  
> <span data-ttu-id="a0487-113">La identidad principal se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0487-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="a0487-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="a0487-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="a0487-115">La llamada se realizó correctamente, pero no hay una identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="a0487-116">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="a0487-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a0487-117">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="a0487-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a0487-118">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a0487-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0487-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0487-119">Remarks</span></span>

<span data-ttu-id="a0487-120">El método **IMAPISession:: QueryIdentity** recupera la identidad principal para la sesión actual y devuelve el valor mediante el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a0487-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="a0487-121">La identidad principal es un objeto, normalmente un usuario de mensajería, que representa al usuario de una sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="a0487-122">_lppEntryID_ devuelve la identidad principal de un objeto [IMailUser](imailuserimapiprop.md) , que también se almacena como la propiedad [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a0487-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="a0487-123">Puede usar el valor devuelto en _lppEntryID_ para abrir un objeto **IMailUser** mediante [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="a0487-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="a0487-124">Aunque muchos proveedores de servicios de varios servicios de mensajes pueden proporcionar la identidad principal para una sesión, MAPI designa a un solo proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a0487-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="a0487-125">El proveedor de servicios que proporciona la identidad principal establece los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a0487-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="a0487-126">La marca STATUS_PRIMARY_IDENTITY en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a0487-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="a0487-127">La propiedad **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a0487-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="a0487-128">La propiedad **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a0487-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="a0487-129">La propiedad **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a0487-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="a0487-130">Si el proveedor de servicios que proporciona la identidad principal pertenece a un servicio de mensajes, los demás proveedores de servicios del servicio de mensajes también establecen las propiedades de PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="a0487-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="a0487-131">Estas propiedades se publican en la tabla de estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="a0487-132">Si es posible, **QueryIdentity** devuelve el valor de la propiedad **PR_IDENTITY_ENTRYID** de la fila status etiquetada con STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="a0487-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="a0487-133">Si falta la propiedad **PR_IDENTITY_ENTRYID** de la fila de identidad principal, **QueryIdentity** devuelve un identificador de entrada único creado con otra información de esa fila.</span><span class="sxs-lookup"><span data-stu-id="a0487-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="a0487-134">Si falta la marca STATUS_PRIMARY_IDENTITY en todas las columnas **PR_RESOURCE_FLAG** de la tabla de estado, **QueryIdentity** devuelve el primer identificador de entrada que encuentra.</span><span class="sxs-lookup"><span data-stu-id="a0487-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="a0487-135">Cuando no hay ningún identificador de entrada adecuado para devolver, **QueryIdentity** se ejecuta correctamente con el MAPI_W_NO_SERVICE de advertencia y apunta _lppEntryID_ a un identificador de entrada codificado de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="a0487-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0487-136">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a0487-136">Notes to callers</span></span>

<span data-ttu-id="a0487-137">Puede llamar al método [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para asignar a un servicio de mensajes la tarea de proporcionar la identidad principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="a0487-138">Otra forma de recuperar la identidad principal consiste en buscar en la tabla de Estados la fila con las columnas **PR_RESOURCE_FLAGS** establecida en STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="a0487-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="a0487-139">Para obtener más información acerca de esta forma alternativa de recuperar información de identidad, consulte [TABLE status and status Objects](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a0487-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="a0487-140">Cuando termine de usar el identificador de entrada de la identidad principal devuelta por **QueryIdentity**, libere la memoria mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a0487-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a0487-141">Para obtener más información acerca de la identidad en general, consulte [identidad principal de MAPI](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="a0487-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="a0487-142">Para obtener más información acerca de la recuperación de la identidad de la sesión MAPI, consulte recuperación de la [identidad principal y del proveedor](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="a0487-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0487-143">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a0487-143">MFCMAPI reference</span></span>

<span data-ttu-id="a0487-144">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a0487-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0487-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a0487-145">**File**</span></span>|<span data-ttu-id="a0487-146">**Función**</span><span class="sxs-lookup"><span data-stu-id="a0487-146">**Function**</span></span>|<span data-ttu-id="a0487-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a0487-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0487-148">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a0487-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a0487-149">CMainDlg:: OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="a0487-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="a0487-150">MFCMAPI usa el método **IMAPISession:: QueryIdentity** para abrir la entrada de la libreta de direcciones para la identidad principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a0487-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0487-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0487-151">See also</span></span>



[<span data-ttu-id="a0487-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a0487-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="a0487-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="a0487-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="a0487-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a0487-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a0487-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0487-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a0487-156">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="a0487-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a0487-157">Identidad principal MAPI</span><span class="sxs-lookup"><span data-stu-id="a0487-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="a0487-158">Recuperación de la identidad principal y del proveedor</span><span class="sxs-lookup"><span data-stu-id="a0487-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="a0487-159">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="a0487-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="a0487-160">Tabla de estado y objetos de estado</span><span class="sxs-lookup"><span data-stu-id="a0487-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

