---
title: Propiedades de la cadena MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572329"
---
# <a name="mapi-string-properties"></a>Propiedades de la cadena MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona tres tipos de propiedad diferentes para describir las propiedades de cadena:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Propiedades de cadena con más frecuencia se definen como PT_TSTRING. El tipo de propiedad PT_TSTRING compila condicionalmente a uno de los otros cadena tipos de propiedad, dependiendo del dependiendo de si se ha definido la macro UNICODE. PT_STRING8 describe las cadenas de caracteres terminada en null de 8 bits en el formato ANSI; PT_UNICODE describe las cadenas de caracteres de doble byte terminada en null. 
  
Pueden elegir ya sea un cliente o un proveedor de servicios, o cliente y proveedor admitir las cadenas de caracteres Unicode. No es necesario. Un cliente que admite cadenas de PT_STRING8 sólo puede funcionar con un proveedor que es compatible con Unicode y viceversa. Para habilitar esta interoperabilidad, clientes y proveedores de servicios de pasan una marca, el indicador MAPI_UNICODE., para indicar que Unicode es compatible con métodos que impliquen el intercambio de cadenas de caracteres. 
  
Por ejemplo, supongamos que un cliente compatible con Unicode y necesita recuperar el nombre para mostrar de una carpeta. Todas las propiedades del cliente PT_TSTRING se compilan para escriba PT_UNICODE. Cuando el cliente llama (método) [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), se pasa el indicador MAPI_UNICODE para solicitar que se devuelva la cadena de nombre para mostrar en el formato Unicode . 
  
Los clientes y proveedores de servicios deben tener en cuenta que especificar un juego de caracteres de una llamada al método es sólo una solicitud. Compatibilidad con uno o ambos conjuntos de caracteres es responsabilidad del implementador del objeto. No obstante, los proveedores de servicios se recomienda para admitir ambos conjuntos de caracteres porque permite conseguir una distribución más generalizada que los proveedores que admiten un solo conjunto. 
  
Propiedades de cadena pueden llegar a ser bastante grande tal como se pueden propiedades binarias, las propiedades que utilice la propiedad escriba PT_BINARY. Para facilitar la trabajar con propiedades de gran tamaño, MAPI permite que los proveedores de servicios establecer estas propiedades aplicar los límites de tamaño. Estos límites pueden variar, dependiendo del:
  
- Si se va las propiedades leído o escrito.
    
- Cómo el proveedor de servicios implementa los métodos de **IMAPIProp** . 
    
- Consideraciones de tiempo de ejecución, como las restricciones de memoria.
    
- Juego de caracteres posibles problemas de traducción. 
    
También se pueden colocar los límites de tamaño en la cadena y establecen propiedades binarias cuando se usan en la columna de una tabla debido a que a veces es imposible que todos los de un gran valor de la propiedad visible. Muchos proveedores de servicios truncan la cadena de gran tamaño o propiedades binarias que se usan en las tablas a 255 bytes. 
  
Cuando un cliente llama a un método del objeto **GetProps** o **SetProps** para funcionar con una cadena de gran tamaño o propiedad binaria y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY. Si es así **GetProps** que tiene errores para una propiedad concreta, el cliente puede recuperar llamando a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitar la **IStream** para el acceso mediante la especificación de IID_IStream como el identificador de interfaz. Uso de **OpenProperty**, el cliente puede recuperar una propiedad de gran tamaño mediante una interfaz como **IStream** que es más adecuado para trabajar con propiedades de gran tamaño. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

