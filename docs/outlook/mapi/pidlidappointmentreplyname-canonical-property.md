---
title: Propiedad canónica PidLidAppointmentReplyName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356045"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a>Propiedad canónica PidLidAppointmentReplyName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el usuario que respondió por última vez a la solicitud de reunión o al objeto de actualización de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidApptReplyName  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008230  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad solo se establece para un delegador cuando un delegado respondió. El valor es igual a la **propiedad PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) del almacén del delegado. Esta propiedad no tiene ningún significado para el organizador. Para obtener más **información PR_MAILBOX_OWNER_NAME**, vea el protocolo de objetos de almacén especificado en [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Proporciona definiciones de tipo de datos.
    
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

