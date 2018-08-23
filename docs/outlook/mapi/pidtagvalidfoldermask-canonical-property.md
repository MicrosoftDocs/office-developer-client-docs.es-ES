---
title: Propiedad canónica PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 605e2f528ea0afc1a35348320abaffeb142d9921
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590725"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Propiedad canónica PidTagValidFolderMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcadores que indican la validez de los identificadores de entrada de las carpetas en un almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Identificador:  <br/> |0x35DF  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Identificador de entrada de una carpeta puede no ser válido si un usuario elimina la carpeta o si se daña el almacén de mensajes.
  
La máscara de bits se pueden establecer uno o varios de los siguientes indicadores: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> La carpeta vistas comunes tiene un identificador de entrada válido. Vea **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> La carpeta del finder tiene un identificador de entrada válido. Vea **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Recibe el mensaje interpersonal (IPM) carpeta tiene un identificador de entrada válido. Vea [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> La carpeta Bandeja de salida IPM tiene un identificador de entrada válido. Vea **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> La carpeta Elementos enviados de IPM tiene un identificador de entrada válido. Vea **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> El subárbol de carpeta IPM tiene un identificador de entrada válido. Vea **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> La carpeta Elementos eliminados de IPM tiene un identificador de entrada válido. Vea **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> La carpeta vistas tiene un identificador de entrada válido. Vea **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

