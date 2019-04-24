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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349283"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="57287-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="57287-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="57287-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57287-105">Devuelve la tabla de destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="57287-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="57287-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="57287-106">Parameters</span></span>

 <span data-ttu-id="57287-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57287-107">_ulFlags_</span></span>
  
> <span data-ttu-id="57287-108">a Máscara de máscara de marcadores que controla la devolución de la tabla.</span><span class="sxs-lookup"><span data-stu-id="57287-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="57287-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="57287-109">The following flags can be set:</span></span>
    
<span data-ttu-id="57287-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="57287-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="57287-111">Permite que **GetRecipientTable** se devuelva correctamente, posiblemente antes de que la tabla esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="57287-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="57287-112">Si la tabla no está disponible, realizar una llamada subsiguiente a ella puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="57287-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="57287-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57287-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="57287-114">Las columnas de cadena deben tener formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="57287-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="57287-115">Si no se establece la marca MAPI_UNICODE, las columnas de cadena deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="57287-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="57287-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="57287-116">_lppTable_</span></span>
  
> <span data-ttu-id="57287-117">contempla Puntero a un puntero a la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="57287-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57287-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57287-118">Return value</span></span>

<span data-ttu-id="57287-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="57287-119">S_OK</span></span> 
  
> <span data-ttu-id="57287-120">La tabla de destinatarios se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="57287-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57287-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57287-121">Remarks</span></span>

<span data-ttu-id="57287-122">El método **IMessage:: GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información sobre todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="57287-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="57287-123">Hay una fila por cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="57287-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="57287-124">Las tablas de destinatarios tienen un conjunto de columnas diferente en función de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="57287-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="57287-125">Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [tablas](recipient-tables.md)de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="57287-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="57287-126">Algunas tablas de destinatarios admiten una amplia variedad de restricciones; otros no.</span><span class="sxs-lookup"><span data-stu-id="57287-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="57287-127">La compatibilidad con las restricciones depende de la implementación del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57287-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="57287-128">Si se establece la marca MAPI_UNICODE en el parámetro _ulFlags_ , se verán afectadas las siguientes llamadas a la tabla recipient:</span><span class="sxs-lookup"><span data-stu-id="57287-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="57287-129">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="57287-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="57287-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="57287-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="57287-131">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="57287-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="57287-132">Al establecer el indicador Unicode, se solicita que la información de las columnas de cadena devueltas por estas llamadas esté en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="57287-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="57287-133">Sin embargo, como no todos los proveedores de almacenamiento de mensajes admiten Unicode, establecer esta marca es solo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="57287-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="57287-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="57287-134">Notes to callers</span></span>

<span data-ttu-id="57287-135">Puede cambiar una tabla de destinatarios mientras está abierta llamando al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="57287-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="57287-136">**ModifyRecipients** agrega los destinatarios, elimina los destinatarios o modifica las propiedades de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="57287-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57287-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="57287-137">See also</span></span>



[<span data-ttu-id="57287-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="57287-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="57287-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="57287-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="57287-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="57287-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="57287-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="57287-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

