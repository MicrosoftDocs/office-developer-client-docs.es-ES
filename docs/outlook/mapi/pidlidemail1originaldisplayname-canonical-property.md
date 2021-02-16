---
title: Propiedad canónica PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335045"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a>Propiedad canónica PidLidEmail1OriginalDisplayName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el primer nombre para mostrar que corresponde a la dirección de correo electrónico especificada para el contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidEmail1OriginalDisplayName  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008084  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el valor de la propiedad **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad **dispidEmail1OriginalDisplayName** correspondiente debe ser igual al valor de la propiedad **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) respectiva. Esta propiedad muestra una dirección de usuario alternativa que es equivalente a la de la propiedad **dispidEmail1EmailAddress.** 
  
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

