---
title: Propiedad canónica PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358824"
---
# <a name="pidtagtemplateid-canonical-property"></a>Propiedad canónica PidTagTemplateid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expresado como un formato de identificador de entrada permanente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TEMPLATEID  <br/> |
|Identificador:  <br/> |0x3902  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Este valor debe estar presente para todos los objetos de la libreta de direcciones en un servidor de interfaz de proveedor de servicios de nombres (NSPI), su nombre distintivo (DN) debe coincidir con el valor de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y su DN debe seguir la especificación de formato DN específica para el tipo de objeto. 
  
Esta propiedad no está presente en objetos de una libreta de direcciones sin conexión.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

