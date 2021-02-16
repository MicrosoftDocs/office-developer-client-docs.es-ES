---
title: Propiedad canónica PidLidAutoFillLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoFillLocation
api_type:
- COM
ms.assetid: e4db6cae-4730-45d0-8b8a-9bd484c8bd3f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2d1edf371486c5db0aa8b869726c8a9a7b62ab06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344999"
---
# <a name="pidlidautofilllocation-canonical-property"></a>Propiedad canónica PidLidAutoFillLocation

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que el valor de la propiedad **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) está establecido en la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del recipientRow que representa un recurso.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidAutoFillLocation  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000823A  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Reuniones  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener más información sobre RecipientRow, vea el protocolo Message y Attachment Object como se especifica en [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).
  
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

