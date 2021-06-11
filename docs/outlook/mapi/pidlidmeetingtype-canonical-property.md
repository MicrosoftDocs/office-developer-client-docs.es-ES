---
title: Propiedad canónica PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331580"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propiedad canónica PidLidMeetingType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el tipo de solicitud de reunión o actualización de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidMeetingType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Meeting  <br/> |
|Id. largo (LID):  <br/> |0x00000026  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta propiedad debe establecerse en uno de los siguientes valores:
  
|**Propiedad**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |No especificado.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Solicitud de reunión inicial.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Actualización completa.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Actualización informativo.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Después de esta, se recibió una nueva solicitud de reunión o actualización de reunión.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Esto se establece en la copia del delegado cuando un delegado controla objetos relacionados con reuniones.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

