---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412635"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="3e28e-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="3e28e-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="3e28e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e28e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e28e-105">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="3e28e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3e28e-106">Parameters</span></span>

 <span data-ttu-id="3e28e-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3e28e-107">_lpInterface_</span></span>
  
> <span data-ttu-id="3e28e-108">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="3e28e-109">Los identificadores de interfaz válidos incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="3e28e-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="3e28e-110">Si se pasa NULL, el proveedor de almacén de mensajes devolverá la interfaz de mensaje estándar, [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="3e28e-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="3e28e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e28e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="3e28e-112">a Una máscara de máscara de marcas que controla cómo se crea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="3e28e-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3e28e-113">The following flags can be set:</span></span>
    
<span data-ttu-id="3e28e-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="3e28e-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="3e28e-115">Indica al almacén de carpetas personales (PST) que el mensaje es apto para el procesamiento de reglas antes de que el almacén notifique a los clientes de escuchas la llegada del nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="3e28e-116">El procesamiento de reglas solo se aplica a los mensajes nuevos que se crean en un servidor que no es Microsoft Exchange Server, ya que Exchange Server procesa las reglas para los mensajes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e28e-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="3e28e-117">Por lo tanto, el proveedor o el cliente que crea el mensaje debe pasar esta marca en combinación con guardar un mensaje con [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) con NON_EMS_XP_SAVE, que indica que el servidor no es un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e28e-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="3e28e-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="3e28e-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="3e28e-119">El mensaje que se va a crear debe incluirse en la tabla de contenido asociada en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="3e28e-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="3e28e-120">Los mensajes asociados están ocultos para la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="3e28e-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="3e28e-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="3e28e-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="3e28e-122">**CreateMessage** puede tener éxito incluso si la operación de creación no se completó completamente.</span><span class="sxs-lookup"><span data-stu-id="3e28e-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="3e28e-123">Esto implica que el nuevo mensaje puede que no esté disponible inmediatamente para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3e28e-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="3e28e-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="3e28e-124">_lppMessage_</span></span>
  
> <span data-ttu-id="3e28e-125">contempla Un puntero a un puntero al mensaje que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="3e28e-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e28e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e28e-126">Return value</span></span>

<span data-ttu-id="3e28e-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e28e-127">S_OK</span></span> 
  
> <span data-ttu-id="3e28e-128">El mensaje se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e28e-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e28e-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e28e-129">Remarks</span></span>

<span data-ttu-id="3e28e-130">El método **IMAPIFolder:: CreateMessage** crea un nuevo mensaje con contenido genérico o asociado y asigna un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="3e28e-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="3e28e-131">El identificador de entrada consta de una parte que representa al proveedor de almacenamiento de mensajes y una parte que representa el mensaje individual.</span><span class="sxs-lookup"><span data-stu-id="3e28e-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3e28e-132">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="3e28e-132">Notes to implementers</span></span>

<span data-ttu-id="3e28e-133">Puede elegir si desea establecer todas las propiedades de mensaje necesarias en **CreateMessage** o en el método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="3e28e-134">No es necesario que estas propiedades estén disponibles hasta que se haya guardado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e28e-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="3e28e-135">Para obtener más información sobre cómo trabajar con información asociada, vea tablas [de información asociada a carpetas](folder-associated-information-tables.md) y [tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3e28e-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e28e-136">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3e28e-136">Notes to callers</span></span>

<span data-ttu-id="3e28e-137">Algunos proveedores de almacenamiento de mensajes permiten que el identificador de entrada del nuevo mensaje esté disponible inmediatamente una vez devuelto **CreateMessage** ; otros proveedores de almacenamiento de mensajes retrasan su disponibilidad hasta que se guarda el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="3e28e-138">Como no todos los proveedores de almacenamiento de mensajes generan un identificador de entrada para un mensaje nuevo hasta que se llama al método **IMAPIProp:: SaveChanges** del mensaje, es posible que no pueda obtener acceso al identificador de entrada cuando **CreateMessage** devuelve.</span><span class="sxs-lookup"><span data-stu-id="3e28e-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="3e28e-139">Además, es posible que el nuevo mensaje no se incluya en la tabla de contenido de la carpeta hasta que se guarde.</span><span class="sxs-lookup"><span data-stu-id="3e28e-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="3e28e-140">Se espera que el identificador de entrada asignado al nuevo mensaje sea único y que sea único en el almacén de mensajes actual, pero lo más probable es que todos los almacenes de mensajes estén abiertos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="3e28e-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="3e28e-141">Se produce una excepción a esta regla cuando en el perfil aparecen varias entradas para un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3e28e-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="3e28e-142">Esto hace que el almacén de mensajes se abra varias veces y que se dupliquen los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="3e28e-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="3e28e-143">Para crear un mensaje saliente, llame al método **IMAPIFolder:: CreateMessage** de la carpeta Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="3e28e-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="3e28e-144">Si elimina una carpeta que contiene un mensaje nuevo antes de guardar el mensaje, los resultados quedan sin definir.</span><span class="sxs-lookup"><span data-stu-id="3e28e-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3e28e-145">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3e28e-145">MFCMAPI reference</span></span>

<span data-ttu-id="3e28e-146">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3e28e-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3e28e-147">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3e28e-147">**File**</span></span>|<span data-ttu-id="3e28e-148">**Función**</span><span class="sxs-lookup"><span data-stu-id="3e28e-148">**Function**</span></span>|<span data-ttu-id="3e28e-149">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3e28e-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e28e-150">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="3e28e-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="3e28e-151">CFolder:: OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="3e28e-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="3e28e-152">MFCMAPI usa el método **IMAPIFolder:: CreateMessage** para crear y guardar un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e28e-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e28e-153">Ver también</span><span class="sxs-lookup"><span data-stu-id="3e28e-153">See also</span></span>



[<span data-ttu-id="3e28e-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="3e28e-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="3e28e-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3e28e-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="3e28e-156">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3e28e-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

