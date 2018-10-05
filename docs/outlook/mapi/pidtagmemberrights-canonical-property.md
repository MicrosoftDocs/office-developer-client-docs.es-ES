---
title: Propiedad canónica PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397341"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propiedad canónica PidTagMemberRights

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un conjunto de bits que indica los derechos de este miembro en una carpeta o un buzón de correo.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificador:  <br/> |0x6673  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se utiliza con la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir los derechos de un miembro en una carpeta. Estos derechos se pueden mostrar y modificar. Los siguientes valores son los derechos definidos para esta propiedad. 
  
frightsReadAny
  
> Miembros pueden leer todos los mensajes.
    
frightsCreate
  
> Miembros pueden crear mensajes.
    
frightsEditOwned
  
> Miembros pueden editar todos los mensajes que pertenecen al usuario.
    
frightsDeleteOwned
  
> Miembro puede eliminar todos los mensajes que pertenecen al usuario.
    
frightsEditAny
  
> Miembro puede editar cualquier mensaje.
    
frightsDeleteAny
  
> Miembro puede eliminar cualquier mensaje.
    
frightsCreateSubfolder
  
> Miembro puede crear subcarpetas para la carpeta.
    
frightsOwner
  
> Miembro tiene todos los derechos anteriores en la carpeta.
    
frightsContact
  
> Miembro puede tener su nombre aparecen como el contacto en la carpeta.
    
frightsVisible
  
> Miembro puede ver que existe la carpeta.
    
rightsNone
  
> Miembro no tiene derechos en la carpeta.
    
rightsReadOnly
  
> Miembros pueden leer los mensajes en la carpeta.
    
rightsReadWrite
  
> Miembro puede leer desde y escribir en cualquier mensaje en la carpeta.
    
rightsAll
  
> Miembro tiene todos los derechos anteriores en la carpeta.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con los elementos de mensaje y calendario cuando actúen en nombre de otro usuario.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

