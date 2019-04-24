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
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309523"
---
# <a name="mapi-string-properties"></a>Propiedades de la cadena MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona tres tipos de propiedades diferentes para describir las propiedades de cadena:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Las propiedades de cadena suelen definirse como PT_TSTRING. El tipo de propiedad PT_TSTRING se compila condicionalmente a uno de los otros tipos de propiedades de cadena, en función de si se ha definido la macro uniCODE. PT_STRING8 describe las cadenas de caracteres terminadas en NULL de 8 bits en formato ANSI; PT_UNICODE describe las cadenas de caracteres de doble byte terminadas en NULL. 
  
Un cliente o proveedor de servicios, o bien el cliente y el proveedor pueden elegir admitir cadenas de caracteres Unicode. No es necesario. Un cliente que admite sólo cadenas PT_STRING8 puede operar con un proveedor compatible con Unicode y viceversa. Para habilitar esta interoperabilidad, los clientes y los proveedores de servicios pasan una marca, la marca MAPI_UNICODE, para indicar que se admite Unicode en los métodos que implican el intercambio de cadenas de caracteres. 
  
Por ejemplo, supongamos que un cliente es compatible con Unicode y necesita recuperar el nombre para mostrar de una carpeta. Todas las propiedades de PT_TSTRING del cliente se compilan en el tipo PT_UNICODE. Cuando el cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), pasa la marca MAPI_UNICODE para solicitar que la cadena de nombre para mostrar se devuelva en el formato Unicode . 
  
Los clientes y los proveedores de servicios deben tener en cuenta que especificar un juego de caracteres en una llamada de método es solo una solicitud. La compatibilidad con uno o ambos conjuntos de caracteres depende del implementador del objeto. Sin embargo, se recomienda a los proveedores de servicios que admitan ambos conjuntos de caracteres porque les permite obtener una distribución más extendida que los proveedores que admiten un solo conjunto. 
  
Las propiedades de cadena pueden crecer para ser bastante grandes como propiedades binarias — propiedades que usan el tipo de propiedad PT_BINARY. Para facilitar el trabajo con propiedades grandes, MAPI permite que los proveedores de servicios establezcan estas propiedades para exigir límites de tamaño. Estos límites pueden variar en función de:
  
- Si las propiedades se van a leer o escribir.
    
- Cómo implementa el proveedor de servicios los métodos **IMAPIProp** . 
    
- Consideraciones de tiempo de ejecución, como las restricciones de memoria.
    
- Problemas de traducción del juego de caracteres. 
    
Los límites de tamaño también se pueden colocar en propiedades binarias y de cadena cuando se utilizan en el conjunto de columnas de una tabla porque a veces es imposible hacer visible todo el valor de una propiedad grande. Muchos proveedores de servicios truncan las propiedades binarias o de cadena de gran tamaño que se usan en las tablas a 255 bytes. 
  
Cuando un cliente llama a un método **GetProps** o **SetProps** de un objeto para trabajar con una propiedad binaria o de cadena de gran tamaño y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY. Si es **GetProps** que produce errores en una propiedad específica, el cliente puede recuperarse llamando a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y solicitando a **IStream** el acceso especificando IID_IStream como identificador de interfaz. Con **OpenProperty**, el cliente puede recuperar una propiedad grande mediante una interfaz como **IStream** , que es más adecuada para trabajar con propiedades grandes. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

