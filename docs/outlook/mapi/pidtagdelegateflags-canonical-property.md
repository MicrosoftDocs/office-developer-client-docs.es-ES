---
title: Propiedad canónica PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d43ec0bd2978c64e3a5ceb635f0dcda57de01cfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590739"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propiedad canónica PidTagDelegateFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si un delegado puede ver objetos de mensaje privado de la persona que delega.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificador:  <br/> |0x686B  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Mensaje definido por la clase transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Cada entrada de esta propiedad debe establecerse en uno de los valores siguientes.
  
|**Flag**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |El delegado no deberían ver objetos de mensaje privado.  <br/> |
|ShowPrivate  <br/> |1  <br/> |El delegado debe permitirse para ver objetos de mensaje privado.  <br/> |
   
Esta propiedad se debe establecer en el objeto de información de delegado. El valor de "ShowPrivate" indica que el usuario delegado desea hacer que los objetos de mensaje privado que esté visible. Esta preferencia es aplicable a todas las carpetas para los que el delegado tiene un rol de revisor, el autor o editor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

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

