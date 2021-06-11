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
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417087"
---
# <a name="retrieving-mapi-properties"></a>Recuperación de propiedades MAPI

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un cliente o proveedor de servicios recupera una propiedad de un objeto, el objeto pone a disposición el valor, el tipo y el identificador de la propiedad. 
  
Los clientes y proveedores de servicios pueden recuperar las propiedades de un objeto llamando a una de las siguientes opciones:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
El **método GetProps** se usa para recuperar una o más propiedades que no necesitan una interfaz especializada o alternativa para el acceso. Esto implica que las propiedades disponibles con **GetProps** son pequeñas, como enteros y valores booleanos. 
  
 **Para recuperar varias propiedades**
  
1. Asigne una [estructura SPropTagArray](sproptagarray.md) lo suficientemente grande como para contener el número de propiedades que se recuperarán. 
    
2. Establezca el **miembro cValues** de la estructura **SPropTagArray** en el número de propiedades que se recuperarán y establezca cada miembro **de aulPropTag** en el identificador y escriba, si es posible, una de las propiedades de destino. Si el tipo es desconocido, estadóla en PT_UNSPECIFIED. Si el tipo y el identificador son desconocidos, busque esta información llamando a [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList devuelve** una matriz de etiquetas de propiedad con todas las propiedades admitidas del objeto. Si solo hay un nombre de propiedad disponible, llama [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener acceso al identificador asociado. 
    
3. Llama [a IMAPIProp::GetProps](imapiprop-getprops.md) para abrir la propiedad o las propiedades. 
    
El **método OpenProperty** se usa para abrir propiedades más grandes que requieren una interfaz alternativa, como **IStream** o [IMAPITable](imapitableiunknown.md) para el acceso. **OpenProperty** se suele usar para abrir propiedades de cadena de caracteres grandes, binarias y de objeto y solo puede abrir una propiedad a la vez. Los autores de llamadas pasan el identificador de la interfaz adicional necesaria como uno de los parámetros de entrada. 
  
Algunos de los usos comunes de **OpenProperty** incluyen abrir **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad que contiene el cuerpo de un mensaje basado en texto, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propiedad que contiene un objeto OLE o datos adjuntos de mensajes y **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propiedad que contiene una carpeta o tabla de contenido de contenedor de libreta de direcciones. 
  
Según la propiedad, se solicita una interfaz diferente a **OpenProperty**. **IStream**, una interfaz que permite leer y escribir datos de propiedades como una secuencia de bytes, se usa normalmente para obtener acceso a **PR_BODY**. Se [puede usar IMessage](imessageimapiprop.md) **o IStream** para obtener acceso a **PR_ATTACH_DATA_OBJ**. Los datos adjuntos de mensajes incrustados que son mensajes estándar usan **IMessage,** mientras que los mensajes en formato TNEF usan **IStream**. Dado **PR_CONTAINER_CONTENTS** es un objeto table, se tiene acceso a él con [IMAPITable](imapitableiunknown.md).
  
 **Para recuperar la propiedad PR_ATTACH_DATA_BIN datos adjuntos**
  
1. Llame a [la función OpenStreamOnFile](openstreamonfile.md) para abrir una secuencia para el archivo. 
    
2. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para recuperar la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) con la **interfaz IStream.** Establezca las marcas MAPI_MODIFY y MAPI_CREATE. 
    
3. Asigne una **estructura STATSTG** y pásala en una llamada al método **IStream::Stat** de la secuencia de archivos para determinar su tamaño. Otra forma de determinar el tamaño de secuencia es llamar a **IStream::Seek con** la marca STREAM_SEEK_END. 
    
4. Llame al método **IStream::CopyTo** de la secuencia para copiar los datos de la secuencia del archivo en la secuencia de datos adjuntos. 
    
5. Cuando finalice la operación de copia, libere ambas secuencias llamando a sus **métodos IUnknown::Release.** 
    
Cuando **se usa IStream** para el acceso a propiedades, algunos proveedores de servicios envían automáticamente el tamaño de la propiedad con la secuencia. Llamar **a OpenProperty** con MAPI_DEFERRED_ERRORS marca puede retrasar la apertura de la propiedad y el retorno del tamaño de la secuencia. Si se llama a **IStream::Stat** para recuperar este tamaño después de **OpenProperty** con la marca MAPI_DEFERRED_ERRORS establecida, el rendimiento se verá afectado porque esta secuencia de llamadas fuerza una llamada de procedimiento remoto adicional. Para evitar el impacto en el rendimiento, los clientes pueden llamar a cualquier método MAPI entre las llamadas a **OpenProperty** y **Stat**.
  
La [función HrGetOneProp,](hrgetoneprop.md) como **OpenProperty,** abre una propiedad a la vez. **HrGetOneProp** solo debe usarse cuando el objeto de destino existe en el equipo local. Cuando el objeto de destino no está disponible localmente, el uso de **HrGetOneProp** repetidamente puede provocar varias llamadas a procedimientos remotos y una degradación del rendimiento. 
  
Los autores de llamadas que necesitan varias propiedades pueden llamar a **HrGetOneProp** o **OpenProperty** en un bucle o realizar una llamada a **GetProps**. Llamar **a GetProps una** vez es más eficaz. 
  
> [!NOTE]
> Las propiedades seguras no están disponibles automáticamente con otras propiedades en una llamada **GetProps**, **HrGetOneProp** o **GetPropList.** Las propiedades seguras deben solicitarse explícitamente mediante sus identificadores de propiedad. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

