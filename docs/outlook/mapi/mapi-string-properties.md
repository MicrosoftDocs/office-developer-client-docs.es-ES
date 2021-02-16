---
title: Propiedades de cadena MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431396"
---
# <a name="mapi-string-properties"></a>Propiedades de cadena MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona tres tipos de propiedades diferentes para describir las propiedades de cadena:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Las propiedades de cadena se definen normalmente como PT_TSTRING. El PT_TSTRING de propiedad se compila condicionalmente en uno de los otros tipos de propiedad de cadena, dependiendo de si se ha definido la macro UNICODE. PT_STRING8 describe cadenas de caracteres terminadas en null de 8 bits en formato ANSI; PT_UNICODE describe las cadenas de caracteres terminadas en null de doble byte. 
  
Un cliente o un proveedor de servicios, o tanto el cliente como el proveedor pueden elegir admitir cadenas de caracteres Unicode. No es necesario. Un cliente que solo admite PT_STRING8 cadenas pueden funcionar con un proveedor compatible con Unicode y viceversa. Para habilitar esta interoperabilidad, los clientes y proveedores de servicios pasan una marca, la marca MAPI_UNICODE, para indicar que Unicode es compatible con métodos que implican el intercambio de cadenas de caracteres. 
  
Por ejemplo, supongamos que un cliente admite Unicode y necesita recuperar el nombre para mostrar de una carpeta. Todas las propiedades de PT_TSTRING cliente se compilan para escribir PT_UNICODE. Cuando el cliente llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), pasa la marca MAPI_UNICODE para solicitar que la cadena de nombre para mostrar se devuelva en formato Unicode. 
  
Los clientes y proveedores de servicios deben tener en cuenta que especificar un juego de caracteres en una llamada de método es solo una solicitud. La compatibilidad con uno o ambos conjuntos de caracteres es cosa del implementador del objeto. Sin embargo, se recomienda a los proveedores de servicios que admitan ambos conjuntos de caracteres porque les permite lograr una distribución más generalizada que los proveedores que solo admiten un conjunto. 
  
Las propiedades de cadena pueden crecer hasta ser bastante grandes como las propiedades binarias( propiedades que usan el tipo de propiedad PT_BINARY. Para facilitar el trabajo con propiedades de gran tamaño, MAPI permite a los proveedores de servicios establecer estas propiedades para aplicar límites de tamaño. Estos límites pueden variar en función de:
  
- Si las propiedades se leen o escriben.
    
- Cómo implementa el proveedor de servicios los **métodos IMAPIProp.** 
    
- Consideraciones en tiempo de ejecución, como restricciones de memoria.
    
- Problemas de traducción de juego de caracteres. 
    
Los límites de tamaño también se pueden colocar en propiedades binarias y de cadena cuando se usan en el conjunto de columnas de una tabla porque a veces es imposible hacer visible todo el valor de una propiedad grande. Muchos proveedores de servicios truncan las propiedades binarias o de cadena de gran tamaño que se usan en las tablas a 255 bytes. 
  
Cuando un cliente llama al método **GetProps** o **SetProps** de un objeto para trabajar con una cadena de gran tamaño o una propiedad binaria y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY. Si se trata de **GetProps** que está fallando para una propiedad específica, el cliente puede recuperar llamando a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitando el **IStream** para obtener acceso especificando IID_IStream como identificador de interfaz. Con **OpenProperty,** el cliente puede recuperar una propiedad grande mediante una interfaz como **IStream** que sea más adecuada para trabajar con propiedades de gran tamaño. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

