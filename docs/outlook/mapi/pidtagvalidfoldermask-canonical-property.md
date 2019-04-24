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
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360749"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Propiedad canónica PidTagValidFolderMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de máscara de marcas que indican la validez de los identificadores de entrada de las carpetas en un almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Identificador:  <br/> |0x35DF  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Almacén de mensajes MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El identificador de entrada de una carpeta puede dejar de ser válido si un usuario elimina la carpeta o si se daña el almacén de mensajes.
  
Se pueden establecer uno o varios de los siguientes indicadores para la máscara de la máscara: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> La carpeta vistas comunes tiene un identificador de entrada válido. Vea **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> La carpeta Finder tiene un identificador de entrada válido. Vea **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> La carpeta de recepción del mensaje interpersonal (IPM) tiene un identificador de entrada válido. Vea [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> La carpeta de la bandeja de salida IPM tiene un identificador de entrada válido. Vea **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> La carpeta elementos enviados de IPM tiene un identificador de entrada válido. Vea **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> El subárbol de la carpeta IPM tiene un identificador de entrada válido. Vea **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> La carpeta de elementos eliminados IPM tiene un identificador de entrada válido. Vea **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> La carpeta views tiene un identificador de entrada válido. Vea **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

