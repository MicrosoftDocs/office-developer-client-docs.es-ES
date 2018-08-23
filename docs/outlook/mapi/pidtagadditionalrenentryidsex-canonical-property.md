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
ms.openlocfilehash: fcea014ca4c1b1629505127484c44ae990eed855
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590809"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propiedad canónica PidTagAdditionalRenEntryIdsEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la entrada de carpeta especial los identificadores de un objeto store. Cada entrada de esta propiedad con varios valores se puede asignar a uno o varios de los identificadores de entrada, es decir, hay una relación uno a varios entre una entrada y su identificadores de entrada asociada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificador:  <br/> |0x36D9  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad se utiliza, contiene una matriz de bloques que especifica los identificadores de entrada para las carpetas. Los bloques de seguir el formato especificado por las siguientes cuatro tablas.
  
**Bloque de PersistData**

|**Nombre**|**Tipo**|**Size**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Escriba el valor de identificador para esta entrada de **PersistData** . Vea la tabla "Valores de PersistBlockType" para la lista de valores válidos.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Tamaño, en bytes, del campo **DataElements** .  <br/> |
|**DataElements** <br/> |matriz de bloques de **PersistElement**  <br/> |variable  <br/> |Indica cuántas entradas **PersistElement** existen para el almacén. Consulte la tabla "PersistElement Block" para el formato de esta estructura.  <br/> |
   
**Valores de PersistBlockType**

|**Nombre**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indica que no hay más bloques de **PersistData** se procesará.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0 x 8001  <br/> |Indica que este bloque contiene datos para la carpeta suscripciones RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indica que este bloque contiene datos para la carpeta realiza un seguimiento de procesamiento de correo.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0 x 8004  <br/> |Indica que este bloque contiene datos para la carpeta de búsqueda de tareas pendientes.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indica que este bloque contiene datos para la carpeta de configuración de la acción de conversación.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0 x 8007  <br/> |Este valor está reservado.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indica que este bloque contiene datos de la carpeta Contactos sugeridos.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indica que este bloque contiene datos para la carpeta de búsqueda de contactos.  <br/> Usa sólo en Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indica que este bloque contiene datos para la carpeta de listas de contactos de mensajería instantánea (mi). La carpeta que se hace referencia contiene listas de distribución personales (propias PDL) que representa a cada grupo dentro de la lista de contactos de mensajería instantánea.  <br/> Utilizado por Outlook y Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indica que este bloque contiene datos para la carpeta de contactos de mensajería instantánea. La carpeta que se hace referencia contiene los contactos individuales que se hace referencia a los grupos de la lista de contactos de mensajería instantánea.  <br/> Utilizado por Outlook y Exchange.  <br/> |
   
Si el valor de **PersistBlockType** no es uno de los que se define aquí, se omite el bloque de **PersistData** y procesamiento continúa hasta que se procesa una PERSIST_SENTINEL **PersistID** o se alcanza el final de la secuencia. 
  
**PersistElementBlock**

|**Nombre**|**Tipo**|**Size**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Especifica el valor de identificador de tipo para este bloque **PersistElement** . Vea la tabla "Valores de PersistElementType" para obtener una lista de valores válidos.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Especifica el tamaño, en bytes, del campo **ElementData** .  <br/> |
|**ElementData** <br/> |matriz de datos binarios  <br/> |variable  <br/> |Contiene los datos para este **PersistID** + **ElementID** par.  <br/> |
   
**Valores de PersistElementType**

|**Nombre**|**Valor**|**Valor de ElementDataSize**|**Descripción**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indica que el campo de **ElementData** de este bloque contiene un valor de encabezado de DWORD. Cómo se interpreta este valor depende de tipo de **PersistID** del bloque.  <br/> Para todos los tipos de **PersistID** especificados en [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), este valor es cero.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0 x 0001  <br/> |variable  <br/> |Indica que este bloque contiene la **propiedad EntryID** de la carpeta especificada por **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indica que no hay más bloques de **PersistElement** se procesará.  <br/> |
   
Si el valor de **PersistElementType** no es uno de los que se define aquí, se omite el bloque de **PersistElement** y procesamiento continúa hasta que se procesa una ELEMENT_SENTINEL **ElementID** o se alcanza el final de la secuencia. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica y marca los mensajes de correo electrónico que están diseñados para engañar a los destinatarios para que divulguen información confidencial (por ejemplo, las contraseñas y otra información personal) a un origen no confiable.
    
### <a name="header-files"></a>Archivos de encabezado

Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

