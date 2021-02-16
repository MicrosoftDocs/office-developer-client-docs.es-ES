---
title: Propiedad canónica PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360070"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Propiedad canónica PidLidTaskMultipleRecipients

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona sugerencias de optimización sobre los destinatarios de una tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskMultRecips  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008120  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece, esta propiedad debe establecerse en una operación **OR** bit a bit de cero o más de los siguientes valores. 
  
|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |La tarea tiene varios destinatarios principales.  <br/> |
|Cantidad.Recibida  <br/> |0x00000002  <br/> |Aunque la sugerencia enviada no estaba presente, el cliente detectó que la tarea tiene varios destinatarios principales.  <br/> |
|Reserved  <br/> |0x00000004  <br/> |Este valor está reservado.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

