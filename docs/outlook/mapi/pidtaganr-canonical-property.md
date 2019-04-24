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
  
Contiene un valor de tipo String que se usa en una restricción de propiedad en una tabla de contenido del contenedor de la libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Identificador:  <br/> |0x360C  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades no pertenecen a ningún objeto; la proporcionan los proveedores de libreta de direcciones en las estructuras [SPropertyRestriction](spropertyrestriction.md) . Esta propiedad contiene una cadena de resolución de nombres ambiguos (ANR) que puede probarse con una tabla de contenido de un contenedor de libreta de direcciones para buscar los destinatarios de mensajes correspondientes. 
  
Los proveedores de la libreta de direcciones coinciden con el valor de **PR_ANR** y las propiedades asociadas con todas las entradas de la tabla de contenido, utilizando un algoritmo de coincidencia definido por el proveedor. La columna o columnas que se usan en esta coincidencia las elige el proveedor como parte del algoritmo. La columna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es la que se usa con más frecuencia; la columna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) también es útil cuando contiene el nombre de correo electrónico del usuario. 
  
Para obtener más información acerca de la resolución de nombres ambiguos, consulte restricciones de la [Libreta de direcciones](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

