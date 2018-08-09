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
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817226"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="6b217-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="6b217-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="6b217-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b217-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b217-105">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b217-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="6b217-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b217-106">Parameters</span></span>

 <span data-ttu-id="6b217-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6b217-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6b217-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="6b217-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="6b217-109">Identificadores de interfaz válido incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="6b217-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="6b217-110">Pasando NULL hace que el proveedor de almacenamiento de mensajes devolver la interfaz de mensaje estándar, [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6b217-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="6b217-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b217-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6b217-112">[entrada] Una máscara de bits de indicadores que controla cómo se crea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b217-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="6b217-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="6b217-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6b217-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="6b217-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="6b217-115">Indica al almacén de carpetas personales (PST) que el mensaje es apto para reglas de procesamiento antes de que el almacén notifica a cualquier cliente de escucha de la llegada del nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b217-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="6b217-116">Las reglas de procesamiento sólo se aplica a los nuevos mensajes que se crean en un servidor que no es un servidor de Exchange de Microsoft, debido a que Exchange Server procesa las reglas para los mensajes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="6b217-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="6b217-117">Por lo tanto, el proveedor o cliente que crea el mensaje debe pasar esta marca en combinación con el almacenamiento de un mensaje con [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) con NON_EMS_XP_SAVE, que indica que el servidor no es un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b217-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="6b217-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="6b217-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="6b217-119">El mensaje que se va a crear se debe incluir en la tabla de contenido asociadas en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="6b217-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="6b217-120">Los mensajes asociados están ocultos de interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="6b217-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="6b217-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6b217-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6b217-122">Se permite que **CreateMessage** correctamente incluso si no se ha completado la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="6b217-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="6b217-123">Esto implica que el nuevo mensaje es posible que no sean inmediatamente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6b217-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="6b217-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="6b217-124">_lppMessage_</span></span>
  
> <span data-ttu-id="6b217-125">[out] Un puntero a un puntero al mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="6b217-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b217-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b217-126">Return value</span></span>

<span data-ttu-id="6b217-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b217-127">S_OK</span></span> 
  
> <span data-ttu-id="6b217-128">El mensaje se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b217-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b217-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b217-129">Remarks</span></span>

<span data-ttu-id="6b217-130">El método **IMAPIFolder::CreateMessage** crea un nuevo mensaje con contenido genérico o asociado y le asigna un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b217-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="6b217-131">El identificador de entrada consta de un elemento que representa el proveedor de almacén de mensajes y un elemento que representa el mensaje individual.</span><span class="sxs-lookup"><span data-stu-id="6b217-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b217-132">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="6b217-132">Notes to implementers</span></span>

<span data-ttu-id="6b217-133">Puede elegir si va a establecer todas las propiedades del mensaje se requiere en **CreateMessage** o en el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b217-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="6b217-134">No es necesario que estas propiedades esté disponible hasta que se ha producido una operación de guardar correcta.</span><span class="sxs-lookup"><span data-stu-id="6b217-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="6b217-135">Para obtener más información acerca de cómo trabajar con información asociada, vea [Las tablas de información de Folder-Associated](folder-associated-information-tables.md) y [Las tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6b217-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6b217-136">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6b217-136">Notes to callers</span></span>

<span data-ttu-id="6b217-137">Algunos proveedores de almacén de mensajes permiten el identificador de entrada del nuevo mensaje para que estén disponibles inmediatamente después de **CreateMessage** devuelve; otros proveedores de almacenes de mensaje retrasar su disponibilidad hasta que se guarda el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b217-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="6b217-138">Debido a que no todos los proveedores de almacén de mensajes generan un identificador de entrada para un nuevo mensaje de hasta que se ha llamado (método **IMAPIProp::SaveChanges** ) del mensaje, es posible que no se puede obtener acceso al identificador de entrada cuando **CreateMessage** devuelve.</span><span class="sxs-lookup"><span data-stu-id="6b217-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="6b217-139">Además, el nuevo mensaje es posible que no se incluyan en la tabla de contenido de la carpeta hasta que se produce la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="6b217-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="6b217-140">Esperar el identificador de entrada asignado al mensaje nuevo para ser únicos no sólo en el almacén de mensajes actual, pero es más probable que a través de todos los almacenes de mensajes que están abiertos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6b217-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="6b217-141">Una excepción a esta regla se produce cuando aparecen varias entradas para un almacén de mensajes en el perfil.</span><span class="sxs-lookup"><span data-stu-id="6b217-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="6b217-142">Esto hace que el almacén de mensajes que se va a abrir varias veces y los identificadores de entrada que se va a duplicar.</span><span class="sxs-lookup"><span data-stu-id="6b217-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="6b217-143">Para crear un mensaje saliente, llamar al método **IMAPIFolder::CreateMessage** de la carpeta Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="6b217-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="6b217-144">Si elimina una carpeta que contiene un mensaje nuevo antes de que el mensaje se guarda, los resultados son no definidos.</span><span class="sxs-lookup"><span data-stu-id="6b217-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b217-145">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6b217-145">MFCMAPI reference</span></span>

<span data-ttu-id="6b217-146">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6b217-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b217-147">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6b217-147">**File**</span></span>|<span data-ttu-id="6b217-148">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="6b217-148">**Function**</span></span>|<span data-ttu-id="6b217-149">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6b217-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b217-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6b217-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="6b217-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="6b217-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="6b217-152">MFCMAPI usa el método **IMAPIFolder::CreateMessage** para crear y guardar un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="6b217-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b217-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b217-153">See also</span></span>



[<span data-ttu-id="6b217-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6b217-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6b217-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6b217-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="6b217-156">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="6b217-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

