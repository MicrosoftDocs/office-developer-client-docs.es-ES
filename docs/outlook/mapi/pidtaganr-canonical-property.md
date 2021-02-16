---
title: Propiedad canónica PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327968"
---
# <a name="pidtaganr-canonical-property"></a>Propiedad canónica PidTagAnr

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de cadena para su uso en una restricción de propiedad en una tabla de contenido de contenedor de libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificador:  <br/> |0x360C  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades no pertenecen a ningún objeto; lo ofrecen los proveedores de libretas de direcciones en [estructuras SPropertyRestriction.](spropertyrestriction.md) Esta propiedad contiene una cadena de resolución de nombres ambiguos (ANR) que se puede probar con la tabla de contenido de un contenedor de libreta de direcciones para buscar los destinatarios de mensajes correspondientes. 
  
Los proveedores de libretas de direcciones coinciden con el valor de **PR_ANR** y las propiedades asociadas con cada entrada de la tabla de contenido, mediante un algoritmo de coincidencia definido por el proveedor. El proveedor elige la columna o las columnas que se usan en esta coincidencia como parte del algoritmo. La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es la más usada; la **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) también es útil cuando contiene el nombre de correo electrónico del usuario. 
  
Para obtener más información sobre la resolución de nombres ambiguos, vea [Restricciones de la libreta de direcciones.](address-book-restrictions.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

