---
title: Propiedad canónica PidLidRecurrenceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389179"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propiedad canónica PidLidRecurrenceType

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica el tipo de periodicidad de la serie periódica.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidRecurType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008231  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el tipo de periodicidad de la serie periódica mediante el uso de uno de los valores enumerados a continuación.
  
|**Status**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Una cita de una sola instancia.  <br/> |
|rectypeDaily  <br/> |1  <br/> |Un patrón de periodicidad diario.  <br/> |
|rectypeWeekly  <br/> |2  <br/> |Un patrón de periodicidad semanal.  <br/> |
|rectypeMonthly  <br/> |3  <br/> |Un patrón de periodicidad mensual.  <br/> |
|rectypeYearly  <br/> |4  <br/> |Un patrón de periodicidad anual.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

