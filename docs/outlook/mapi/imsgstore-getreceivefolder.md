---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435351"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="36f46-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="36f46-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="36f46-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36f46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36f46-105">Obtiene la carpeta que se estableció como destino para los mensajes entrantes de una clase de mensaje especificada o como la carpeta de recepción predeterminada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="36f46-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="36f46-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="36f46-106">Parameters</span></span>

 <span data-ttu-id="36f46-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="36f46-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="36f46-108">a Un puntero a una clase de mensaje que está asociado a una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="36f46-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="36f46-109">Si el parámetro _lpszMessageClass_ está establecido en null o una cadena vacía, **GetReceiveFolder** devuelve la carpeta de recepción predeterminada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="36f46-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="36f46-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36f46-110">_ulFlags_</span></span>
  
> <span data-ttu-id="36f46-111">a Máscara de bits de marcadores que controla el tipo de las cadenas que se han pasado y se han devuelto.</span><span class="sxs-lookup"><span data-stu-id="36f46-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="36f46-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="36f46-112">The following flag can be set:</span></span>
    
<span data-ttu-id="36f46-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36f46-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36f46-114">La cadena de clase de mensaje está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="36f46-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="36f46-115">Si no se establece la marca MAPI_UNICODE, la cadena de clase de mensaje está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="36f46-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="36f46-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="36f46-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="36f46-117">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="36f46-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="36f46-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="36f46-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="36f46-119">contempla Un puntero a un puntero al identificador de entrada de la carpeta de recepción solicitada.</span><span class="sxs-lookup"><span data-stu-id="36f46-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="36f46-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="36f46-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="36f46-121">contempla Un puntero a un puntero a la clase de mensaje que establece explícitamente como su carpeta de recepción la carpeta a la que apunta _lppEntryID_.</span><span class="sxs-lookup"><span data-stu-id="36f46-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="36f46-122">Esta clase de mensaje debe ser la misma que la clase en el parámetro _lpszMessageClass_ o una clase base de dicha clase.</span><span class="sxs-lookup"><span data-stu-id="36f46-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="36f46-123">Si se pasa NULL, indica que la carpeta a la que apunta _lppEntryID_ es la carpeta de recepción predeterminada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="36f46-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36f46-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36f46-124">Return value</span></span>

<span data-ttu-id="36f46-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="36f46-125">S_OK</span></span> 
  
> <span data-ttu-id="36f46-126">La carpeta de recepción se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="36f46-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36f46-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36f46-127">Remarks</span></span>

<span data-ttu-id="36f46-128">El método **IMsgStore:: GetReceiveFolder** obtiene el identificador de entrada de una carpeta de recepción, una carpeta designada para recibir los mensajes entrantes de una clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="36f46-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="36f46-129">Los autores de llamadas pueden especificar una clase de mensaje o NULL en el parámetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="36f46-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="36f46-130">Si _lpszMessageClass_ es null, **GetReceiveFolder** devuelve los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="36f46-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="36f46-131">En _lppszExplicitClass_, el nombre de la primera clase base de la clase de mensaje a la que apunta _lpszMessageClass_ que hace que se establezca explícitamente una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="36f46-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="36f46-132">En _lppEntryID_, el identificador de entrada de la carpeta de recepción para la clase base apuntado por el parámetro _lppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="36f46-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="36f46-133">Por ejemplo, supongamos que la carpeta de recepción de la clase de mensaje **IPM. Note** se ha establecido en el identificador de entrada de la bandeja de entrada y se llama a **GetReceiveFolder** con el contenido de _lpszMessageClass_ establecido en **IPM. Note. Phone**.</span><span class="sxs-lookup"><span data-stu-id="36f46-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="36f46-134">Si se trata de **IPM. Note. Phone** no tiene un conjunto de carpetas de recepción explícito, **GetReceiveFolder** devuelve el identificador de entrada de la bandeja de entrada en _lppEntryID_ e **IPM. Nota** en _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="36f46-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="36f46-135">Si el cliente llama a **GetReceiveFolder** para una clase de mensaje y no ha establecido una carpeta de recepción para la clase de mensaje, _lppszExplicitClass_ es una cadena de longitud cero, una cadena en formato Unicode o una cadena en formato ANSI, en función de si el el cliente estableció la marca MAPI_UNICODE en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="36f46-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="36f46-136">Siempre existe una carpeta de recepción predeterminada, obtenida pasando un valor NULL en el parámetro _lpszMessageClass_ , para cada almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="36f46-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="36f46-137">Un cliente debe llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando se realiza con el identificador de entrada devuelto en _lppEntryID_ para liberar la memoria que contiene el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="36f46-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="36f46-138">También debe llamar a **MAPIFreeBuffer** cuando se ha realizado con la cadena de clase de mensaje devuelta en _lppszExplicitClass_ para liberar la memoria que contiene esa cadena.</span><span class="sxs-lookup"><span data-stu-id="36f46-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36f46-139">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36f46-139">MFCMAPI reference</span></span>

<span data-ttu-id="36f46-140">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="36f46-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36f46-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="36f46-141">**File**</span></span>|<span data-ttu-id="36f46-142">**Función**</span><span class="sxs-lookup"><span data-stu-id="36f46-142">**Function**</span></span>|<span data-ttu-id="36f46-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="36f46-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36f46-144">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="36f46-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="36f46-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="36f46-145">GetInbox</span></span>  <br/> |<span data-ttu-id="36f46-146">MFCMAPI usa el método **IMsgStore:: GetReceiveFolder** para localizar la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="36f46-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36f46-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="36f46-147">See also</span></span>



[<span data-ttu-id="36f46-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="36f46-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="36f46-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="36f46-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="36f46-150">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="36f46-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

