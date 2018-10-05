---
title: Propiedad canónica PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383306"
---
# <a name="pidlidbusystatus-canonical-property"></a>Propiedad canónica PidLidBusyStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Representa la disponibilidad del usuario para una cita.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidBusyStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008205  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendario  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica la disponibilidad de un usuario para el evento descrito por el objeto y debe ser uno de los valores especificados por debajo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |El usuario está disponible.  <br/> |
|0x00000001  <br/> |El usuario tiene un evento provisional programado.  <br/> |
|0x00000002  <br/> |El usuario está ocupado.  <br/> |
|0 x 00000003  <br/> |El usuario no está en la oficina.  <br/> |
   
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

