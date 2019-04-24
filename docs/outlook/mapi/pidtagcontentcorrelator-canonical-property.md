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
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331979"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propiedad canónica PidTagContentCorrelator

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que el remitente del mensaje puede usar para hacer coincidir un informe con el mensaje original.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificador:  <br/> |0x0007  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

El contenido de la cadena binaria se define por el autor del mensaje. Si se establece en un mensaje saliente, esta propiedad debe copiarse en cualquier informe generado en respuesta al mensaje.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

