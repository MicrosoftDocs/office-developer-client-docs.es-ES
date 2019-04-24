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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319078"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente compatibles con MAPI y los proveedores de servicios pueden usar caracteres ANSI (bit único) o caracteres Unicode (byte doble). No se admiten juegos de caracteres OEM. Una cadena OEM pasada a un método o función MAPI hará que se produzca un error en ese método o función. Las aplicaciones cliente que trabajan con nombres de archivo en el juego de caracteres OEM deben tener cuidado de convertirlas a ANSI antes de pasarlas a un método o función MAPI.
  
La compatibilidad con el juego de caracteres Unicode es opcional tanto para los clientes como para los proveedores de servicios. Todos los proveedores de servicios deben escribir su código para que se puedan compilar independientemente de si admiten Unicode. Los clientes se compilan condicionalmente, en función de su nivel de compatibilidad, pero no lo hacen los proveedores de servicios. No deben volver a compilarse cuando cambia el juego de caracteres. Ningún código del proveedor de servicios debe ser condicional. 
  
Cuando los clientes o proveedores de servicios que admiten Unicode realizan una llamada de método que incluye cadenas de caracteres como parámetros de entrada o salida, establecen la marca MAPI_UNICODE. Establecer esta marca indica a la implementación que todas las cadenas entrantes son cadenas Unicode. En la salida, al establecer este indicador se solicita que todas las cadenas que se devuelvan de la implementación deban ser cadenas Unicode, si es posible. Los implementadores de métodos compatibles con Unicode cumplirán con la solicitud; los implementadores de métodos que no proporcionan compatibilidad con Unicode no cumplen con lo especificado. Las propiedades de cadena que no están en formato Unicode son del tipo PT_STRING8.
  
MAPI define la constante **fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado. Si un cliente o un proveedor de servicios admite Unicode, **fMapiUnicode** se establece en MAPI_UNICODE. Los clientes y los proveedores de servicios que no admiten Unicode set **fMapiUnicode** en cero. 
  
Los proveedores de servicios que no admiten Unicode deben:
  
- Rehusar realizar conversiones entre conjuntos de caracteres.
    
- Nunca pase la marca MAPI_UNICODE en las llamadas de método.
    
- Devuelve MAPI_E_BAD_CHARWIDTH cuando se pasa la marca MAPI_UNICODE.
    
- Declarar explícitamente las propiedades de la cadena ANSI. 
    
Los proveedores de servicios también pueden devolver MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no pasan la marca MAPI_UNICODE. 
  
 La versión actual de MAPI admite Unicode en los métodos siguientes: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Solo implementación de**IAddrBook** ) 
  
Para estos métodos, los autores de las llamadas pueden esperar que las cadenas que se devuelvan sean Unicode. Las cadenas de caracteres devueltas por las implementaciones MAPI de cualquier otro método serán cadenas de caracteres ANSI.
  

