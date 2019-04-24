---
title: Propiedad canónica PidTagAdditionalRenEntryIdsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335206"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propiedad canónica PidTagAdditionalRenEntryIdsEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los identificadores de entrada de una carpeta especial para un objeto Store. Cada entrada de esta propiedad de varios valores se puede asignar a uno o varios identificadores de entrada, es decir, hay una relación de uno a varios entre una entrada y sus identificadores de entrada asociados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificador:  <br/> |0x36D9  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se usa esta propiedad, contiene una matriz de bloques que especifica los identificadores de entrada de las carpetas. Los bloques siguen el formato especificado por las cuatro tablas siguientes.
  
**Bloque PersistData**

|**Name**|**Type**|**Size**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |segundo  <br/> |Tipo: valor del identificador de esta entrada de **PersistData** . Consulte la tabla "valores de PersistBlockType" para ver la lista de valores válidos.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |segundo  <br/> |Tamaño, en bytes, del campo de **los elementos** de la misma.  <br/> |
|**Elementos de elemento de la** <br/> |matriz de bloques **PersistElement**  <br/> |variable  <br/> |Indica cuántas entradas de **PersistElement** existen para la tienda. Consulte la tabla "bloque PersistElement" para obtener el formato de esta estructura.  <br/> |
   
**Valores de PersistBlockType**

|**Nombre**|**Value**|**Descripción**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indica que no se procesarán más bloques **PersistData** .  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indica que este bloque contiene datos para la carpeta suscripciones RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indica que este bloque contiene datos para la carpeta de procesamiento de correo con seguimiento.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indica que este bloque contiene datos para la carpeta de búsqueda de tareas pendientes.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indica que este bloque contiene datos para la carpeta de configuración de la acción de conversación.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Este valor está reservado.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indica que este bloque contiene datos para la carpeta de contactos sugerida.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indica que este bloque contiene datos para la carpeta de búsqueda contactos.  <br/> Usado solo por Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indica que este bloque contiene datos para la carpeta de listas de contactos de mensajería instantánea (mi). La carpeta a la que se hace referencia contiene listas de distribución personales (PDLs) que representan todos los grupos de la lista de contactos de mensajería instantánea.  <br/> Usada por Outlook y Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indica que este bloque contiene datos para la carpeta contactos de mensajería instantánea. La carpeta a la que se hace referencia contiene los contactos individuales a los que hacen referencia los grupos de listas de contactos de mensajería instantánea.  <br/> Usada por Outlook y Exchange.  <br/> |
   
Si el valor de **PersistBlockType** no es uno de los definidos aquí, el bloque **PersistData** se ignora y el procesamiento continúa hasta que se procesa un **PersistID** PERSIST_SENTINEL o hasta que se alcanza el final de la secuencia. 
  
**PersistElementBlock**

|**Name**|**Type**|**Size**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |segundo  <br/> |Especifica el valor del identificador de tipo para este bloque **PersistElement** . Consulte la tabla "valores de PersistElementType" para obtener una lista de valores válidos.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |segundo  <br/> |Especifica el tamaño, en bytes, del campo **ElementData** .  <br/> |
|**ElementData** <br/> |matriz de datos binarios  <br/> |variable  <br/> |Contiene los datos de este par de **PersistID** + **ElementID** .  <br/> |
   
**Valores de PersistElementType**

|**Nombre**|**Value**|**Valor de ElementDataSize**|**Descripción**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indica que el campo **ElementData** de este bloque contiene un valor de encabezado DWORD. El modo en que se interpreta este valor depende del tipo **PersistID** del bloque.  <br/> Para todos los tipos de **PersistID** especificados en [[ms-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), este valor es cero.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variable  <br/> |Indica que este bloque contiene la propiedad **EntryID** de la carpeta especificada por **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indica que no se procesarán más bloques **PersistElement** .  <br/> |
   
Si el valor **PersistElementType** no es uno de los definidos aquí, el bloque **PersistElement** se ignora y el procesamiento continúa hasta que se procesa un ELEMENT_SENTINEL **ElementID** o hasta que se alcanza el final de la secuencia. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica y marca los mensajes de correo electrónico diseñados para engañar a los destinatarios para que divulguen información confidencial (como contraseñas y otra información personal) a un origen que no es de confianza.
    
### <a name="header-files"></a>Archivos de encabezado

Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

