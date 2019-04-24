---
title: Propiedad canónica PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316411"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propiedad canónica PidTagExpiryUnits

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la unidad de tiempo en la que la propiedad **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplica.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificador:  <br/> |0x3FEE  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad, si se establece, debe ser uno de los siguientes valores:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |DeScription (tiempo)  <br/> |
|0x00000000  <br/> |Minutos, por ejemplo 60 segundos  <br/> |
|0x00000001  <br/> |Horas, por ejemplo 60x60 segundos  <br/> |
|0x00000002  <br/> |Día, por ejemplo 24x60x60 segundos  <br/> |
|0x00000003  <br/> |Semana, por ejemplo 7x24x60x60 segundos  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.
    
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

