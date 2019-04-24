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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299373"
---
# <a name="handling-named-property-errors"></a>Control de errores de propiedad con nombre
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Cuando no se encuentra un resultado llamada �xito parcial, por ejemplo, cuando la solicitud es para los nombres que se asignan a identificadores espec�ficos y uno o varios nombres, **GetNamesFromIDs** devuelve MAPI_W_ERRORS_RETURNED y coloca PT_ERROR en el tipo de propiedad para la propiedad que faltan en la matriz de la etiqueta de propiedad. 
  
En ocasiones, un cliente realiza una llamada a **GetNamesFromIDs** que da como resultado ninguna propiedad que se devuelve, como cuando no hay ninguna propiedad en un conjunto de propiedades especificado, o cuando todas las propiedades con nombre de un tipo que excluya las marcas. Los clientes pueden esperar los proveedores de servicios: 
  
- Devuelve S_OK.
    
- Establecer el contenido del puntero de matriz de etiqueta de propiedad en una matriz de etiqueta de propiedad reci�n asignados con su miembro **cValues** establece en cero. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- Establecer el contenido del recuento de estructuras **MAPINAMEID** en cero. 
    
## <a name="see-also"></a>Vea también

- [Propiedades con nombre MAPI](mapi-named-properties.md)

