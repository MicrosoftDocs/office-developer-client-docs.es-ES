---
title: Propiedad canónica PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 884bbad509e459d4f329e6468dd99124cec6c7d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819598"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a>Propiedad canónica PidTagInitialDetailsPane

  
  
**Hace referencia a**: Outlook 
  
Indica la página de una plantilla de presentación para mostrar primero.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_INITIAL_DETAILS_PANE  <br/> |
|Identificador:  <br/> |0x3F08  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tablas MAPI para mostrar  <br/> |
   
## <a name="remarks"></a>Comentarios

Debe estar presente en todos los objetos de la libreta de direcciones en un servidor de la interfaz de proveedor de servicio de nombres (NSPI) y debe tener el valor cero (0). No se debe definir para los objetos en una libreta de direcciones sin conexión.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

