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
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349276"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="cf9b0-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="cf9b0-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="cf9b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf9b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf9b0-105">Devuelve la tabla de datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="cf9b0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf9b0-106">Parameters</span></span>

 <span data-ttu-id="cf9b0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf9b0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cf9b0-108">a Máscara de máscara de los marcadores que se relacionan con la creación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="cf9b0-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="cf9b0-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="cf9b0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cf9b0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cf9b0-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="cf9b0-112">Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="cf9b0-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="cf9b0-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="cf9b0-114">Permite que **GetAttachmentTable** se devuelva correctamente, posiblemente antes de que la tabla esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="cf9b0-115">Si la tabla no está disponible, realizar una llamada subsiguiente a ella puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="cf9b0-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="cf9b0-116">_lppTable_</span></span>
  
> <span data-ttu-id="cf9b0-117">contempla Puntero a un puntero a la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf9b0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf9b0-118">Return value</span></span>

<span data-ttu-id="cf9b0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf9b0-119">S_OK</span></span> 
  
> <span data-ttu-id="cf9b0-120">La tabla de datos adjuntos se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf9b0-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf9b0-121">Remarks</span></span>

<span data-ttu-id="cf9b0-122">El método **IMessage:: GetAttachmentTable** devuelve un puntero a la tabla de datos adjuntos del mensaje, que incluye información sobre todos los datos adjuntos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="cf9b0-123">Los clientes pueden obtener acceso a datos adjuntos solo a través de la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="cf9b0-124">Al recuperar el número de datos adjuntos, su propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), un cliente puede usar varios de los métodos **IMessage** para trabajar con los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="cf9b0-125">Hay una fila por cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-125">There is one row for each attachment.</span></span> <span data-ttu-id="cf9b0-126">Para obtener una lista completa de las columnas de una tabla de datos adjuntos, vea [tablas de datos](attachment-tables.md)adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="cf9b0-127">Los datos adjuntos no suelen aparecer en la tabla de datos adjuntos hasta que se guardan los datos adjuntos y el mensaje con una llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="cf9b0-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="cf9b0-128">Las tablas de datos adJuntos son dinámicas.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="cf9b0-129">Si un cliente crea un nuevo dato adjunto, elimina un archivo de datos adjuntos existente o cambia una o más propiedades una vez que se han realizado las llamadas de **SaveChanges** en los datos adjuntos del mensaje, la tabla de datos adjuntos se actualizará para reflejar la nueva información.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="cf9b0-130">Algunas tablas de datos adjuntos admiten una amplia variedad de restricciones; otros no.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="cf9b0-131">La compatibilidad con las restricciones depende de la implementación del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="cf9b0-132">Cuando se abren por primera vez, las tablas de datos adjuntos no están necesariamente ordenadas en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="cf9b0-133">Si se establece la marca MAPI_UNICODE en el parámetro _ulFlags_ , se verán afectadas las siguientes llamadas a la tabla Attachment:</span><span class="sxs-lookup"><span data-stu-id="cf9b0-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="cf9b0-134">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="cf9b0-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="cf9b0-136">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="cf9b0-137">Al establecer el indicador Unicode, se solicita que la información de las columnas de cadena devueltas por estas llamadas esté en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="cf9b0-138">Sin embargo, como no todos los proveedores de almacenamiento de mensajes admiten Unicode, establecer esta marca es solo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf9b0-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf9b0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf9b0-139">See also</span></span>



[<span data-ttu-id="cf9b0-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="cf9b0-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="cf9b0-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="cf9b0-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="cf9b0-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="cf9b0-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="cf9b0-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf9b0-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

