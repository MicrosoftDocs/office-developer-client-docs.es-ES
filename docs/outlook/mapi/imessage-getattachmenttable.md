---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588520"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="185b6-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="185b6-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="185b6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="185b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="185b6-105">Devuelve la tabla de datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="185b6-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="185b6-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="185b6-106">Parameters</span></span>

 <span data-ttu-id="185b6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="185b6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="185b6-108">[entrada] Máscara de bits de marcadores que se relacionan con la creación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="185b6-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="185b6-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="185b6-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="185b6-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="185b6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="185b6-111">Las columnas de cadena se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="185b6-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="185b6-112">Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="185b6-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="185b6-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="185b6-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="185b6-114">Permite **GetAttachmentTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="185b6-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="185b6-115">Si no está disponible en la tabla, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="185b6-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="185b6-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="185b6-116">_lppTable_</span></span>
  
> <span data-ttu-id="185b6-117">[out] Puntero a un puntero a la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="185b6-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="185b6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="185b6-118">Return value</span></span>

<span data-ttu-id="185b6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="185b6-119">S_OK</span></span> 
  
> <span data-ttu-id="185b6-120">En la tabla de datos adjuntos se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="185b6-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="185b6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="185b6-121">Remarks</span></span>

<span data-ttu-id="185b6-122">El método **IMessage::GetAttachmentTable** devuelve un puntero a la tabla de datos adjuntos del mensaje, que incluye información acerca de todos los datos adjuntos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="185b6-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="185b6-123">Los clientes pueden obtener acceso a los datos adjuntos sólo a través de la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="185b6-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="185b6-124">Al recuperar el número de adjuntos su propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) un cliente puede usar varios de los métodos **IMessage** para trabajar con los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="185b6-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="185b6-125">Hay una fila por cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="185b6-125">There is one row for each attachment.</span></span> <span data-ttu-id="185b6-126">Para obtener una lista completa de las columnas de una tabla de datos adjuntos, vea [Las tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="185b6-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="185b6-127">Normalmente, datos adjuntos no aparecen en la tabla de datos adjuntos hasta que se han guardado los datos adjuntos y el mensaje con una llamada a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="185b6-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="185b6-128">Tablas de datos adjuntos son dinámicas.</span><span class="sxs-lookup"><span data-stu-id="185b6-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="185b6-129">Si un cliente crea un anexo nuevo, elimina un archivo adjunto existente o cambia una o más propiedades una vez que se han realizado las llamadas **SaveChanges** en los datos adjuntos en el mensaje, en la tabla de datos adjuntos se actualizarán para reflejar la nueva información.</span><span class="sxs-lookup"><span data-stu-id="185b6-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="185b6-130">Algunas tablas de datos adjuntos admiten una amplia variedad de restricciones; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="185b6-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="185b6-131">Compatibilidad con restricciones depende de la implementación del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="185b6-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="185b6-132">Cuando se abre inicialmente, tablas de datos adjuntos no se ordenan necesariamente en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="185b6-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="185b6-133">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta a las siguientes llamadas a la tabla de datos adjuntos:</span><span class="sxs-lookup"><span data-stu-id="185b6-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="185b6-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="185b6-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="185b6-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas.</span><span class="sxs-lookup"><span data-stu-id="185b6-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="185b6-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="185b6-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="185b6-137">Configuración de las solicitudes de marca de Unicode que la información de todas las columnas de cadena devueltos por estas llamadas estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="185b6-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="185b6-138">Sin embargo, debido a que no todos los proveedores de almacén de mensajes compatible con Unicode, al establecer este indicador es sólo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="185b6-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="185b6-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="185b6-139">See also</span></span>



[<span data-ttu-id="185b6-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="185b6-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="185b6-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="185b6-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="185b6-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="185b6-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="185b6-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="185b6-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

