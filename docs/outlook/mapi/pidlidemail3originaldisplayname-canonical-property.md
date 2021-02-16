---
title: Propiedad canónica PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338076"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>Propiedad canónica PidLidEmail3OriginalDisplayName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el tercer nombre para mostrar que corresponde a la dirección de correo electrónico especificada para el contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x000080A4  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de la propiedad **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad **dispidEmail3OriginalDisplayName** correspondiente debe ser igual al valor de la **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)). El propósito de esta propiedad es mostrar una dirección alternativa fácil de usar que es equivalente a la de **dispidEmail3EmailAddress**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

