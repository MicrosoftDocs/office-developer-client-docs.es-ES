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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315914"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propiedad canónica PidLidRecurrenceType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el tipo de periodicidad de la serie periódica.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidRecurType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008231  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el tipo de periodicidad de la serie periódica mediante uno de los valores enumerados a continuación.
  
|**Estado**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Una cita de instancia única.  <br/> |
|rectypeDaily  <br/> |1   <br/> |Patrón de periodicidad diario.  <br/> |
|rectypeWeekly  <br/> |2   <br/> |Patrón de periodicidad semanal.  <br/> |
|rectypeMonthly  <br/> |3   <br/> |Patrón de periodicidad mensual.  <br/> |
|rectypeYearly  <br/> |4   <br/> |Patrón de periodicidad anual.  <br/> |
   
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

