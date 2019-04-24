---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317286"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="51143-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51143-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="51143-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51143-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51143-105">Abre un objeto Folder o Message y devuelve un puntero al objeto para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="51143-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="51143-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="51143-106">Parameters</span></span>

 <span data-ttu-id="51143-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="51143-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="51143-108">a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="51143-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="51143-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="51143-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="51143-110">a Un puntero a la dirección del identificador de entrada de la carpeta o del objeto de mensaje que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="51143-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="51143-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="51143-111">_lpInterface_</span></span>
  
> <span data-ttu-id="51143-112">a Un puntero al identificador de interfaz (IID) para el objeto.</span><span class="sxs-lookup"><span data-stu-id="51143-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="51143-113">Si se pasa NULL, indica que el objeto se convierte en la interfaz estándar para este tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="51143-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="51143-114">El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto.</span><span class="sxs-lookup"><span data-stu-id="51143-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="51143-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="51143-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="51143-116">a Máscara de máscara de marcadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="51143-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="51143-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="51143-117">The following flags can be set:</span></span>
    
<span data-ttu-id="51143-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51143-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="51143-119">El objeto debe abrirse con los permisos máximos permitidos para el usuario y los permisos máximos de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="51143-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="51143-120">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto se abre con el permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto se abre con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="51143-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="51143-121">El cliente puede recuperar el nivel de permisos al obtener la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="51143-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="51143-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="51143-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="51143-123">La llamada puede tener éxito incluso si el objeto subyacente no está disponible para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="51143-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="51143-124">Si el objeto no está disponible, una llamada subsiguiente al objeto puede devolver un error.</span><span class="sxs-lookup"><span data-stu-id="51143-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="51143-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="51143-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="51143-126">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51143-126">Requests read/write permission.</span></span> <span data-ttu-id="51143-127">De forma predeterminada, los objetos se crean con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51143-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="51143-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="51143-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="51143-129">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="51143-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="51143-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="51143-130">_lppUnk_</span></span>
  
> <span data-ttu-id="51143-131">contempla Un puntero al puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="51143-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51143-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51143-132">Return value</span></span>

<span data-ttu-id="51143-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="51143-133">S_OK</span></span> 
  
> <span data-ttu-id="51143-134">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="51143-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51143-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51143-135">Remarks</span></span>

<span data-ttu-id="51143-136">MAPI llama al método **IMSLogon:: OpenEntry** para abrir una carpeta o un mensaje en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="51143-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="51143-137">MAPI pasa el identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="51143-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="51143-138">El proveedor de almacenamiento de mensajes debe devolver un puntero que permita obtener más acceso al objeto especificado en el parámetro _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="51143-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="51143-139">Antes de que MAPI llame a **IMSLogon:: OpenEntry**, primero determina que el identificador de entrada de mensajes o carpetas especificado coincida con uno registrado por este proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="51143-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="51143-140">Para obtener más información sobre cómo los proveedores de almacenamiento registran identificadores de entrada, vea [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="51143-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="51143-141">**IMSLogon:: OpenEntry** es idéntico al método [IMsgStore:: OpenEntry](imsgstore-openentry.md) del objeto de almacén de mensajes, excepto que el cliente no llama a **IMSLogon:: OpenEntry**; MAPI llama a **IMSLogon:: OpenEntry** cuando procesa un método **IMAPISession:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="51143-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="51143-142">Los objetos abiertos mediante **IMSLogon:: OpenEntry** deben tratarse exactamente de la misma forma que los objetos abiertos mediante el objeto de almacén de mensajes; en concreto, los objetos abiertos mediante esta llamada deben invalidarse cuando se libere el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="51143-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51143-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="51143-143">See also</span></span>



[<span data-ttu-id="51143-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="51143-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="51143-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51143-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="51143-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51143-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

