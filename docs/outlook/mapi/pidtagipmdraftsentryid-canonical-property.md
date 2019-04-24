---
title: Propiedad canónica PidTagIpmDraftsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327891"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a>Propiedad canónica PidTagIpmDraftsEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la propiedad **EntryID** de la carpeta Borradores de Outlook. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IPM_DRAFTS_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D7  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se almacena en la carpeta Bandeja de entrada, así como en la carpeta raíz del almacén de mensajes. Para obtener acceso a la propiedad en un almacén de mensajes específico, haga lo siguiente: 
  
1. En primer lugar, busque la propiedad en la carpeta Bandeja de entrada. Use [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para obtener una referencia a la propiedad **EntryID** de la carpeta Bandeja de entrada. 
    
2. Si **IMsgStore:: GetReceiveFolder** se realiza correctamente, use la referencia a **EntryID** de la bandeja de entrada y [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir la bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** . 
    
3. Si **IMsgStore:: OpenEntry** se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener la propiedad deseada. 
    
4. Si se produce un error en el paso 1, 2 o 3, busque la propiedad en la carpeta raíz. Para ello, use **IMsgStore:: OpenEntry**, especificando null para **lpEntryID**, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** . 
    
5. Si la carpeta raíz se abre correctamente, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp:: GetProps** para obtener la propiedad deseada. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.
    
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

