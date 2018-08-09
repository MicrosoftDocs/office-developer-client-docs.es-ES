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
ms.openlocfilehash: 225c435107ba79183c737ddb8e09cda1ffbd83f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820250"
---
# <a name="pidtagselectable-canonical-property"></a>Propiedad canónica PidTagSelectable

  
  
**Hace referencia a**: Outlook 
  
Contiene TRUE si se puede seleccionar la entrada en la tabla de uso único. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SELECTABLE  <br/> |
|Identificador:  <br/> |0x3609  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Contenedor de la libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa principalmente para el formato visual de una tabla de uso único. Las plantillas se pueden agrupar mediante la creación de una entrada que indica el título para el grupo. Al establecer esta propiedad en FALSE para el encabezado se asegura de que el usuario puede seleccionar sólo las plantillas reales en el grupo y no esta entrada del encabezado. 
  
Esta propiedad se aplica sólo a una tabla de uso único, no a una tabla de jerarquía de la libreta de direcciones. 
  
MAPI permite a un proveedor de la libreta de direcciones para agrupar los elementos visualmente por medio de dos. En primer lugar, algunas filas pueden funcionar como encabezados de forma no seleccionable. En segundo lugar, los elementos seleccionables aplicará sangría con respecto a sus encabezados mediante el uso de la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Esta propiedad se usa en esa agrupación para indicar si este elemento se puede seleccionar de una lista para crear una dirección de uso único. Por ejemplo, si un cliente tiene varias plantillas para la creación de direcciones de fax, lo puede mostrarlos como se indica a continuación: 
  
Plantillas de FAX (profundidad 0, no se puede seleccionar)
  
 Local (profundidad 1, seleccionable) 
  
 Llamadas de larga distancia (profundidad de 1, seleccionable) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para las plantillas de la libreta de direcciones.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Propiedad canónica PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

