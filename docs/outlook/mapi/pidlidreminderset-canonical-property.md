---
title: Propiedad canónica PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335157"
---
# <a name="pidlidreminderset-canonical-property"></a>Propiedad canónica PidLidReminderSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si se establece un aviso en el objeto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidReminderSet  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x00008503  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Comentarios

Si un objeto de calendario periódico tiene esta propiedad establecida en TRUE, el cliente puede invalidar este valor para excepciones.
  
Si esta propiedad es FALSE en un objeto de calendario periódico, los avisos se deshabilitan para toda la serie, incluidas las excepciones. Para los objetos de tarea periódicos, esta propiedad no se puede invalidar mediante excepciones (vea [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) y [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) para obtener más información). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

