---
title: Propiedad canónica PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337964"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Propiedad canónica PidLidEmail2OriginalDisplayName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el segundo nombre para mostrar que corresponde a la dirección de correo electrónico especificada para el contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008094  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de la propiedad **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad **PidLidEmail2OriginalDisplayName** respectiva debe ser igual al valor de los respectivos ** propiedad dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)). La finalidad de esta propiedad es mostrar una dirección descriptiva alternativa que sea equivalente a la del **dispidEmail2EmailAddress**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

