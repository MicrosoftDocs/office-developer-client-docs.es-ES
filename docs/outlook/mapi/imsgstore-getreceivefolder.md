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
ms.openlocfilehash: a8cd211cc16b620ac47357271070e0b45b867bea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579945"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="f4c9d-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="f4c9d-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="f4c9d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4c9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4c9d-105">Obtiene la carpeta que se estableció como el destino para los mensajes entrantes de una clase de mensaje especificado o como el valor predeterminado de recepción carpeta para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="f4c9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4c9d-106">Parameters</span></span>

 <span data-ttu-id="f4c9d-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="f4c9d-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="f4c9d-108">[entrada] Un puntero a una clase de mensaje que está asociada con una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="f4c9d-109">Si el parámetro _lpszMessageClass_ se establece en NULL o una cadena vacía, **GetReceiveFolder** devuelve el valor predeterminado recibir carpeta para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="f4c9d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4c9d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f4c9d-111">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas en el pasado y devueltos.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="f4c9d-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="f4c9d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f4c9d-113">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f4c9d-114">La cadena de la clase de mensaje está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="f4c9d-115">Si no está establecido el indicador MAPI_UNICODE., la cadena de la clase de mensaje está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="f4c9d-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4c9d-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="f4c9d-117">[out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f4c9d-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f4c9d-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4c9d-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="f4c9d-119">[out] Un puntero a un puntero al identificador de entrada para el solicitado recibir carpeta.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="f4c9d-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="f4c9d-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="f4c9d-121">[out] Un puntero a un puntero a la clase de mensaje que se establezca explícitamente como su carpeta la carpeta indicada por _lppEntryID_de recepción.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="f4c9d-122">Esta clase de mensaje debe ser la misma que la clase en el parámetro _lpszMessageClass_ , o una clase de la clase base.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="f4c9d-123">Paso de NULL indica que la carpeta indicada por _lppEntryID_ es el valor predeterminado recibir carpeta para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4c9d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4c9d-124">Return value</span></span>

<span data-ttu-id="f4c9d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4c9d-125">S_OK</span></span> 
  
> <span data-ttu-id="f4c9d-126">La carpeta de recepción se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4c9d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4c9d-127">Remarks</span></span>

<span data-ttu-id="f4c9d-128">El método **IMsgStore::GetReceiveFolder** Obtiene el identificador de entrada de una carpeta de recepción, una carpeta designada para recibir los mensajes entrantes de una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="f4c9d-129">Los autores de llamadas pueden especificar una clase de mensaje o NULL en el parámetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="f4c9d-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="f4c9d-130">Si _lpszMessageClass_ es NULL, **GetReceiveFolder** devuelve los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f4c9d-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="f4c9d-131">En _lppszExplicitClass_, el nombre de la clase base inicial de la clase de mensaje que apunta _lpszMessageClass_ que establecer explícitamente una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="f4c9d-132">En _lppEntryID_, el identificador de entrada de la carpeta de recepción de la clase base indicada por el parámetro _lppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="f4c9d-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="f4c9d-133">Por ejemplo, supongamos que la carpeta de recepción de la clase de mensaje IPM **. Nota** se ha establecido para la entrada de identificador de la Bandeja de entrada y **GetReceiveFolder** se denomina con el contenido de _lpszMessageClass_ establecido en **IPM. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="f4c9d-134">Si **IPM. Note.Phone** no haya explícita recibe conjunto de carpetas, **GetReceiveFolder** devuelve el identificador de entrada de la Bandeja de entrada de _lppEntryID_ y **IPM. Nota** en _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="f4c9d-135">Si el cliente llama a **GetReceiveFolder** para una clase de mensaje y no ha establecido una carpeta de recepción para esa clase de mensaje, _lppszExplicitClass_ es una cadena de longitud cero, una cadena en formato Unicode o una cadena en formato ANSI dependiendo de si el cliente establecer el indicador MAPI_UNICODE en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="f4c9d-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="f4c9d-136">Un valor predeterminado recibir carpeta, obtenido por pasando NULL en el parámetro _lpszMessageClass_ , siempre existe para cada almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="f4c9d-137">Un cliente debe llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando se realiza con el identificador de entrada que se devuelven en _lppEntryID_ para liberar la memoria que contiene ese identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="f4c9d-138">También debe llamar **MAPIFreeBuffer** cuando se hace con la cadena de la clase de mensaje devuelta en _lppszExplicitClass_ para liberar la memoria que contiene dicha cadena.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4c9d-139">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f4c9d-139">MFCMAPI reference</span></span>

<span data-ttu-id="f4c9d-140">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4c9d-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f4c9d-141">**File**</span></span>|<span data-ttu-id="f4c9d-142">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="f4c9d-142">**Function**</span></span>|<span data-ttu-id="f4c9d-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f4c9d-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4c9d-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f4c9d-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f4c9d-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="f4c9d-145">GetInbox</span></span>  <br/> |<span data-ttu-id="f4c9d-146">MFCMAPI usa el método **IMsgStore::GetReceiveFolder** para buscar la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4c9d-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4c9d-147">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f4c9d-147">See also</span></span>



[<span data-ttu-id="f4c9d-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f4c9d-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f4c9d-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4c9d-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="f4c9d-150">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="f4c9d-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

