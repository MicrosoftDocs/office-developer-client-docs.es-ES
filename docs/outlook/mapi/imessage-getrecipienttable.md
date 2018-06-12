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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817644"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="4f720-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="4f720-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="4f720-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f720-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f720-105">Devuelve la tabla de destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f720-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="4f720-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4f720-106">Parameters</span></span>

 <span data-ttu-id="4f720-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f720-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4f720-108">[entrada] Máscara de bits de indicadores que controla la devolución de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4f720-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="4f720-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4f720-109">The following flags can be set:</span></span>
    
<span data-ttu-id="4f720-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4f720-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4f720-111">Permite **GetRecipientTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4f720-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="4f720-112">Si no está disponible en la tabla, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="4f720-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="4f720-113">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4f720-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4f720-114">Columnas de la cadena deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f720-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="4f720-115">Si no está establecido el indicador MAPI_UNICODE., las columnas de la cadena deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4f720-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="4f720-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="4f720-116">_lppTable_</span></span>
  
> <span data-ttu-id="4f720-117">[out] Puntero a un puntero a la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4f720-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f720-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f720-118">Return value</span></span>

<span data-ttu-id="4f720-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f720-119">S_OK</span></span> 
  
> <span data-ttu-id="4f720-120">La tabla de destinatarios se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f720-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f720-121">Notas</span><span class="sxs-lookup"><span data-stu-id="4f720-121">Remarks</span></span>

<span data-ttu-id="4f720-122">El método **IMessage::GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información acerca de todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f720-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="4f720-123">No hay una fila por cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="4f720-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="4f720-124">Tablas de destinatarios tienen una columna diferente establecer dependiendo de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f720-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="4f720-125">Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [Las tablas de destinatario](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4f720-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="4f720-126">Algunas tablas de destinatarios de admiten una amplia variedad de restricciones; otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="4f720-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="4f720-127">Compatibilidad con restricciones depende de la implementación del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4f720-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="4f720-128">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta a las siguientes llamadas a la tabla de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="4f720-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="4f720-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="4f720-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="4f720-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas.</span><span class="sxs-lookup"><span data-stu-id="4f720-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="4f720-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="4f720-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="4f720-132">Configuración de las solicitudes de marca de Unicode que la información de todas las columnas de cadena devueltos por estas llamadas estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f720-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="4f720-133">Sin embargo, debido a que no todos los proveedores de almacén de mensajes compatible con Unicode, al establecer este indicador es sólo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f720-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f720-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4f720-134">Notes to callers</span></span>

<span data-ttu-id="4f720-135">Puede cambiar una tabla de destinatario mientras está abierto llamando al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="4f720-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="4f720-136">**ModifyRecipients** agrega a destinatarios, elimina a los destinatarios o modifica las propiedades de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4f720-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f720-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f720-137">See also</span></span>



[<span data-ttu-id="4f720-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4f720-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4f720-139">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="4f720-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="4f720-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="4f720-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="4f720-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4f720-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

