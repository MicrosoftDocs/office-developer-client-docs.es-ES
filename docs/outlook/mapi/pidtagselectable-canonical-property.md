---
title: Propiedad canónica PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359020"
---
# <a name="pidtagselectable-canonical-property"></a>Propiedad canónica PidTagSelectable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si se puede seleccionar la entrada de la tabla de uso único. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SELECTABLE  <br/> |
|Identificador:  <br/> |0x3609  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Contenedor de libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa principalmente para el formato visual de una tabla de un solo uso. Las plantillas se pueden agrupar creando una entrada que indique el encabezado del grupo. Si se establece esta propiedad en FALSE para el encabezado, se garantiza que el usuario puede seleccionar sólo las plantillas reales del grupo y no esta entrada de encabezado. 
  
Esta propiedad solo se aplica a una tabla de un solo uso, no a una tabla de jerarquía de la libreta de direcciones. 
  
MAPI permite que un proveedor de libreta de direcciones agrupe los elementos visualmente por dos medios. En primer lugar, ciertas filas pueden funcionar como encabezados al no ser seleccionables. En segundo lugar, los elementos seleccionables se pueden sangrar con relación a sus encabezados mediante la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Esta propiedad se usa en dicha agrupación para indicar si este elemento se puede seleccionar de una lista para crear una dirección de un solo uso. Por ejemplo, si un cliente tiene varias plantillas para crear direcciones de fax, puede mostrarlas de la siguiente manera: 
  
Plantillas de FAX (profundidad 0, no seleccionable)
  
 Local (profundidad 1, seleccionable) 
  
 A larga distancia (profundidad 1, seleccionable) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para las plantillas de la libreta de direcciones.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propiedad canónica PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

