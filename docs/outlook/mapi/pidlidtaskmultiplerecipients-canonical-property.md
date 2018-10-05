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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391174"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Propiedad canónica PidLidTaskMultipleRecipients

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Proporciona optimización de las sugerencias acerca de los destinatarios de una tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskMultRecips  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008120  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece, esta propiedad debe establecerse en una operación **OR** bit a bit de cero o más de los siguientes valores. 
  
|**Nombre**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|Enviado  <br/> |0x00000001  <br/> |La tarea tiene varios destinatarios principales.  <br/> |
|Cantidad.Recibida  <br/> |0x00000002  <br/> |Aunque la sugerencia enviados no estuviera presente, el cliente detecta que la tarea tiene varios destinatarios principales.  <br/> |
|Reservado  <br/> |0 x 00000004  <br/> |Este valor está reservado.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

