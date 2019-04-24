---
title: Claves de búsqueda y registro MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328137"
---
# <a name="mapi-record-and-search-keys"></a>Claves de búsqueda y registro MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las claves de registro y las claves de búsqueda son identificadores binarios que se asignan a muchos objetos MAPI. A diferencia del identificador de entrada de un objeto, su registro o clave de búsqueda es directamente comparable y transmite. 
  
## <a name="record-keys"></a>Claves de registro

Una clave de registro se usa para comparar dos objetos. Los objetos del almacén de mensajes y la libreta de direcciones deben tener claves de registro, que se almacenan en su propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Debido a que una clave de registro identifica un objeto y no sus datos, cada instancia de un objeto tiene una clave de registro única. El ámbito de una clave de registro para carpetas y mensajes es el almacén de mensajes. El ámbito de los contenedores de la libreta de direcciones, los usuarios de mensajería y las listas de distribución es el conjunto de contenedores de nivel superior proporcionados por MAPI para su uso en la libreta de direcciones integrada.
  
Las claves de registro se pueden duplicar en otro recurso. Por ejemplo, diferentes mensajes en dos almacenes de mensajes diferentes pueden tener la misma clave de registro. Esto es diferente de los identificadores de entrada a largo plazo; como los identificadores de entrada a largo plazo contienen una referencia al proveedor de servicios, tienen un ámbito más amplio. La clave de registro de un almacén de mensajes es similar en el ámbito a un identificador de entrada a largo plazo; debe ser único en todos los proveedores de almacenamiento de mensajes. Para garantizar esta exclusividad, los proveedores de almacenamiento de mensajes normalmente establecen su clave de registro en un valor que es la combinación de su propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) y un identificador que es único para el almacén de mensajes.
  
## <a name="search-keys"></a>Teclas de búsqueda

Se usa una clave de búsqueda para comparar los datos de dos objetos. La clave de búsqueda de un objeto se almacena en su propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Dado que una clave de búsqueda representa los datos de un objeto y no el propio objeto, dos objetos distintos con los mismos datos pueden tener la misma clave de búsqueda. Cuando se copia un objeto, por ejemplo, tanto el objeto original como su copia tienen los mismos datos y la misma clave de búsqueda.
  
Los usuarios de mensajes y mensajería tienen claves de búsqueda. La clave de búsqueda de un mensaje es un identificador único de los datos del mensaje. Los proveedores de almacenamiento de mensajes suministran la propiedad **PR_SEARCH_KEY** de un mensaje en el momento de crear el mensaje. La clave de búsqueda de una entrada de la libreta de direcciones se calcula a partir de su tipo de dirección (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) y dirección (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si la entrada de la libreta de direcciones es grabable, es posible que su clave de búsqueda no esté disponible hasta que se establezca el tipo de dirección y la dirección mediante el método [IMAPIProp:: SetProps](imapiprop-setprops.md) y se haya guardado la entrada con el método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Cuando estas propiedades de dirección cambian, es posible que la clave de búsqueda correspondiente no se sincronice con los nuevos valores hasta que los cambios se hayan confirmado con una llamada de **SaveChanges** . 
  
El valor de la clave de registro de un objeto puede ser el mismo o diferente que el valor de la clave de búsqueda, según el proveedor de servicios. Algunos proveedores de servicios usan el mismo valor para la clave de búsqueda, la clave de registro y el identificador de entrada de un objeto. Otros proveedores de servicios asignan valores únicos para cada uno de los identificadores de los objetos. 
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

