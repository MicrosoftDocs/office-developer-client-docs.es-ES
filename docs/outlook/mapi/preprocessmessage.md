---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437248"
---
# <a name="preprocessmessage"></a><span data-ttu-id="e8453-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="e8453-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="e8453-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8453-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8453-105">Define una función que preprocesa el contenido del mensaje o el formato de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8453-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8453-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e8453-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8453-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e8453-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e8453-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="e8453-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e8453-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e8453-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="e8453-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="e8453-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e8453-111">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="e8453-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="e8453-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8453-112">Parameters</span></span>

 <span data-ttu-id="e8453-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="e8453-113">_lpvSession_</span></span>
  
> <span data-ttu-id="e8453-114">[entrada] Puntero a la sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e8453-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="e8453-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e8453-115">_lpMessage_</span></span>
  
> <span data-ttu-id="e8453-116">[entrada] Puntero al mensaje que se va a preprocesar.</span><span class="sxs-lookup"><span data-stu-id="e8453-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="e8453-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="e8453-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="e8453-118">[entrada] Puntero a la libreta de direcciones desde la que el usuario debe seleccionar destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8453-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="e8453-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="e8453-119">_lpFolder_</span></span>
  
> <span data-ttu-id="e8453-120">[entrada, salida] Puntero a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e8453-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="e8453-121">En la entrada, el  _parámetro lpFolder_ apunta a la carpeta que contiene los mensajes que se deben preprocesar.</span><span class="sxs-lookup"><span data-stu-id="e8453-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="e8453-122">En el resultado,  _lpFolder_ apunta a la carpeta donde se han colocado los mensajes preprocesados.</span><span class="sxs-lookup"><span data-stu-id="e8453-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="e8453-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e8453-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e8453-124">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="e8453-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e8453-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e8453-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e8453-126">[entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e8453-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="e8453-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e8453-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e8453-128">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="e8453-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e8453-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="e8453-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="e8453-130">[salida] Puntero al número de mensajes de la matriz a los que apunta el _parámetro lpppMessage._</span><span class="sxs-lookup"><span data-stu-id="e8453-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="e8453-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="e8453-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="e8453-132">[salida] Puntero a un puntero a una matriz de punteros a mensajes preprocesados o generados de otro modo.</span><span class="sxs-lookup"><span data-stu-id="e8453-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="e8453-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="e8453-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="e8453-134">[salida] Puntero a una estructura [ADRLIST](adrlist.md) devuelta opcional, que enumera los destinatarios detectados por el preprocesador para los que el mensaje no se puede entregar.</span><span class="sxs-lookup"><span data-stu-id="e8453-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="e8453-135">Para obtener más información acerca del contenido de esta lista, vea el método [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md)</span><span class="sxs-lookup"><span data-stu-id="e8453-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8453-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8453-136">Return value</span></span>

<span data-ttu-id="e8453-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8453-137">S_OK</span></span>
  
> <span data-ttu-id="e8453-138">El contenido del mensaje se preprocesó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8453-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8453-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8453-139">Remarks</span></span>

<span data-ttu-id="e8453-140">Un preprocesador de mensajes del proveedor de transporte puede presentar un indicador de progreso durante el preprocesamiento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8453-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="e8453-141">Sin embargo, nunca debe presentar un cuadro de diálogo que requiera la interacción del usuario durante el preprocesamiento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8453-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="e8453-142">Cuando un preprocesador agrega grandes cantidades de datos a un mensaje saliente, deben seguirse ciertos procedimientos.</span><span class="sxs-lookup"><span data-stu-id="e8453-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="e8453-143">Este tipo de mensaje se puede almacenar en un almacén de mensajes basado en servidor, lo que hace que el preprocesador tenga acceso a un almacén remoto, un procedimiento que requiere mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="e8453-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="e8453-144">Para evitar tener que hacerlo, el preprocesador debe tener una opción que le permita almacenar datos que necesitan una gran cantidad de espacio en un almacén de mensajes local y proporcionar una referencia a ese almacén local en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e8453-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="e8453-145">El preprocesador no debe liberar ninguno de los objetos pasados originalmente a la **función basada en PreprocessMessage.**</span><span class="sxs-lookup"><span data-stu-id="e8453-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="e8453-146">Para que la cola MAPI pueda llamar a una función **PreprocessMessage,** el proveedor de transporte debe haber registrado la función en una llamada al método [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="e8453-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="e8453-147">Después de llamar a **una función PreprocessMessage,** la cola no puede continuar enviando un mensaje hasta que la función vuelva.</span><span class="sxs-lookup"><span data-stu-id="e8453-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="e8453-148">La cola MAPI es la propietaria de la tarea de enviar mensajes.</span><span class="sxs-lookup"><span data-stu-id="e8453-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="e8453-149">Esto significa que el mensaje original nunca se coloca en una matriz de punteros de mensaje y que nunca se requiere una llamada a los métodos **SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="e8453-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8453-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8453-150">See also</span></span>



[<span data-ttu-id="e8453-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e8453-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="e8453-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e8453-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="e8453-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8453-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

