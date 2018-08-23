---
title: Recuperación de propiedades MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 1404239a54f9b8991099a66831e3364d9a683d1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566337"
---
# <a name="retrieving-mapi-properties"></a>Recuperación de propiedades MAPI

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un proveedor de servicio o cliente, recupera una propiedad de un objeto, el objeto pone a disposición identificador, tipo y valor de la propiedad. 
  
Los clientes y proveedores de servicios pueden recuperar propiedades de un objeto mediante una llamada a uno de estos procedimientos:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
El método **GetProps** se usa para recuperar una o varias propiedades que no necesitan una interfaz especializada o alternativa para el acceso. Esto implica que las propiedades disponibles con **GetProps** son pequeñas, como enteros y valores booleanos. 
  
 **Para recuperar las propiedades de varios**
  
1. Asignar una estructura de [elemento SPropTagArray](sproptagarray.md) suficientemente grande para contener el número de propiedades que se va a recuperar. 
    
2. Establezca al miembro **cValues** de la estructura del **elemento SPropTagArray** en el número de propiedades que se recuperan y miembro del grupo de cada **aulPropTag** para el identificador y el tipo, si es posible, de una de las propiedades de destino. Si el tipo es desconocido, establézcalo en PT_UNSPECIFIED. Si el tipo y el identificador están desconocidas, busque esta información mediante una llamada a [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** devuelve una matriz de etiqueta (propiedad) con todas las propiedades del objeto compatibles. Si sólo hay disponible un nombre de propiedad, llame a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener acceso al identificador asociado. 
    
3. Llame a [IMAPIProp::GetProps](imapiprop-getprops.md) para abrir la propiedad o propiedades. 
    
El método **OpenProperty** se usa para abrir propiedades más grandes que requieren una interfaz alternativa como **IStream** o [IMAPITable](imapitableiunknown.md) para el acceso. **OpenProperty** normalmente se usa para abrir la cadena de caracteres de gran tamaño, binario y las propiedades del objeto y sólo se puede abrir una propiedad a la vez. Los autores de llamadas pasan el identificador de la interfaz adicional que se requiere como uno de los parámetros de entrada. 
  
Algunos de los usos comunes de **OpenProperty** incluyen la apertura de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad que contiene el cuerpo de un mensaje basado en texto, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propiedad que contiene un Datos adjuntos de mensaje o el objeto OLE y **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propiedad que contiene una tabla de contenido de un contenedor de libreta direcciones o la carpeta. 
  
Dependiendo de la propiedad, se solicita una interfaz diferente de **OpenProperty**. **IStream**, una interfaz que permite que los datos de propiedad se puede leer y escribir como una secuencia de bytes, normalmente se usa para tener acceso a **PR_BODY**. [IMessage](imessageimapiprop.md) o **IStream** puede utilizarse para tener acceso a **PR_ATTACH_DATA_OBJ**. Datos adjuntos de incrustación de mensajes que son mensajes estándares utilizan **IMessage** mientras que los mensajes en el formato TNEF usar **IStream**. Debido a que **PR_CONTAINER_CONTENTS** es un objeto table, se tiene acceso con [IMAPITable](imapitableiunknown.md).
  
 **Para recuperar PR_ATTACH_DATA_BIN propiedad un documento adjunto**
  
1. Llame a la función [OpenStreamOnFile](openstreamonfile.md) para abrir una secuencia para el archivo. 
    
2. Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para recuperar la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) con la interfaz **IStream** . Establecer los indicadores de la MAPI_MODIFY y la MAPI_CREATE. 
    
3. Asignar una estructura **STATSTG** y pasar en una llamada al método de la secuencia archivo **IStream:: Stat** para determinar su tamaño. Otra forma de determinar el tamaño de la secuencia es llamar a **IStream:: Seek** con la marca STREAM_SEEK_END. 
    
4. Llame al método de la secuencia **IStream:: CopyTo** para copiar los datos de secuencia del archivo en la secuencia de datos adjuntos. 
    
5. Cuando finalice la operación de copia, versión ambas secuencias llamando a sus métodos **IUnknown:: Release** . 
    
Cuando se usa **IStream** para el acceso de propiedad, algunos proveedores de servicios de envían automáticamente el tamaño de la propiedad con la secuencia. Llamar a **OpenProperty** con el MAPI_DEFERRED_ERRORS marca puede retrasar la apertura de la propiedad y la devolución del tamaño de la secuencia. Si se llama a **IStream:: Stat** para recuperar este tamaño después de **OpenProperty** con el MAPI_DEFERRED_ERRORS marcador establecido, se verán afectado el rendimiento debido a que esta secuencia de llamadas obliga a una llamada a procedimiento remoto adicional. Para evitar la pérdida de rendimiento, los clientes pueden llamar a cualquier método MAPI entre las llamadas a **OpenProperty** y a **Stat**.
  
La función [HrGetOneProp](hrgetoneprop.md) , al igual que **OpenProperty**, abre una propiedad a la vez. **HrGetOneProp** sólo se debe utilizar cuando el objeto de destino no existe en el equipo local. Cuando el objeto de destino no está disponible localmente, se puede producir utilizando **HrGetOneProp** repetidamente en varias llamadas a procedimiento remoto y una degradación del rendimiento. 
  
Los autores de llamadas que necesitan varias propiedades pueden llamar **HrGetOneProp** o **OpenProperty** en un bucle o realizar una llamada a **GetProps**. Llamar a **GetProps** una vez es más eficaz. 
  
> [!NOTE]
> Propiedades seguras no están disponibles automáticamente con otras propiedades en una llamada **GetProps**, **HrGetOneProp**o **GetPropList** . Propiedades seguras deben solicitarla explícitamente con sus identificadores de propiedad. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

