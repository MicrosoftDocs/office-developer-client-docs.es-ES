---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4e2d4f76fe436fd18b439bbbb558b1169094b438
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589465"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="9f158-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="9f158-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="9f158-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f158-105">Establece una carpeta como destino de los mensajes entrantes de una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="9f158-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="9f158-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f158-106">Parameters</span></span>

 <span data-ttu-id="9f158-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="9f158-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="9f158-108">[entrada] Un puntero a la clase de mensaje es que se asociará con la nueva carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="9f158-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="9f158-109">Si el parámetro _lpszMessageClass_ se establece en NULL o una cadena vacía, **SetReceiveFolder** conjuntos de carpeta para el almacén de mensajes de recepción la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9f158-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="9f158-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f158-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9f158-111">[entrada] Una máscara de bits de indicadores que controla el tipo del texto en las cadenas que se pasan en.</span><span class="sxs-lookup"><span data-stu-id="9f158-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="9f158-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f158-112">The following flag can be set:</span></span>
    
<span data-ttu-id="9f158-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f158-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9f158-114">La cadena de la clase de mensaje está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9f158-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="9f158-115">Si no está establecido el indicador MAPI_UNICODE., la cadena de la clase de mensaje está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9f158-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="9f158-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9f158-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="9f158-117">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9f158-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9f158-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9f158-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="9f158-119">[entrada] Un puntero al identificador de entrada de la carpeta que se va a establecer como la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="9f158-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="9f158-120">Si el parámetro _lpEntryID_ se establece en NULL, **SetReceiveFolder** reemplaza la recepción de la actual carpeta con predeterminado del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f158-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f158-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f158-121">Return value</span></span>

<span data-ttu-id="9f158-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f158-122">S_OK</span></span> 
  
> <span data-ttu-id="9f158-123">Una carpeta de recepción se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="9f158-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f158-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f158-124">Remarks</span></span>

<span data-ttu-id="9f158-125">El método **IMsgStore::SetReceiveFolder** establece o cambia la carpeta de recepción para una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="9f158-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="9f158-126">Con **SetReceiveFolder**, un cliente puede, mediante llamadas sucesivas, especificar una diferentes recibir carpeta para cada clase de mensaje definido o especificar que los mensajes entrantes para todas las clases de mensaje varios van a la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f158-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="9f158-127">Por ejemplo, un cliente puede tener su propia clase de mensajes entran en su propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f158-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="9f158-128">Una aplicación de fax puede designar una carpeta en la que el proveedor de almacenamiento coloca los faxes entrantes y otra carpeta en la que el proveedor coloca los faxes salientes.</span><span class="sxs-lookup"><span data-stu-id="9f158-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="9f158-129">Si se produce un error durante la llamada a **SetReceiveFolder**, la configuración de la carpeta de recepción permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="9f158-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="9f158-130">Si cambia de **SetReceiveFolder** la configuración de la carpeta de recepción con _lpEntryID_ establecido en NULL, que indica que se debe establecer la carpeta de recepción predeterminada, **SetReceiveFolder** devuelve S_OK incluso si se ha producido ningún valor existente para el indicado clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f158-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f158-131">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9f158-131">MFCMAPI reference</span></span>

<span data-ttu-id="9f158-132">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9f158-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f158-133">**File**</span><span class="sxs-lookup"><span data-stu-id="9f158-133">**File**</span></span>|<span data-ttu-id="9f158-134">**Función**</span><span class="sxs-lookup"><span data-stu-id="9f158-134">**Function**</span></span>|<span data-ttu-id="9f158-135">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9f158-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f158-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9f158-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9f158-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="9f158-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="9f158-138">MFCMAPI usa el método **IMsgStore::SetReceiveFolder** para establecer una carpeta como la carpeta de recepción para una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="9f158-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f158-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f158-139">See also</span></span>



[<span data-ttu-id="9f158-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9f158-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="9f158-141">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9f158-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

