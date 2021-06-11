---
title: Control de errores de propiedad con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429869"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="e7fb5-103">Control de errores de propiedad con nombre</span><span class="sxs-lookup"><span data-stu-id="e7fb5-103">Handling named property errors</span></span>
  
<span data-ttu-id="e7fb5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7fb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7fb5-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="e7fb5-107">Cuando no se encuentra un resultado llamada �xito parcial, por ejemplo, cuando la solicitud es para los nombres que se asignan a identificadores espec�ficos y uno o varios nombres, **GetNamesFromIDs** devuelve MAPI_W_ERRORS_RETURNED y coloca PT_ERROR en el tipo de propiedad para la propiedad que faltan en la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="e7fb5-p102">En ocasiones, un cliente realiza una llamada a **GetNamesFromIDs** que da como resultado ninguna propiedad que se devuelve, como cuando no hay ninguna propiedad en un conjunto de propiedades especificado, o cuando todas las propiedades con nombre de un tipo que excluya las marcas. Los clientes pueden esperar los proveedores de servicios:</span><span class="sxs-lookup"><span data-stu-id="e7fb5-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="e7fb5-110">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-110">Return S_OK.</span></span>
    
- <span data-ttu-id="e7fb5-111">Establecer el contenido del puntero de matriz de etiqueta de propiedad en una matriz de etiqueta de propiedad reci�n asignados con su miembro **cValues** establece en cero.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="e7fb5-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="e7fb5-113">Establecer el contenido del recuento de estructuras **MAPINAMEID** en cero.</span><span class="sxs-lookup"><span data-stu-id="e7fb5-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e7fb5-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7fb5-114">See also</span></span>

- [<span data-ttu-id="e7fb5-115">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="e7fb5-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

