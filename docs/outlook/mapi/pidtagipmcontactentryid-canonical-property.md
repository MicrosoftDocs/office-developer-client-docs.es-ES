---
title: Propiedad canónica PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c09d4848373a530e80298d6c01ad3d411d9eb60e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567415"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>Propiedad canónica PidTagIpmContactEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la **propiedad EntryID** de la carpeta de contactos de Outlook. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D1  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes. Para obtener acceso a la propiedad en un almacén de mensajes específicos, haga lo siguiente: 
  
1. En primer lugar, busque la propiedad en la carpeta Bandeja de entrada. Utilice **IMsgStore::GetReceiveFolder** para obtener una referencia a la **propiedad EntryID** de la carpeta Bandeja de entrada. 
    
2. Si **IMsgStore::GetReceiveFolder** se realiza correctamente, a continuación, usar la referencia a la **propiedad EntryID** de la Bandeja de entrada y **IMsgStore::OpenEntry** para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** . 
    
3. Si **IMsgStore::OpenEntry** se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada. 
    
4. Si se produce un error en el paso 1, 2 o 3, busque la propiedad en la carpeta raíz. Para ello, use **IMsgStore::OpenEntry**, especificar NULL para ** lpEntryID **, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** . 
    
5. Si abrir la carpeta raíz se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad que desee. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.
    
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

