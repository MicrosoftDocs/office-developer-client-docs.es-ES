---
title: Denominado de tratamiento de errores (propiedad)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9ea1c4063c08844052618c50fe53fdc0064787a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816939"
---
# <a name="handling-named-property-errors"></a>Denominado de tratamiento de errores (propiedad)
  
**Se aplica a**: Outlook 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Cuando no se encuentra un resultado llamada �xito parcial, por ejemplo, cuando la solicitud es para los nombres que se asignan a identificadores espec�ficos y uno o varios nombres, **GetNamesFromIDs** devuelve MAPI_W_ERRORS_RETURNED y coloca PT_ERROR en el tipo de propiedad para la propiedad que faltan en la matriz de la etiqueta de propiedad. 
  
En ocasiones, un cliente realiza una llamada a **GetNamesFromIDs** que da como resultado ninguna propiedad que se devuelve, como cuando no hay ninguna propiedad en un conjunto de propiedades especificado, o cuando todas las propiedades con nombre de un tipo que excluya las marcas. Los clientes pueden esperar los proveedores de servicios: 
  
- Devuelve S_OK.
    
- Establecer el contenido del puntero de matriz de etiqueta de propiedad en una matriz de etiqueta de propiedad reci�n asignados con su miembro **cValues** establece en cero. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- Establecer el contenido del recuento de estructuras **MAPINAMEID** en cero. 
    
## <a name="see-also"></a>Vea tambi�n

- [Con el nombre de las propiedades de MAPI](mapi-named-properties.md)

