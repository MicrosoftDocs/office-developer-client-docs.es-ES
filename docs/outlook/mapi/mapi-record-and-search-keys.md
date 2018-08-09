---
title: Registro MAPI y las claves de búsqueda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e1b05be64029f80ec8a7379ed7b313b9cf645fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818185"
---
# <a name="mapi-record-and-search-keys"></a>Registro MAPI y las claves de búsqueda

  
  
**Hace referencia a**: Outlook 
  
Claves de registro y las claves de búsqueda son identificadores binarios que se asignan a muchos objetos MAPI. A diferencia de identificador de entrada de un objeto, su clave de registro o búsqueda es directamente comparable, así como transmisible. 
  
## <a name="record-keys"></a>Claves de registro

Una clave de registro se usa para comparar dos objetos. Almacén de mensajes y dirección de objetos book deben tener las claves de registro, que se almacenan en su propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Debido a que una clave de registro identifica un objeto y no sus datos, cada instancia de un objeto tiene una clave de registro único. El ámbito de una clave de registro para las carpetas y los mensajes es el almacén de mensajes. El ámbito de los contenedores de la libreta de direcciones, los usuarios de mensajería y listas de distribución es el conjunto de contenedores de nivel superior proporcionado por MAPI para su uso en la libreta de direcciones integrada.
  
Claves de registro se pueden duplicar en otro recurso. Por ejemplo, distintos de los mensajes en dos almacenes de mensaje distinto pueden tener la misma clave de registro. Esto es diferente de los identificadores de entrada a largo plazo; debido a que los identificadores de entrada a largo plazo contienen una referencia al proveedor de servicios, que tienen un ámbito más amplio. Clave de registro de un almacén de mensajes es similar en el ámbito a un identificador de entrada a largo plazo; debe ser único entre todos los proveedores de almacén de mensajes. Para garantizar esta exclusividad, los proveedores de almacén de mensajes normalmente establecen su clave de registro en un valor que es la combinación de su propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) y un identificador único para el almacén de mensajes.
  
## <a name="search-keys"></a>Claves de búsqueda

Una clave de búsqueda se usa para comparar los datos en dos objetos. Clave de búsqueda de un objeto se almacena en su propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Debido a que una clave de búsqueda representa los datos de un objeto y no el propio objeto, dos objetos diferentes con los mismos datos pueden tener la misma clave de búsqueda. Cuando se copia un objeto, por ejemplo, el objeto original y su copia tienen los mismos datos y la misma clave de búsqueda.
  
Los mensajes y los usuarios de mensajería tienen claves de búsqueda. La clave de búsqueda de un mensaje es un identificador único de los datos del mensaje. Los proveedores de almacén de mensajes presentar la propiedad **PR_SEARCH_KEY** de un mensaje a la hora de creación del mensaje. La clave de búsqueda de una entrada de la libreta de direcciones se calcula a partir de su tipo de dirección (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) y dirección (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si la entrada de la libreta de direcciones es grabable, su clave de búsqueda puede no estar disponible hasta que se han establecido mediante el método [IMAPIProp::SetProps](imapiprop-setprops.md) el tipo de dirección y la dirección y la entrada se ha guardado mediante el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Al cambian estas propiedades de dirección, es posible que la clave de búsqueda correspondiente no que se sincronizará con los nuevos valores hasta que los cambios se han confirmado con una llamada de **SaveChanges** . 
  
El valor de la clave de registro de un objeto puede ser igual o diferente que el valor de su clave de búsqueda, según el proveedor de servicio. Algunos proveedores de servicios de usan el mismo valor de clave de búsqueda de un objeto, la clave de registro y el identificador de entrada. Otros proveedores de servicios de asignan valores únicos para cada uno de los identificadores de sus objetos. 
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

