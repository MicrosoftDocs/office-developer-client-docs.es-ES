---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424612"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="943b9-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="943b9-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="943b9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="943b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="943b9-105">Devuelve la tabla de destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="943b9-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="943b9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="943b9-106">Parameters</span></span>

 <span data-ttu-id="943b9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="943b9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="943b9-108">[in] Máscara de bits de marcas que controla el retorno de la tabla.</span><span class="sxs-lookup"><span data-stu-id="943b9-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="943b9-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="943b9-109">The following flags can be set:</span></span>
    
<span data-ttu-id="943b9-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="943b9-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="943b9-111">Permite **que GetRecipientTable** vuelva correctamente, posiblemente antes de que la tabla esté totalmente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="943b9-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="943b9-112">Si la tabla no está disponible, realizar una llamada posterior a ella puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="943b9-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="943b9-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="943b9-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="943b9-114">Las columnas de cadena deben tener un formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="943b9-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="943b9-115">Si no MAPI_UNICODE marca, las columnas de cadena deben tener el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="943b9-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="943b9-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="943b9-116">_lppTable_</span></span>
  
> <span data-ttu-id="943b9-117">[salida] Puntero a un puntero a la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="943b9-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="943b9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="943b9-118">Return value</span></span>

<span data-ttu-id="943b9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="943b9-119">S_OK</span></span> 
  
> <span data-ttu-id="943b9-120">La tabla de destinatarios se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="943b9-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="943b9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="943b9-121">Remarks</span></span>

<span data-ttu-id="943b9-122">El **método IMessage::GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información sobre todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="943b9-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="943b9-123">Hay una fila para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="943b9-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="943b9-124">Las tablas de destinatarios tienen un conjunto de columnas diferente en función de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="943b9-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="943b9-125">Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [Tablas de destinatarios](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="943b9-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="943b9-126">Algunas tablas de destinatarios admiten una amplia variedad de restricciones; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="943b9-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="943b9-127">La compatibilidad con restricciones depende de la implementación del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="943b9-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="943b9-128">Establecer la MAPI_UNICODE en el  _parámetro ulFlags_ afecta a las siguientes llamadas a la tabla de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="943b9-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="943b9-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="943b9-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="943b9-130">[IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="943b9-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="943b9-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="943b9-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="943b9-132">Al establecer la marca Unicode, se solicita que la información de las columnas de cadena devueltas de estas llamadas esté en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="943b9-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="943b9-133">Sin embargo, como no todos los proveedores de almacén de mensajes admiten Unicode, establecer esta marca es solo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="943b9-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="943b9-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="943b9-134">Notes to callers</span></span>

<span data-ttu-id="943b9-135">Puede cambiar una tabla de destinatarios mientras está abierta llamando al [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="943b9-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="943b9-136">**ModifyRecipients** agrega destinatarios, elimina destinatarios o modifica las propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="943b9-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="943b9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="943b9-137">See also</span></span>



[<span data-ttu-id="943b9-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="943b9-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="943b9-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="943b9-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="943b9-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="943b9-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="943b9-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="943b9-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

