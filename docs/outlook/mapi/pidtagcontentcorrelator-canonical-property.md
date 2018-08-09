---
title: Propiedad canónica PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819355"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propiedad canónica PidTagContentCorrelator

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor que se puede usar el remitente del mensaje para que coincida con un informe con el mensaje original.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificador:  <br/> |0 x 0007  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

El contenido de la cadena binaria se define por el autor del mensaje. Si se configura en un mensaje saliente, esta propiedad debe copiarse en cualquier informes generados en respuesta al mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

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

