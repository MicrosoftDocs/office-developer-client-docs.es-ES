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
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579539"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="39752-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="39752-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="39752-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39752-105">Devuelve la tabla de destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="39752-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="39752-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="39752-106">Parameters</span></span>

 <span data-ttu-id="39752-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39752-107">_ulFlags_</span></span>
  
> <span data-ttu-id="39752-108">[entrada] Máscara de bits de indicadores que controla la devolución de la tabla.</span><span class="sxs-lookup"><span data-stu-id="39752-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="39752-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="39752-109">The following flags can be set:</span></span>
    
<span data-ttu-id="39752-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="39752-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="39752-111">Permite **GetRecipientTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="39752-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="39752-112">Si no está disponible en la tabla, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="39752-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="39752-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39752-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39752-114">Columnas de la cadena deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="39752-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="39752-115">Si no está establecido el indicador MAPI_UNICODE., las columnas de la cadena deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="39752-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="39752-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="39752-116">_lppTable_</span></span>
  
> <span data-ttu-id="39752-117">[out] Puntero a un puntero a la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="39752-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39752-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39752-118">Return value</span></span>

<span data-ttu-id="39752-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="39752-119">S_OK</span></span> 
  
> <span data-ttu-id="39752-120">La tabla de destinatarios se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="39752-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39752-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39752-121">Remarks</span></span>

<span data-ttu-id="39752-122">El método **IMessage::GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información acerca de todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="39752-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="39752-123">No hay una fila por cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="39752-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="39752-124">Tablas de destinatarios tienen una columna diferente establecer dependiendo de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="39752-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="39752-125">Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [Las tablas de destinatario](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="39752-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="39752-126">Algunas tablas de destinatarios de admiten una amplia variedad de restricciones; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="39752-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="39752-127">Compatibilidad con restricciones depende de la implementación del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="39752-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="39752-128">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta a las siguientes llamadas a la tabla de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="39752-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="39752-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="39752-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="39752-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas.</span><span class="sxs-lookup"><span data-stu-id="39752-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="39752-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="39752-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="39752-132">Configuración de las solicitudes de marca de Unicode que la información de todas las columnas de cadena devueltos por estas llamadas estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="39752-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="39752-133">Sin embargo, debido a que no todos los proveedores de almacén de mensajes compatible con Unicode, al establecer este indicador es sólo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="39752-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="39752-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="39752-134">Notes to callers</span></span>

<span data-ttu-id="39752-135">Puede cambiar una tabla de destinatario mientras está abierto llamando al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="39752-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="39752-136">**ModifyRecipients** agrega a destinatarios, elimina a los destinatarios o modifica las propiedades de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="39752-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39752-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="39752-137">See also</span></span>



[<span data-ttu-id="39752-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="39752-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="39752-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="39752-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="39752-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="39752-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="39752-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="39752-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

