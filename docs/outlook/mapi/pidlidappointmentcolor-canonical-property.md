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
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345440"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Propiedad canónica PidLidAppointmentColor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el color que se debe usar al mostrar el calendario.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptColor  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008214  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el color que se va a usar al mostrar el calendario. Un cliente o servidor debe establecer este valor para la compatibilidad con versiones anteriores con clientes antiguos. En su lugar, puede mostrar el calendario en función del valor de la propiedad **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) tal como se especifica en [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Cuando se establece, el valor debe ser uno de los siguientes.
  
|**Valor**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Ninguno  <br/> |
|0x00000001  <br/> |Rojo  <br/> |
|0x00000002  <br/> |Azul  <br/> |
|0x00000003  <br/> |Verde  <br/> |
|0x00000004  <br/> |Gris  <br/> |
|0x00000005  <br/> |Anaranjado  <br/> |
|0x00000006  <br/> |Aguamarina  <br/> |
|0x00000007  <br/> |Oliva  <br/> |
|0x00000008  <br/> |Púrpura  <br/> |
|0x00000009  <br/> |Verde azulado  <br/> |
|0x0000000A  <br/> |Amarillo  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

