---
title: Conjuntos de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582535"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Pueden usar proveedores de servicios y aplicaciones de cliente compatible con MAPI (byte único) los caracteres ANSI o Unicode (de doble byte). No se admiten los conjuntos de caracteres OEM. Una cadena de OEM se pasa a un método MAPI o función hará que dicho método o función se lleve a cabo. Las aplicaciones de cliente que funcionan con los nombres de archivo en el juego de caracteres OEM deben tener cuidadas convertir a ANSI antes de pasarlas a un método MAPI o función.
  
Compatibilidad con Unicode juego de caracteres es opcional, tanto para los clientes y proveedores de servicios. Todos los proveedores de servicios deben escribir su código para que puede compilar independientemente de si o no admiten Unicode. Los clientes compilación condicionalmente, dependiendo de su nivel de compatibilidad, pero no lo hacen los proveedores de servicios. No tendrán que volver a compilar cuando el juego de los cambios. Nada en el código de proveedor de servicio debe ser condicional. 
  
Cuando los clientes o proveedores de servicios que admiten Unicode realizar una llamada de método que incluye las cadenas de caracteres como parámetros de entrada o salidas, establecer el indicador MAPI_UNICODE.. Establecer esta marca indica a la implementación que todas las cadenas entrantes son cadenas Unicode. En la salida, establecer este las solicitudes de marca que hacer una copia de todas las cadenas que se pasan desde la implementación debe ser cadenas Unicode si es posible. Los implementadores de método que admiten Unicode cumplirá la solicitud; no se cumplen los implementadores de método que no proporcionan compatibilidad con Unicode. Propiedades de cadena que no están en formato Unicode son de tipo PT_STRING8.
  
MAPI define la constante **fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado. Si un proveedor de servicio o cliente es compatible con Unicode, **fMapiUnicode** se establece en MAPI_UNICODE.. Los clientes y proveedores de servicios que no admiten Unicode establecen **fMapiUnicode** a cero. 
  
Proveedores de servicios que no admiten Unicode deben:
  
- Denegar realizar las conversiones entre conjuntos de caracteres.
    
- Nunca pase el indicador MAPI_UNICODE llamadas al método.
    
- Devolver MAPI_E_BAD_CHARWIDTH cuando se pasa el indicador MAPI_UNICODE en.
    
- Declarar explícitamente las propiedades de cadena ANSI. 
    
Proveedores de servicio también pueden devolver MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no se pasa el indicador MAPI_UNICODE.. 
  
 La versión actual de MAPI admite Unicode en los siguientes métodos: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Sólo en la implementación**IAddrBook** ) 
  
Para estos métodos, los autores de llamadas pueden esperar cualquier cadenas devueltas como cadenas Unicode. Las cadenas de caracteres devueltas desde las implementaciones de MAPI de cualquier otro método será cadenas de caracteres ANSI.
  

