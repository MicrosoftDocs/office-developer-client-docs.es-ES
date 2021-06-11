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
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417556"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente compatibles con MAPI y los proveedores de servicios pueden usar caracteres ANSI (byte único) o caracteres Unicode (byte doble). No se admiten los conjuntos de caracteres OEM. Una cadena OEM que se pasa a un método o función MAPI provocará un error en ese método o función. Las aplicaciones cliente que trabajan con nombres de archivo en el juego de caracteres OEM deben tener cuidado de convertirlos en ANSI antes de pasarlos a un método o función MAPI.
  
La compatibilidad con el juego de caracteres Unicode es opcional, tanto para clientes como para proveedores de servicios. Todos los proveedores de servicios deben escribir su código para que puedan compilar independientemente de si admiten Unicode o no. Los clientes se compilan condicionalmente, según su nivel de compatibilidad, pero los proveedores de servicios no lo hacen. No deben tener que volver a compilarse cuando cambie el juego de caracteres. Nada en el código del proveedor de servicios debe ser condicional. 
  
Cuando los clientes o proveedores de servicios compatibles con Unicode hacen una llamada al método que incluye cadenas de caracteres como parámetros de entrada o salida, establecen la marca MAPI_UNICODE caracteres. Si se establece esta marca, se indica a la implementación que todas las cadenas entrantes son cadenas Unicode. Al salir, al establecer esta marca se solicita que todas las cadenas pasadas de la implementación sean cadenas Unicode si es posible. Los implementadores de métodos compatibles con Unicode cumplirán con la solicitud; los implementadores de métodos que no proporcionan compatibilidad con Unicode no cumplirán. Las propiedades de cadena que no están en formato Unicode son de tipo PT_STRING8.
  
MAPI define la **constante fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado. Si un cliente o proveedor de servicios admite Unicode, **fMapiUnicode** se establece en MAPI_UNICODE. Los clientes y proveedores de servicios que no admiten Unicode establecen **fMapiUnicode** en cero. 
  
Los proveedores de servicios que no admiten Unicode deben:
  
- Rehúsa realizar conversiones entre conjuntos de caracteres.
    
- Nunca pase la marca MAPI_UNICODE en llamadas a métodos.
    
- Devuelve MAPI_E_BAD_CHARWIDTH cuando se pasa MAPI_UNICODE la marca.
    
- Declare explícitamente las propiedades de cadena ANSI. 
    
Los proveedores de servicios también pueden devolver MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no pasan la marca MAPI_UNICODE. 
  
 La versión actual de MAPI admite Unicode en los siguientes métodos: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**solo implementación de IAddrBook)** 
  
Para estos métodos, los autores de llamadas pueden esperar que las cadenas devueltas sean cadenas Unicode. Las cadenas de caracteres devueltas de implementaciones MAPI de cualquier otro método serán cadenas de caracteres ANSI.
  

