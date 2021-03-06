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
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359902"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propiedad canónica PidTagDelegateFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si un delegado puede ver los objetos de mensaje privados del delegado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificador:  <br/> |0x686B  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Transmitible definida por la clase message  <br/> |
   
## <a name="remarks"></a>Comentarios

Cada entrada de esta propiedad debe establecerse en uno de los siguientes valores.
  
|**Flag**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |No se debe permitir que el delegado vea objetos de mensaje privados.  <br/> |
|ShowPrivate  <br/> |1  <br/> |El delegado debe tener permiso para ver objetos de mensaje privados.  <br/> |
   
Esta propiedad debe establecerse en el objeto de información de delegado. El valor de "ShowPrivate" indica que el delegado desea que los objetos de mensaje privados sean visibles. Esta preferencia se aplica a todas las carpetas para las que el delegado tiene un rol de revisor, autor o editor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

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

