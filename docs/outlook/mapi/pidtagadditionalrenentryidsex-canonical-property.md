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
  
Contiene identificadores de entrada de carpeta especial para un objeto store. Cada entrada de esta propiedad multivalor se puede asignar a uno o más identificadores de entrada, es decir, hay una relación de uno a varios entre una entrada y sus identificadores de entrada asociados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificador:  <br/> |0x36D9  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Outlook aplicación  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se usa esta propiedad, contiene una matriz de bloques que especifica los identificadores de entrada de las carpetas. Los bloques siguen el formato especificado por las cuatro tablas siguientes.
  
**Bloque PersistData**

|**Nombre**|**Tipo**|**Tamaño**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Escriba el valor del identificador para **esta entrada PersistData.** Consulte la tabla "PersistBlockType Values" para obtener la lista de valores válidos.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Tamaño, en bytes, del **campo DataElements.**  <br/> |
|**DataElements** <br/> |matriz de **bloques PersistElement**  <br/> |variable  <br/> |Indica cuántas **entradas de PersistElement** existen para el almacén. Consulte la tabla "Bloque PersistElement" para obtener el formato de esta estructura.  <br/> |
   
**Valores de PersistBlockType**

|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indica que no se procesarán más **bloques PersistData.**  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indica que este bloque contiene datos de la carpeta Suscripciones RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indica que este bloque contiene datos de la carpeta Procesamiento de correo rastreado.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indica que este bloque contiene datos de la carpeta To-Do búsqueda.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indica que este bloque contiene datos para la carpeta De acción de Configuración conversación.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Este valor está reservado.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indica que este bloque contiene datos de la carpeta Contactos sugeridos.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indica que este bloque contiene datos de la carpeta Búsqueda de contactos.  <br/> Solo lo usa Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indica que este bloque contiene datos de la carpeta Listas de contactos de mensajería instantánea (MI). La carpeta a la que se hace referencia contiene listas de distribución personales (PDL) que representan cada grupo dentro de la lista de contactos de mensajería instantánea.  <br/> Se usa tanto Outlook como Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indica que este bloque contiene datos de la carpeta Contactos de mensajería instantánea. La carpeta a la que se hace referencia contiene los contactos individuales a los que hacen referencia los grupos de listas de contactos de mensajería instantánea.  <br/> Se usa tanto Outlook como Exchange.  <br/> |
   
Si el valor **PersistBlockType** no es uno de los definidos aquí, el bloque **PersistData** se omite y el procesamiento continúa hasta que se procesa **un persistID** de PERSIST_SENTINEL o se alcanza el final de la secuencia. 
  
**PersistElementBlock**

|**Nombre**|**Tipo**|**Tamaño**|**Descripción**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Especifica el valor del identificador de tipo para este **bloque PersistElement.** Vea la tabla "PersistElementType Values" para obtener una lista de valores válidos.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Especifica el tamaño, en bytes, del **campo ElementData.**  <br/> |
|**ElementData** <br/> |matriz de datos binarios  <br/> |variable  <br/> |Contiene los datos de este par **ElementID de PersistID.**  +    <br/> |
   
**Valores de PersistElementType**

|**Name**|**Valor**|**Valor de ElementDataSize**|**Descripción**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indica que el campo **ElementData de** este bloque contiene un valor de encabezado DWORD. La forma en que se interpreta este valor depende del tipo **PersistID del** bloque.  <br/> Para todos **los tipos persistID** especificados en [[MS-OXOSFLD],](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)este valor es cero.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variable  <br/> |Indica que este bloque contiene el **EntryID** de la carpeta especificada por **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indica que no se procesarán más bloques **PersistElement.**  <br/> |
   
Si el valor **PersistElementType** no es uno de los definidos aquí, el bloque **PersistElement** se omite y el procesamiento continúa hasta que se procesa un **elementID** de ELEMENT_SENTINEL o se alcanza el final de la secuencia. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para crear y localizar las carpetas especiales en un buzón.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica y marca los mensajes de correo electrónico diseñados para engañar a los destinatarios para que divulgen información confidencial (como contraseñas y otra información personal) a un origen no confiable.
    
### <a name="header-files"></a>Archivos de encabezado

Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

