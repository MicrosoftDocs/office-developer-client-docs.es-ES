---
title: Propiedad canónica PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818471"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Propiedad canónica PidLidAppointmentColor

  
  
**Hace referencia a**: Outlook 
  
Especifica el color para utilizarla al mostrar el calendario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptColor  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008214  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el color para utilizarla al mostrar el calendario. Un cliente o servidor debe establecer este valor para la compatibilidad con versiones anteriores con los clientes más antiguos. En su lugar, puede mostrar el calendario en función del valor de la propiedad **palabras clave** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) como especifica en [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Cuando se establece, el valor debe ser uno de los siguientes.
  
|**Valor**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Ninguno  <br/> |
|0x00000001  <br/> |Rojo  <br/> |
|0x00000002  <br/> |Azul  <br/> |
|0 x 00000003  <br/> |Verde  <br/> |
|0 x 00000004  <br/> |Gris  <br/> |
|0 x 00000005  <br/> |Naranja  <br/> |
|0 x 00000006  <br/> |Cian  <br/> |
|0 x 00000007  <br/> |Oliva  <br/> |
|0 x 00000008  <br/> |Púrpura  <br/> |
|0 x 00000009  <br/> |Verde azulado  <br/> |
|0x0000000A  <br/> |Amarillo  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

