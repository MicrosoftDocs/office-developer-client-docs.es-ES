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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342697"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propiedad canónica PidTagMemberRights

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un conjunto de bits que indica los derechos de este miembro en una carpeta o buzón.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificador:  <br/> |0x6673  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) usa esta propiedad para definir los derechos de un miembro en una carpeta. Estos derechos se pueden mostrar y modificar. Los siguientes valores son derechos definidos para esta propiedad. 
  
frightsReadAny
  
> El miembro puede leer cualquier mensaje.
    
frightsCreate
  
> El miembro puede crear mensajes.
    
frightsEditOwned
  
> El miembro puede editar cualquier mensaje que sea propiedad del usuario.
    
frightsDeleteOwned
  
> El miembro puede eliminar cualquier mensaje que sea propiedad del usuario.
    
frightsEditAny
  
> El miembro puede editar cualquier mensaje.
    
frightsDeleteAny
  
> El miembro puede eliminar cualquier mensaje.
    
frightsCreateSubfolder
  
> El miembro puede crear subcarpetas para la carpeta.
    
frightsOwner
  
> El miembro tiene todos los derechos anteriores en la carpeta.
    
frightsContact
  
> El miembro puede hacer que su nombre aparezca como contacto en la carpeta.
    
frightsVisible
  
> El miembro puede ver que la carpeta existe.
    
rightsNone
  
> El miembro no tiene derechos en la carpeta.
    
rightsReadOnly
  
> El miembro puede leer cualquier mensaje de la carpeta.
    
rightsReadWrite
  
> El miembro puede leer y escribir en cualquier mensaje de la carpeta.
    
rightsAll
  
> El miembro tiene todos los derechos anteriores en la carpeta.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Controla la recuperación de listas de permisos de carpetas almacenadas en el servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse a buzones y configurarlos como delegados e interacciones con elementos de calendario y mensajes cuando actúan en nombre de otro usuario.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

