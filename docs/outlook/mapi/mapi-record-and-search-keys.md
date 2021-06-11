---
title: Claves de registro y búsqueda MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434567"
---
# <a name="mapi-record-and-search-keys"></a>Claves de registro y búsqueda MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las claves de registro y las claves de búsqueda son identificadores binarios que se asignan a muchos objetos MAPI. A diferencia del identificador de entrada de un objeto, su clave de registro o búsqueda es directamente comparable y transmitible. 
  
## <a name="record-keys"></a>Claves de registro

Se usa una clave de registro para comparar dos objetos. Los objetos de almacén de mensajes y libreta de direcciones deben tener claves de registro, que se almacenan en **su propiedad PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Dado que una clave de registro identifica un objeto y no sus datos, cada instancia de un objeto tiene una clave de registro única. El ámbito de una clave de registro para carpetas y mensajes es el almacén de mensajes. El ámbito de los contenedores de libreta de direcciones, los usuarios de mensajería y las listas de distribución es el conjunto de contenedores de nivel superior proporcionado por MAPI para su uso en la libreta de direcciones integrada.
  
Las claves de registro se pueden duplicar en otro recurso. Por ejemplo, los mensajes diferentes en dos almacenes de mensajes diferentes pueden tener la misma clave de registro. Esto es diferente de los identificadores de entrada a largo plazo; dado que los identificadores de entrada a largo plazo contienen una referencia al proveedor de servicios, tienen un ámbito más amplio. La clave de registro de un almacén de mensajes es similar en el ámbito a un identificador de entrada a largo plazo; debe ser único en todos los proveedores de almacén de mensajes. Para garantizar esta singularidad, los proveedores de almacenes de mensajes suelen establecer su clave de registro en un valor que es la combinación de su propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) y un identificador que es único para el almacén de mensajes.
  
## <a name="search-keys"></a>Claves de búsqueda

Se usa una clave de búsqueda para comparar los datos en dos objetos. La clave de búsqueda de un objeto se almacena en **su propiedad PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Dado que una clave de búsqueda representa los datos de un objeto y no el propio objeto, dos objetos diferentes con los mismos datos pueden tener la misma clave de búsqueda. Cuando se copia un objeto, por ejemplo, tanto el objeto original como su copia tienen los mismos datos y la misma clave de búsqueda.
  
Los mensajes y los usuarios de mensajería tienen claves de búsqueda. La clave de búsqueda de un mensaje es un identificador único de los datos del mensaje. Los proveedores de almacén de mensajes ofrecen la propiedad **PR_SEARCH_KEY** de un mensaje en el momento de la creación del mensaje. La clave de búsqueda de una entrada de libreta de direcciones se calcula a partir de su tipo de dirección (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) y dirección (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si la entrada de la libreta de direcciones es grabable, es posible que su clave de búsqueda no esté disponible hasta que el tipo de dirección y la dirección se hayan establecido mediante el método [IMAPIProp::SetProps](imapiprop-setprops.md) y la entrada se haya guardado mediante el método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Cuando cambian estas propiedades de dirección, es posible que la clave de búsqueda correspondiente no se sincronice con los nuevos valores hasta que los cambios se hayan confirmado con una **llamada SaveChanges.** 
  
El valor de la clave de registro de un objeto puede ser igual o diferente que el valor de su clave de búsqueda, según el proveedor de servicios. Algunos proveedores de servicios usan el mismo valor para la clave de búsqueda, la clave de registro y el identificador de entrada de un objeto. Otros proveedores de servicios asignan valores únicos para cada uno de los identificadores de sus objetos. 
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

