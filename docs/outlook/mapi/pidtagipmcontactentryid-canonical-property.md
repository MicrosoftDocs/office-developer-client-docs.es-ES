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
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327905"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>Propiedad canónica PidTagIpmContactEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el **EntryID de** la Outlook contactos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D1  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Carpeta  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes. Para obtener acceso a la propiedad en un almacén de mensajes específico, haga lo siguiente: 
  
1. En primer lugar, busque la propiedad en la carpeta Bandeja de entrada. Use **IMsgStore::GetReceiveFolder** para obtener una referencia al **EntryID** de la carpeta Bandeja de entrada. 
    
2. Si **IMsgStore::GetReceiveFolder** se realiza correctamente, use la referencia al **EntryID** de la Bandeja de entrada e **IMsgStore::OpenEntry** para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder.** 
    
3. Si **IMsgStore::OpenEntry** se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada. 
    
4. Si se produce un error en los pasos 1, 2 o 3, busque la propiedad en la carpeta raíz. Para ello, use **IMsgStore::OpenEntry**, especificando NULL para ** lpEntryID **, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder.** 
    
5. Si la apertura de la carpeta raíz se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para crear y localizar las carpetas especiales en un buzón.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

